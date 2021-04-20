---
description: Utilice el menú Filtrado para utilizar secuencias de comandos que cambien el contenido de un documento web antes de indexarlo.
solution: Target
subtopic: Filtering
title: Acerca del menú Filtrado
topic: Settings,Site search and merchandising
uuid: ebb08fa8-4e17-417d-868b-11fc2af9f284
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '4008'
ht-degree: 1%

---


# Acerca del menú Filtrado{#about-the-filtering-menu}

Utilice el menú Filtrado para utilizar secuencias de comandos que cambien el contenido de un documento web antes de indexarlo.

## Acerca del filtro de script {#concept_E56B73D625854AB2A899EF2D56CFCB47}

Puede utilizar [!DNL Filtering Script] para cambiar el contenido de un documento Web antes de que se indexe.

Puede insertar etiquetas HTML, eliminar contenido irrelevante e incluso crear nuevos metadatos HTML basados en la URL, el tipo MIME y el contenido existente de un documento. El script de filtrado es un script Perl, que proporciona una potente gestión de cadenas y la flexibilidad de la coincidencia de expresiones regulares. La secuencia de comandos de filtrado se utiliza con una secuencia de comandos de inicialización, una secuencia de comandos de finalización, una secuencia de comandos de máscaras de URL y una URL de prueba.

La secuencia de comandos de filtrado se ejecuta cada vez que se lee un documento desde el sitio web. La secuencia de comandos se ejecuta como filtro estándar; en otras palabras, lee datos de STDIN, los transforma de alguna manera y escribe los resultados en STDOUT. Puede utilizar la secuencia de comandos de filtrado para imprimir los mensajes de estado de la secuencia de comandos de filtrado en el registro de índice. Los mensajes se imprimen en STDERR o a través de la subrutina `_search_debug_log()`.

Algunas opciones de diferencia GNU que puede usar mientras está en modo **[!UICONTROL Expert (diff)]** en la página Script de filtrado por etapas son las siguientes:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opción GNU diff </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
   <td colname="col2"> <p> Omite los cambios en la cantidad de espacio en blanco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
   <td colname="col2"> <p> Omite los cambios que insertan o eliminan líneas en blanco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida de contexto, que muestra tres líneas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Líneas C  </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida de contexto, que muestra líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> Ignora los cambios en mayúsculas y minúsculas; considere equivalentes las letras mayúsculas y minúsculas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Convierte la salida en similar a un script ed pero tiene cambios en el orden en que aparece en el archivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> produce diferencias en formato RCS; como <span class="codeph"> -f </span> excepto que cada comando especifica el número de líneas afectadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra tres líneas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -Líneas U  </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra las líneas (un número entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puede utilizar variables locales, variables globales o ambas en estas secuencias de comandos. A todas las variables globales se les agregará el prefijo del área de nombres &quot;main::&quot;. Cuando se inicia el script de filtrado, su entorno contiene los siguientes controladores de archivo estándar:

* STDIN: nada (devuelve EOF inmediatamente cuando se lee)
* STDOUT: reemplace HTML (si los datos se imprimen en STDOUT, se utilizan en lugar del documento original)
* STDERR: los datos impresos en STDERR se imprimen en el registro de índices como un error

Además, puede escribir mensajes personalizados en el registro de índices mediante la subrutina `_search_debug_log()` , como en el siguiente ejemplo:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Estos mensajes aparecen con la palabra `DEBUG` como prefijo y no se registran como errores.

El siguiente es un ejemplo de filtrado. Los campos `<title>` de la página web suelen comenzar con el nombre de la empresa. Aunque esta información es útil para la navegación del sitio, no es relevante cuando se realiza la búsqueda. Si los títulos de todas las páginas web de MegaCorp comienzan con una cadena común, como la siguiente:

```
<title>MegaCorp -- meaningful title 
here</title>
```

Debe eliminar &quot;`MegaCorp --`&quot; desde el principio de cada título de documento y contar cada documento procesado con la secuencia de comandos de filtrado. Para ello, puede utilizar la siguiente secuencia de comandos:

```
# Make sure this is an HTML document. 
if ($main::ws_content_type =~ /^text\/html/) { 
    # Read the entire document into a local scalar variable. 
    my @docarray = <>; 
    my $doc = join("", @docarray); 
 
    # Remove "MegaCorp -- " from the title. 
    $doc =~ s/(<TITLE>)MegaCorp -- /$1/gis; 
 
    # Print the resulting document. 
    print $doc; 
 
    # Count that we've filtered one more document. 
    $main::doc_count++; 
}
```

## Variables globales {#global-variables}

Puede utilizar las siguientes variables en cualquier script de filtrado:

| Variable | Descripción |
|--- |--- |
| `$main::search_crawl_type` | El valor de `$main::search_crawl_type` indica el tipo de operación de índice en curso.  Forma obsoleta: `$main::ws_crawl_type` Las operaciones de índice y los valores asociados incluyen lo siguiente: <ul><li>Índice completo: Manual - `manual`</li><li>Índice completo: Programado - `auto`</li><li>Índice completo: Control remoto - `CGI`</li><li>Índice incremental: Manual - `manual-incremental`</li><li>Índice incremental: Programado - `auto-incremental` </li><li>Índice incremental: Control remoto - `CGI-incremental`</li><li>Índice con secuencias de comandos: Manual - `manual-indexlist.txt` </li><li>Índice con secuencias de comandos: Programado - `auto-indexlist.txt`</li><li>Índice con secuencias de comandos: Control remoto - `CGI-indexlist.txt`</li><li>Regenerar - `manual-upgrade`</li></ul> |
| `$main::search_clear_cache` | El valor indica si la opción de indexación &quot;Borrar caché de índice&quot; se solicitó para la operación de índice actual. Si se solicitó &quot;Borrar caché de índice&quot;, el valor de `$main::search_clear_cache` es &quot; `1`&quot;.  Forma obsoleta: `$main::ws_clear_cache` |
| `$main::search_fields` | El valor contiene una lista separada por tabuladores de los campos de metadatos definidos en la cuenta. De forma predeterminada, el valor es:   `url title desc keys target body alt date charset language` Forma obsoleta: `$main::ws_fields` |
| `$main::search_collections` | El valor contiene una lista separada por tabuladores de las colecciones que se definen en la cuenta.  Forma obsoleta: `$main::ws_collections` |
| `$main::search_url` | El valor es la dirección URL completa del documento.  Forma obsoleta: `$main::ws_url` |
| `$main::search_content_type` | El valor es el tipo de contenido del documento tal como se obtiene de la metaetiqueta http-equiv . Un valor típico es &quot;text/html; charset=iso-8859-1&quot;.  Forma obsoleta: `$main::ws_content_type` |
| `$main::search_content_class` | El valor es la clase de contenido del documento, tal como se deriva del campo de tipo de contenido.  Forma obsoleta: `$main::ws_content_class` |
| `$main::search_syntax_check` | El valor refleja el uso del botón &quot;Comprobar sintaxis&quot;. Si se hace clic, el valor es 1 (uno); de lo contrario, su valor es 0 (cero).  Forma obsoleta: `$main::ws_syntax_check` |
| `$main::search_last_mod_date` | Si lo proporciona el servidor web, este valor contiene la representación de Epoch (segundos transcurridos desde el 1 de enero de 1970) de la fecha de la última modificación del documento.  Puede dar formato a este valor utilizando la llamada de biblioteca Perl localtime() . |

### Sugerencias rápidas {#section_89A5C16911744AF98E232DF608C6A1F5}

* A todas las variables globales se les agregará el área de nombres &quot;main::&quot;: `$main::doc_count = 0;`
* Todas las variables locales se declaran con &quot;my&quot;: `my $i = 0;`
* Las subrutinas se definen en la secuencia de comandos de inicialización. No necesitan un espacio de nombres &quot;main::&quot; explícito: `sub my_sub {` `...`

   `}`

* Pruebe `$main::search_content_type` antes de realizar cambios en un archivo. Las pruebas pueden ayudar a evitar realizar cambios sin cuidado en archivos binarios, como archivos SWF o archivos PDF:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* El `$main::search_content_type` es el encabezado Content-Type completo que su servidor entrega. A veces puede contener un tipo MIME simple, como &quot;text/html&quot;. O bien, puede contener un tipo MIME seguido de otra información, como la codificación del conjunto de caracteres del documento, como &quot;text/html; charset=iso-8859-1&quot;.
* Para cada tipo de documento no HTML, `$main::search_content_type` puede tomar varios valores. La prueba de cada valor en la secuencia de comandos se vuelve engorrosa. Por ejemplo, algunos documentos de Word tienen valores de tipo de contenido de &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; o &quot;application/x-msword&quot;. En estos casos, `$main::search_content_class` puede tomar los siguientes valores:

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* En el ejemplo, probar `$main::search_content_class` para &quot;word&quot; coincidiría con cualquiera de los tres valores posibles de tipo de contenido.
* Si no se imprime nada en STDOUT desde el script de filtrado, el documento se utiliza exactamente como se descargó. Es decir, si no necesita cambiar nada en un documento, no necesita copiar STDIN en STDOUT para ese documento.
* Si desea quitar todo el texto de un documento, imprima un archivo válido STDOUT. Por ejemplo, para eliminar todo el texto de un documento HTML, haga lo siguiente: `print "<html></html>";`

## Adición de un script de filtrado {#task_0AB84FD1133F47F9AA069A79BEA13A22}

El script de filtrado es un script Perl que se ejecuta para cada documento descargado del sitio web.

La secuencia de comandos de filtrado se utiliza junto con una secuencia de comandos de inicialización, una secuencia de comandos de finalización y una secuencia de comandos de máscaras de URL.

Asegúrese de reconstruir el índice del sitio para que los resultados del script de filtrado sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Adición de una secuencia de comandos de filtrado**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Filtering Script]**.
1. (Opcional) En la página [!DNL Filtering Script], en el campo [!DNL Test URL], introduzca la dirección URL de un documento en el sitio web.

   Haga clic en una opción de prueba para ver los cambios en el texto HTML sin procesar.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Campo de dirección URL de prueba </p> </td> 
      <td colname="col2"> <p>Permite introducir la dirección URL de un documento en el sitio web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Prueba </p> </td> 
      <td colname="col2"> <p>Comprueba la dirección URL con las secuencias de comandos de filtrado y las máscaras de URL. </p> <p>Se descarga el documento de la URL de prueba, que luego se utiliza como entrada STDIN en el script de filtrado. A continuación, se ejecutan las secuencias de comandos de inicialización, filtrado y finalización. Si hay alguna salida STDOUT del script de filtrado, esa salida se muestra en una nueva ventana del navegador. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Solo prueba </p> </td> 
      <td colname="col2"> <p>Prueba únicamente la operación de la secuencia de comandos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Vista previa </p> </td> 
      <td colname="col2"> <p>Permite ver la página. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Completo visual </p> </td> 
      <td colname="col2"> <p>Genera una vista de tabla completa antes y después de los documentos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Abreviado visual </p> </td> 
      <td colname="col2"> <p>Muestra únicamente las diferencias entre las vistas anteriores y posteriores. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Experto (diff) </p> </td> 
      <td colname="col2"> <p>Muestra la salida sin procesar del comando GNU diff que se usa para comparar los archivos, usando las opciones de línea de comandos suministradas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Filtrado de secuencias de comandos </p> </td> 
      <td colname="col2"> <p>Permite pegar la secuencia de comandos de filtrado en el campo proporcionado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Guardar cambios </p> </td> 
      <td colname="col2"> <p>Guarda el script de filtrado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Comprobar sintaxis </p> </td> 
      <td colname="col2"> <p>Permite comprobar rápidamente la sintaxis de la secuencia de comandos ejecutando las secuencias de comandos de inicialización, filtrado y finalización. No actualiza ni guarda el script. </p> <p>Se imprimen todos los errores y advertencias del compilador de Perl y todos los resultados de STDERR. </p> <p>Antes de que los efectos de la secuencia de comandos sean visibles para los clientes, debe volver a generar el índice del sitio. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opciones de línea de comandos de GNU diff**

   Algunas opciones de diferencia GNU que puede usar mientras está en modo **[!UICONTROL Expert (diff)]** en la página Script de filtrado por etapas son las siguientes:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción de línea de comandos GNU diff </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
      <td colname="col2"> <p> Omite los cambios en la cantidad de espacio en blanco. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
      <td colname="col2"> <p> Omite los cambios que insertan o eliminan líneas en blanco. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
      <td colname="col2"> <p> Utiliza el formato de salida de contexto, que muestra tres líneas de contexto. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> Líneas C  </span> </p> </td> 
      <td colname="col2"> <p> Utiliza el formato de salida de contexto, que muestra líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
      <td colname="col2"> <p> Ignora los cambios en mayúsculas y minúsculas; considere equivalentes las letras mayúsculas y minúsculas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
      <td colname="col2"> <p> Convierte la salida en similar a un script ed pero tiene cambios en el orden en que aparece en el archivo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
      <td colname="col2"> <p> produce diferencias en formato RCS; como <span class="codeph"> -f </span> excepto que cada comando especifica el número de líneas que se ven afectadas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>-u </p> </td> 
      <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra tres líneas de contexto. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -Líneas U  </span> </p> </td> 
      <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra las líneas (un número entero) de contexto o tres si no se dan líneas. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic en **[!UICONTROL Test]** para realizar pruebas con los scripts de filtrado y las máscaras de URL.

   Al hacer clic en **[!UICONTROL Test]** no se actualiza ni se guarda el script de filtrado.
1. En el campo [!DNL Filtering Script] , pegue la secuencia de comandos.
1. (Opcional) Haga clic en **[!UICONTROL Check Syntax]** para realizar una comprobación rápida de la sintaxis de la secuencia de comandos ejecutando las secuencias de comandos de filtrado, inicialización y finalización.

   **[!UICONTROL Check Syntax]** no actualiza ni guarda el script.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstruya el índice del sitio provisional si desea obtener una vista previa de los resultados.

   Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) En la página [!DNL Filtering Script], realice una de las acciones siguientes:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del script de inicialización {#concept_048B4C8BC9F74BE8BB6162C490C201A3}

Puede utilizar [!DNL Initialization Script] para cambiar el contenido de un documento Web antes de que se indexe.

Puede insertar etiquetas HTML, eliminar contenido irrelevante e incluso crear nuevos metadatos HTML basados en la URL, el tipo MIME y el contenido existente de un documento. La secuencia de comandos de inicialización es una secuencia de comandos Perl, que proporciona una potente gestión de cadenas y la flexibilidad de la coincidencia de expresiones regulares. La secuencia de comandos de inicialización se utiliza con una secuencia de comandos de filtrado, una secuencia de comandos de finalización, una secuencia de comandos de máscaras de URL y una URL de prueba.

La secuencia de comandos de inicialización se ejecuta una vez antes de que comience la indexación. Utilice esta secuencia de comandos para inicializar las variables y subrutinas globales que utilice el script de filtrado. Puede utilizar la secuencia de comandos de inicialización para imprimir mensajes de estado desde la secuencia de comandos de filtrado al registro de índice. Los mensajes se imprimen en STDERR o a través de la subrutina `_search_debug_log()`.

Algunas opciones de diferencia GNU que puede usar mientras está en modo **[!UICONTROL Expert (diff)]** en la página Script de inicialización por etapas son las siguientes:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opción GNU diff </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> Omite los cambios en la cantidad de espacio en blanco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> Omite los cambios que insertan o eliminan líneas en blanco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida de contexto, que muestra tres líneas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Líneas C  </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida de contexto, que muestra líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> Ignora los cambios en mayúsculas y minúsculas; considere equivalentes las letras mayúsculas y minúsculas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Convierte la salida en similar a un script ed pero tiene cambios en el orden en que aparece en el archivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> produce diferencias en formato RCS; como <span class="codeph"> -f </span> excepto que cada comando especifica el número de líneas afectadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra tres líneas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -Líneas U  </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra las líneas (un número entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puede utilizar variables locales, variables globales o ambas en estas secuencias de comandos. A todas las variables globales se les agregará el prefijo del área de nombres &quot;main::&quot;. Cuando se inicia la secuencia de comandos de inicialización, su entorno contiene los siguientes identificadores de archivo estándar:

* STDIN: nada (devuelve EOF inmediatamente cuando se lee)
* STDOUT: nada (si los datos se imprimen en STDOUT, se descartan)
* STDERR: los datos impresos en STDERR se imprimen en el registro de índices como un error

Además, puede escribir mensajes personalizados en el registro de índices mediante la subrutina `_search_debug_log()` , como en el siguiente ejemplo:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Estos mensajes aparecen con la palabra `DEBUG` como prefijo y no se registran como errores.

Un ejemplo de secuencia de comandos de inicialización es el siguiente:

```
# My subroutine to do something. 
sub my_sub_for_the_filtering_script { 
    my ($param1, $param2) = @_; 
    ... 
} 
 
# Initialize the document counter. 
$main::doc_count = 0;
```

Consulte [Variables globales](#global-variables)

### Sugerencias rápidas {#section_A2CC0302CAF14135BF8EF6171FB184F1}

* A todas las variables globales se les agregará el área de nombres &quot;main::&quot;: `$main::doc_count = 0;`
* Todas las variables locales se declaran con &quot;my&quot;: `my $i = 0;`
* Las subrutinas se definen en la secuencia de comandos de inicialización. No necesitan un espacio de nombres &quot;main::&quot; explícito: `sub my_sub {` `...`

   `}`

* Pruebe `$main::search_content_type` antes de realizar cambios en un archivo. Las pruebas pueden ayudar a evitar realizar cambios sin cuidado en archivos binarios, como archivos SWF o archivos PDF:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* El `$main::search_content_type` es el encabezado Content-Type completo que su servidor entrega. A veces puede contener un tipo MIME simple, como &quot;text/html&quot;. O bien, puede contener un tipo MIME seguido de otra información, como la codificación del conjunto de caracteres del documento, como &quot;text/html; charset=iso-8859-1&quot;.
* Para cada tipo de documento no HTML, `$main::search_content_type` puede tomar varios valores. La prueba de cada valor en la secuencia de comandos se vuelve engorrosa. Por ejemplo, algunos documentos de Word tienen valores de tipo de contenido de &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; o &quot;application/x-msword&quot;. En estos casos, `$main::search_content_class` puede tomar los siguientes valores:

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* En el ejemplo, probar `$main::search_content_class` para &quot;word&quot; coincidiría con cualquiera de los tres valores posibles de tipo de contenido.
* Si no se imprime nada en STDOUT desde el script de filtrado, el documento se utiliza exactamente como se descargó. Es decir, si no necesita cambiar nada en un documento, no necesita copiar STDIN en STDOUT para ese documento.
* Si desea quitar todo el texto de un documento, imprima un archivo válido STDOUT. Por ejemplo, para eliminar todo el texto de un documento HTML, haga lo siguiente: `print "<html></html>";`

## Adición de una secuencia de comandos de inicialización {#task_5A03B8D0C46E4674B7CE88203515803B}

La secuencia de comandos de inicialización es una secuencia de comandos Perl que se ejecuta una vez antes de que se indiquen los documentos.

La secuencia de comandos de inicialización se utiliza junto con una secuencia de comandos de filtrado, una secuencia de comandos de finalización y una secuencia de comandos de máscaras de URL.

Asegúrese de reconstruir el índice del sitio para que los resultados de la secuencia de comandos de inicialización sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Adición de una secuencia de comandos de inicialización**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Initialization Script]**.
1. (Opcional) En la página [!DNL Initialization Script], en el campo [!DNL Test URL], introduzca la dirección URL de un documento en el sitio web.

   Haga clic en una opción de prueba para ver los cambios en el texto HTML sin procesar.

   Consulte la tabla de opciones de filtrado en **Añadir un script de filtrado**.

   Haga clic en **[!UICONTROL Test]** para realizar pruebas con los scripts de filtrado y las máscaras de URL.

   Al hacer clic en **[!UICONTROL Test]** no se actualiza ni se guarda la secuencia de comandos de inicialización.
1. En el campo [!DNL Initialization Script] , pegue la secuencia de comandos.
1. (Opcional) Haga clic en **[!UICONTROL Check Syntax]** para realizar una comprobación rápida de la sintaxis de la secuencia de comandos ejecutando las secuencias de comandos de filtrado, inicialización y finalización.

   **[!UICONTROL Check Syntax]** no actualiza ni guarda el script.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstruya el índice del sitio provisional si desea obtener una vista previa de los resultados.

   Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) En la página [!DNL Initialization Script], realice una de las acciones siguientes:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del script de finalización {#concept_AAD6B3B0E7124874AD0947096FC42F47}

Puede utilizar [!DNL Termination Script] para cambiar el contenido de un documento Web antes de que se indexe.

Puede insertar etiquetas HTML, eliminar contenido irrelevante e incluso crear nuevos metadatos HTML basados en la URL, el tipo MIME y el contenido existente de un documento. La secuencia de comandos de inicialización es una secuencia de comandos Perl, que proporciona una potente gestión de cadenas y la flexibilidad de la coincidencia de expresiones regulares. La secuencia de comandos de finalización se utiliza con una secuencia de comandos de inicialización, una secuencia de comandos de filtrado, una secuencia de comandos de finalización, una secuencia de comandos de máscaras de URL y una URL de prueba.

La secuencia de comandos de terminación se ejecuta una vez después de indexar todos los documentos. Puede utilizar la secuencia de comandos de terminación para imprimir los mensajes de estado de la secuencia de comandos de filtrado en el registro de índice. Los mensajes se imprimen en STDERR o a través de la subrutina `_search_debug_log()`.

Algunas opciones de la línea de comandos de GNU diff que puede usar mientras está en modo **[!UICONTROL Expert (diff)]** en la página Script de terminación por etapas son las siguientes:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opción de línea de comandos GNU diff </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> Omite los cambios en la cantidad de espacio en blanco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> Omite los cambios que insertan o eliminan líneas en blanco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida de contexto, que muestra tres líneas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Líneas C  </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida de contexto, que muestra líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> Ignora los cambios en mayúsculas y minúsculas; considere equivalentes las letras mayúsculas y minúsculas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Convierte la salida en similar a un script ed pero tiene cambios en el orden en que aparece en el archivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> produce diferencias en formato RCS; como <span class="codeph"> -f </span> excepto que cada comando especifica el número de líneas que se ven afectadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra tres líneas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -Líneas U  </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra las líneas (un número entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puede utilizar variables locales, variables globales o ambas en estas secuencias de comandos. A todas las variables globales se les agregará el prefijo del área de nombres &quot;main::&quot;. Cuando se inicia la secuencia de comandos de terminación, su entorno contiene los siguientes identificadores de archivo estándar:

* STDIN: nada (devuelve EOF inmediatamente cuando se lee)
* STDOUT: nada (si los datos se imprimen en STDOUT, se descartan)
* STDERR: los datos impresos en STDERR se imprimen en el registro de índice como un error

Además, puede escribir mensajes personalizados en el registro de índices mediante la subrutina `_search_debug_log()` , como en el siguiente ejemplo:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Estos mensajes aparecen con la palabra `DEBUG` como prefijo y no se registran como errores.

Para mostrar el número de documentos procesados por la secuencia de comandos de filtrado como una línea de error en el registro de índice, puede utilizar la siguiente secuencia de comandos de terminación:

```
# Print the value of the document counter. 
print STDERR "Total docs: $main::doc_count\n"; 
# Or, using the log subroutine: 
_search_debug_log("Total docs: " . $main::doc_count);
```

Consulte [Variables globales](#global-variables)

### Sugerencias rápidas {#section_5790EA7ACAC046CBA01F759F88E2460F}

* A todas las variables globales se les agregará el área de nombres &quot;main::&quot;: `$main::doc_count = 0;`
* Todas las variables locales se declaran con &quot;my&quot;: `my $i = 0;`
* Las subrutinas se definen en la secuencia de comandos de inicialización. No necesitan un espacio de nombres &quot;main::&quot; explícito: `sub my_sub {` `...`

   `}`

* Pruebe `$main::search_content_type` antes de realizar cambios en un archivo. Las pruebas pueden ayudar a evitar realizar cambios sin cuidado en archivos binarios, como archivos SWF o archivos PDF:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* El `$main::search_content_type` es el encabezado Content-Type completo que su servidor entrega. A veces puede contener un tipo MIME simple, como &quot;text/html&quot;. O bien, puede contener un tipo MIME seguido de otra información, como la codificación del conjunto de caracteres del documento, como &quot;text/html; charset=iso-8859-1&quot;.
* Para cada tipo de documento no HTML, `$main::search_content_type` puede tomar varios valores. La prueba de cada valor en la secuencia de comandos se vuelve engorrosa. Por ejemplo, algunos documentos de Word tienen valores de tipo de contenido de &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; o &quot;application/x-msword&quot;. En estos casos, `$main::search_content_class` puede tomar los siguientes valores:

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* En el ejemplo, probar `$main::search_content_class` para &quot;word&quot; coincidiría con cualquiera de los tres valores posibles de tipo de contenido.
* Si no se imprime nada en STDOUT desde el script de filtrado, el documento se utiliza exactamente como se descargó. Es decir, si no necesita cambiar nada en un documento, no necesita copiar STDIN en STDOUT para ese documento.
* Si desea quitar todo el texto de un documento, imprima un archivo válido STDOUT. Por ejemplo, para eliminar todo el texto de un documento HTML, haga lo siguiente: `print "<html></html>";`

## Adición de una secuencia de comandos de terminación {#task_F0CFB412871642CFBC88132889C5B6F9}

La secuencia de comandos de terminación es una secuencia de comandos Perl que se ejecuta una vez después de indexar todos los documentos.

La secuencia de comandos de terminación se utiliza junto con una secuencia de comandos de filtrado, una secuencia de comandos de finalización y una secuencia de comandos de máscaras de URL.

Asegúrese de reconstruir el índice del sitio para que los resultados de la secuencia de comandos de inicialización sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Agregar una secuencia de comandos de finalización**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Termination Script]**.
1. (Opcional) En la página [!DNL Termination Script], en el campo [!DNL Test URL], introduzca la dirección URL de un documento en el sitio web.

   Haga clic en una opción de prueba para ver los cambios en el texto HTML sin procesar.

   Consulte la tabla de opciones de filtrado en **Añadir un script de filtrado**.

   Haga clic en **[!UICONTROL Test]** para realizar pruebas con los scripts de filtrado y las máscaras de URL.

   Al hacer clic en **[!UICONTROL Test]** no se actualiza ni se guarda la secuencia de comandos de terminación.
1. En el campo [!DNL Termination Script] , pegue la secuencia de comandos.
1. (Opcional) Haga clic en **[!UICONTROL Check Syntax]** para realizar una comprobación rápida de la sintaxis de la secuencia de comandos ejecutando las secuencias de comandos de inicialización, filtrado y finalización.

   **[!UICONTROL Check Syntax]** no actualiza ni guarda el script.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstruya el índice del sitio provisional si desea obtener una vista previa de los resultados.

   Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) En la página [!DNL Termination Script], realice una de las acciones siguientes:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del script de máscaras de URL {#concept_384F32EA18F84853A7BA99A04009330B}

Con el filtrado, puede cambiar el contenido de un documento web antes de que se indexa. Puede insertar etiquetas HTML, eliminar contenido irrelevante e incluso crear nuevos metadatos HTML basados en la URL, el tipo MIME y el contenido existente de un documento. La secuencia de comandos de máscaras de URL es una secuencia de comandos Perl que proporciona una potente gestión de cadenas y la flexibilidad de la coincidencia de expresiones regulares.

Para cambiar el contenido de los documentos que existen solamente en una parte específica del sitio web, puede especificar incluir máscaras de URL, excluir máscaras de URL, o ambas, para definir las páginas adecuadas.

Si desea cambiar solo los documentos de `"https://www.mysite.com/faqs/"`, puede utilizar el siguiente conjunto de máscaras:

```
include https://www.mysite.com/faqs/ 
exclude *
```

También puede utilizar la expresión regular en un script de máscara de URL como en el siguiente ejemplo:

```
include regexp ^https://www\.mysite\.com.*/faqs/.*$ 
exclude *
```

Consulte [Expresiones regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Las máscaras de URL con secuencias de comandos se tienen en cuenta en el orden en que se introdujeron en el campo [!DNL URL Masks]. Cuando la dirección URL de un documento coincide con una máscara, ese documento se incluye o excluye en función del tipo de máscara. Si la dirección URL de un documento no coincide con ninguna máscara de dirección URL, el documento se incluye únicamente si su tipo MIME es &quot;text/html&quot;. Se excluyen todos los demás tipos de MIME.

## Adición de un script de máscara de URL {#task_D18F2A496C1C45C997B5DA650AAF5D59}

Especifique las direcciones URL que incluyen máscaras y excluyan máscaras para cambiar el contenido de los documentos que solo existen en una parte específica del sitio web.

Antes de que los visitantes vean los efectos de la configuración de las máscaras de URL, reconstruya el índice del sitio.

**Adición de una secuencia de comandos de máscara de URL**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL URL Masks]**.
1. (Opcional) En la página [!DNL URL Masks], en el campo [!DNL Test URL], introduzca una dirección URL de un documento en el sitio web y, a continuación, haga clic en **[!UICONTROL Test]** para probar la dirección URL con las secuencias de comandos y máscaras de filtrado.

   Se descarga el documento de la URL de prueba, que se utiliza como entrada STDIN en el script de filtrado. A continuación, se ejecutan las secuencias de comandos de filtrado, inicialización y finalización. Si hay algún resultado STDOUT del script de filtrado, ese resultado se muestra en una nueva ventana del navegador.

   Al hacer clic en **[!UICONTROL Test]** no se actualiza ni se guarda el script.
1. En el campo [!DNL URL Masks], introduzca una máscara URL por línea.
1. (Opcional) Haga clic en **[!UICONTROL Check Syntax]** para realizar una comprobación de sintaxis rápida de las máscaras de URL ejecutando las secuencias de comandos de filtrado, inicialización y finalización.

   **[!UICONTROL Check Syntax]** no actualiza ni guarda el script.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstruya el índice del sitio provisional si desea obtener una vista previa de los resultados.

   Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) En la página [!DNL URL Masks], realice una de las acciones siguientes:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de los tipos de contenido en el filtro {#concept_E3EFF4A148EA4D21AFD0A5453A00427E}

Permite seleccionar los tipos de contenido que desea filtrar para esta cuenta.

El texto que se encuentra dentro de los tipos de contenido seleccionados se convierte a HTML y luego se procesa con la secuencia de comandos especificada en Secuencia de comandos de filtrado.

Consulte [Acerca del filtrado de secuencias de comandos](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

Los tipos de contenido que puede seleccionar son los siguientes:

* Documentos PDF
* Documentos de texto
* películas de Flash de Adobe
* Archivos de Microsoft Word
* Archivos de Microsoft Office (OpenXML)
* Archivos de Microsoft Excel
* Archivos de Microsoft PowerPoint
* Texto en archivos de música MP3

Antes de que los efectos de la configuración de los tipos de contenido o los cambios en la configuración sean visibles para los clientes, debe volver a generar el índice del sitio.

## Selección de los tipos de contenido filtrados {#task_C46081FA425A43EC8FDE6EA4A52A170A}

Seleccione los tipos de contenido que desea pasar a la secuencia de comandos especificada en Secuencia de comandos de filtrado.

Consulte [Acerca del filtrado de secuencias de comandos](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

**Seleccionar los tipos de contenido que se filtran**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Content Types]**.
1. En la página [!DNL Content Types], compruebe los tipos de contenido que desea pasar al script de filtro.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstruya el índice del sitio provisional si desea obtener una vista previa de los resultados.

   Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) En la página [!DNL Content Types], realice una de las acciones siguientes:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
