---
description: Utilice el menú Filtrado para utilizar secuencias de comandos que cambien el contenido de un documento web antes de indexarlo.
seo-description: Utilice el menú Filtrado para utilizar secuencias de comandos que cambien el contenido de un documento web antes de indexarlo.
seo-title: Acerca del menú Filtro
solution: Target
subtopic: Filtering
title: Acerca del menú Filtro
topic: Settings,Site search and merchandising
uuid: ebb08fa8-4e17-417d-868b-11fc2af9f284
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Acerca del menú Filtro{#about-the-filtering-menu}

Utilice el menú Filtrado para utilizar secuencias de comandos que cambien el contenido de un documento web antes de indexarlo.

## Acerca del filtrado de secuencias de comandos {#concept_E56B73D625854AB2A899EF2D56CFCB47}

Puede utilizar [!DNL Filtering Script] para cambiar el contenido de un documento Web antes de indizarlo.

Puede insertar etiquetas HTML, eliminar contenido irrelevante e incluso crear nuevos metadatos HTML basados en la URL, el tipo MIME y el contenido existente de un documento. La secuencia de comandos de filtrado es una secuencia de comandos Perl, que proporciona una potente gestión de cadenas y la flexibilidad de la coincidencia de expresiones regulares. La secuencia de comandos de filtrado se utiliza con una secuencia de comandos de inicialización, una secuencia de comandos de finalización, una secuencia de comandos de máscaras URL y una URL de prueba.

La secuencia de comandos de filtrado se ejecuta cada vez que se lee un documento del sitio web. La secuencia de comandos se ejecuta como un filtro estándar. En otras palabras, lee datos de STDIN, los transforma de alguna manera y escribe los resultados en STDOUT. Puede utilizar la secuencia de comandos de filtrado para imprimir mensajes de estado desde la secuencia de comandos de filtrado al registro de índice. Puede imprimir los mensajes en STDERR o a través de la `_search_debug_log()` subrutina.

Algunas opciones de diferencias GNU que puede usar mientras está en **[!UICONTROL Expert (diff)]** modo en la página Secuencia de comandos de filtrado por etapas son las siguientes:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opción diff GNU </p> </th> 
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
   <td colname="col1"> <p> <span class="codeph"> Líneas C </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida de contexto, mostrando líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> Omite los cambios en el caso; considere equivalentes las letras mayúsculas y minúsculas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
   <td colname="col2"> <p> Convierte los resultados en una salida similar a una secuencia de comandos de final, pero con cambios en el orden en que aparecen en el archivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> Produce diferencias en formato RCS; como <span class="codeph"> -f </span> excepto que cada comando especifica el número de líneas afectadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra tres líneas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -Líneas U </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, mostrando líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puede utilizar variables locales, variables globales o ambas en estas secuencias de comandos. Todas las variables globales llevan el prefijo &quot;main::&quot;. Cuando se inicia la secuencia de comandos de filtrado, su entorno contiene los siguientes identificadores de archivo estándar:

* STDIN: nada (devuelve EOF inmediatamente cuando se lee)
* STDOUT - reemplazo de HTML (si los datos se imprimen en STDOUT, se utiliza en lugar del documento original)
* STDERR: los datos impresos en STDERR se imprimen en el Registro de índice como un error

Además, puede escribir mensajes personalizados en el registro de índice mediante la `_search_debug_log()` subrutina, como en el ejemplo siguiente:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Estos mensajes aparecen con la palabra `DEBUG` como un prefijo y no se registran como errores.

El siguiente es un ejemplo de filtrado. Los campos de página `<title>` Web suelen comenzar por el nombre de la empresa. Aunque esta información es útil para la navegación del sitio, no es relevante para la búsqueda. Si los títulos de todas las páginas web de MegaCorp comienzan con una cadena común, como por ejemplo:

```
<title>MegaCorp -- meaningful title 
here</title>
```

Debe eliminar &quot; `MegaCorp --`&quot; desde el principio de cada título de documento y contar cada documento procesado con la secuencia de comandos de filtrado. Para ello, puede utilizar la siguiente secuencia de comandos:

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

Puede utilizar las siguientes variables en cualquier secuencia de comandos de filtrado:

| Variable | Descripción |
|--- |--- |
| `$main::search_crawl_type` | El valor de `$main::search_crawl_type` indica el tipo de operación de índice en curso.  Formulario desaprobado: `$main::ws_crawl_type` Las operaciones de índice y los valores asociados incluyen lo siguiente: <ul><li>Índice completo: Manual - `manual`</li><li>Índice completo: Programado - `auto`</li><li>Índice completo: Control remoto - `CGI`</li><li>Índice incremental: Manual - `manual-incremental`</li><li>Índice incremental: Programado - `auto-incremental` </li><li>Índice incremental: Control remoto - `CGI-incremental`</li><li>Índice con secuencias de comandos: Manual - `manual-indexlist.txt` </li><li>Índice con secuencias de comandos: Programado - `auto-indexlist.txt`</li><li>Índice con secuencias de comandos: Control remoto - `CGI-indexlist.txt`</li><li>Regenerar - `manual-upgrade`</li></ul> |
| `$main::search_clear_cache` | El valor indica si se solicitó la opción de indexación &quot;Borrar caché de índice&quot; para la operación de índice actual. Si se solicitó &quot;Borrar caché de índice&quot;, el valor de `$main::search_clear_cache` es &quot; `1`&quot;.  Forma obsoleta: `$main::ws_clear_cache` |
| `$main::search_fields` | El valor contiene una lista separada por tabuladores de los campos de metadatos definidos en la cuenta. De forma predeterminada, el valor es:   `url title desc keys target body alt date charset language` Formulario desaprobado: `$main::ws_fields` |
| `$main::search_collections` | El valor contiene una lista separada por tabuladores de las colecciones que se definen en la cuenta.  Forma obsoleta: `$main::ws_collections` |
| `$main::search_url` | El valor es la dirección URL completa del documento.  Forma obsoleta: `$main::ws_url` |
| `$main::search_content_type` | El valor es el tipo de contenido del documento tal como se obtiene de la etiqueta meta http-equiv. Un valor típico es &quot;text/html; charset=iso-8859-1&quot;.  Forma obsoleta: `$main::ws_content_type` |
| `$main::search_content_class` | El valor es la clase de contenido del documento, tal como se deriva del campo de tipo de contenido.  Forma obsoleta: `$main::ws_content_class` |
| `$main::search_syntax_check` | El valor refleja el uso del botón &quot;Comprobar sintaxis&quot;. Si se hace clic, el valor es 1 (uno); de lo contrario, su valor es 0 (cero).  Forma obsoleta: `$main::ws_syntax_check` |
| `$main::search_last_mod_date` | Si lo proporciona el servidor web, este valor contiene la representación Epoch (segundos transcurridos desde el 1 de enero de 1970) de la fecha de la última modificación del documento.  Puede dar formato a este valor mediante la llamada de biblioteca Perl localtime(). |

### Sugerencias rápidas {#section_89A5C16911744AF98E232DF608C6A1F5}

* Todas las variables globales llevan el prefijo &quot;main:&quot;: `$main::doc_count = 0;`
* Todas las variables locales se declaran con &quot;my&quot;: `my $i = 0;`
* Las subrutinas se definen en la secuencia de comandos de inicialización. No necesitan un espacio de nombres explícito &quot;main::&quot;: `sub my_sub {`  `...`

   `}`

* Pruebe el `$main::search_content_type` antes de realizar cambios en un archivo. La prueba puede ayudarle a evitar realizar cambios irresponsables en archivos binarios, como archivos SWF o archivos PDF:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* El `$main::search_content_type` es el encabezado Content-Type completo que su servidor entrega. A veces puede contener un tipo MIME simple, como &quot;text/html&quot;. O bien, puede contener un tipo MIME seguido de otra información, como la codificación del conjunto de caracteres del documento, como &quot;text/html; charset=iso-8859-1&quot;.
* Para cada tipo de documento que no sea HTML, `$main::search_content_type` puede tomar varios valores. La prueba de cada valor de la secuencia de comandos resulta engorrosa. Por ejemplo, algunos documentos de Word tienen valores de tipo de contenido de &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; o &quot;application/x-msword&quot;. En estos casos, `$main::search_content_class` puede tomar los siguientes valores:

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* En el ejemplo, la prueba `$main::search_content_class` de &quot;palabra&quot; coincidiría con cualquiera de los tres valores posibles de tipo de contenido.
* Si no se imprime nada en STDOUT desde la secuencia de comandos de filtrado, el documento se utiliza exactamente como se descargó. Es decir, si no necesita cambiar nada en un documento, no necesita copiar STDIN en STDOUT para ese documento.
* Si desea eliminar todo el texto de un documento, imprima un archivo STDOUT válido. Por ejemplo, para eliminar por completo todo el texto de un documento HTML, haga lo siguiente: `print "<html></html>";`

## Adición de un script de filtrado {#task_0AB84FD1133F47F9AA069A79BEA13A22}

La secuencia de comandos de filtrado es una secuencia de comandos Perl que se ejecuta para cada documento descargado del sitio web.

La secuencia de comandos de filtrado se utiliza junto con una secuencia de comandos de inicialización, una secuencia de comandos de finalización y una secuencia de comandos de máscaras URL.

Asegúrese de volver a generar el índice del sitio para que los resultados de la secuencia de comandos de filtrado sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

**Adición de una secuencia de comandos de filtrado**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Filtering Script]**.
1. (Opcional) En la [!DNL Filtering Script] página, en el [!DNL Test URL] campo, introduzca la dirección URL de un documento en el sitio web.

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
      <td colname="col1"> <p>Campo de la dirección URL de prueba </p> </td> 
      <td colname="col2"> <p>Permite introducir la dirección URL de un documento en el sitio web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Prueba </p> </td> 
      <td colname="col2"> <p>Prueba la dirección URL con las secuencias de comandos de filtrado y las máscaras URL. </p> <p>Se descarga el documento de la URL de prueba, que luego se utiliza como entrada STDIN en el script de filtrado. A continuación, se ejecutan las secuencias de comandos de inicialización, filtrado y finalización. Si hay algún resultado STDOUT del script de filtrado, ese resultado se muestra en una nueva ventana del explorador. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sólo prueba </p> </td> 
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
      <td colname="col1"> <p>Vídeo breve </p> </td> 
      <td colname="col2"> <p>Muestra únicamente las diferencias entre las vistas antes y después. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Experto (diff) </p> </td> 
      <td colname="col2"> <p>Muestra el resultado sin procesar del comando diff GNU que se utiliza para comparar los archivos, usando las opciones de línea de comandos suministradas. </p> </td> 
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
      <td colname="col2"> <p>Permite realizar una comprobación rápida de la sintaxis de la secuencia de comandos mediante la ejecución de las secuencias de comandos de inicialización, filtrado y finalización. No actualiza ni guarda la secuencia de comandos. </p> <p>Se imprimen todos los errores y advertencias del compilador de Perl y todos los resultados de STDERR. </p> <p>Antes de que los clientes vean los efectos de la secuencia de comandos, debe volver a generar el índice del sitio. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opciones de la línea de comandos GNU diff**

   Algunas opciones de diferencias GNU que puede usar mientras está en **[!UICONTROL Expert (diff)]** modo en la página Secuencia de comandos de filtrado por etapas son las siguientes:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción de línea de comandos GNU diff </p> </th> 
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
      <td colname="col1"> <p> <span class="codeph"> Líneas C </span> </p> </td> 
      <td colname="col2"> <p> Utiliza el formato de salida de contexto, mostrando líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
      <td colname="col2"> <p> Omite los cambios en el caso; considere equivalentes las letras mayúsculas y minúsculas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
      <td colname="col2"> <p> Convierte los resultados en una salida similar a una secuencia de comandos de final, pero con cambios en el orden en que aparecen en el archivo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
      <td colname="col2"> <p> Produce diferencias en formato RCS; como <span class="codeph"> -f </span> excepto que cada comando especifica el número de líneas afectadas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>-u </p> </td> 
      <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra tres líneas de contexto. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -Líneas U </span> </p> </td> 
      <td colname="col2"> <p> Utiliza el formato de salida unificado, mostrando líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic en **[!UICONTROL Test]** para realizar pruebas con las secuencias de comandos de filtrado y las máscaras URL.

   Al hacer clic **[!UICONTROL Test]** no se actualiza ni se guarda la secuencia de comandos de filtrado.
1. En el [!DNL Filtering Script] campo, pegue la secuencia de comandos.
1. (Opcional) Haga clic en **[!UICONTROL Check Syntax]** para realizar una comprobación rápida de la sintaxis de la secuencia de comandos mediante la ejecución de las secuencias de comandos de filtrado, inicialización y finalización.

   **[!UICONTROL Check Syntax]** no actualiza ni guarda la secuencia de comandos.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Si desea obtener una vista previa de los resultados, vuelva a generar el índice del sitio escalonado.

   Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.
1. (Opcional) En la [!DNL Filtering Script] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del script de inicialización {#concept_048B4C8BC9F74BE8BB6162C490C201A3}

Puede utilizar [!DNL Initialization Script] para cambiar el contenido de un documento Web antes de indizarlo.

Puede insertar etiquetas HTML, eliminar contenido irrelevante e incluso crear nuevos metadatos HTML basados en la URL, el tipo MIME y el contenido existente de un documento. La secuencia de comandos de inicialización es una secuencia de comandos Perl, que proporciona una potente gestión de cadenas y la flexibilidad de la coincidencia de expresiones regulares. La secuencia de comandos de inicialización se utiliza con una secuencia de comandos de filtrado, una secuencia de comandos de finalización, una secuencia de comandos de máscaras URL y una URL de prueba.

La secuencia de comandos de inicialización se ejecuta una vez antes de que comience la indexación. Utilice esta secuencia de comandos para inicializar las variables y subrutinas globales que utilice el script de filtrado. Puede utilizar la secuencia de comandos de inicialización para imprimir mensajes de estado desde la secuencia de comandos de filtrado al registro de índice. Puede imprimir los mensajes en STDERR o a través de la `_search_debug_log()` subrutina.

Algunas opciones de diferencias GNU que puede usar mientras está en **[!UICONTROL Expert (diff)]** modo en la página Secuencia de comandos de inicialización escalonada incluyen lo siguiente:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opción diff GNU </p> </th> 
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
   <td colname="col1"> <p> <span class="codeph"> Líneas C </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida de contexto, mostrando líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> Omite los cambios en el caso; considere equivalentes las letras mayúsculas y minúsculas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
   <td colname="col2"> <p> Convierte los resultados en una salida similar a una secuencia de comandos de final, pero con cambios en el orden en que aparecen en el archivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> Produce diferencias en formato RCS; como <span class="codeph"> -f </span> excepto que cada comando especifica el número de líneas afectadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra tres líneas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -Líneas U </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, mostrando líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puede utilizar variables locales, variables globales o ambas en estas secuencias de comandos. Todas las variables globales llevan el prefijo &quot;main::&quot;. Cuando se inicia la secuencia de comandos de inicialización, su entorno contiene los siguientes identificadores de archivo estándar:

* STDIN: nada (devuelve EOF inmediatamente cuando se lee)
* STDOUT - nada (si los datos se imprimen en STDOUT, se descartan)
* STDERR: los datos impresos en STDERR se imprimen en el Registro de índice como un error

Además, puede escribir mensajes personalizados en el registro de índice mediante la `_search_debug_log()` subrutina, como en el ejemplo siguiente:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Estos mensajes aparecen con la palabra `DEBUG` como un prefijo y no se registran como errores.

A continuación se muestra un ejemplo de secuencia de comandos de inicialización:

```
# My subroutine to do something. 
sub my_sub_for_the_filtering_script { 
    my ($param1, $param2) = @_; 
    ... 
} 
 
# Initialize the document counter. 
$main::doc_count = 0;
```

Consulte Variables [globales](#global-variables)

### Sugerencias rápidas {#section_A2CC0302CAF14135BF8EF6171FB184F1}

* Todas las variables globales llevan el prefijo &quot;main:&quot;: `$main::doc_count = 0;`
* Todas las variables locales se declaran con &quot;my&quot;: `my $i = 0;`
* Las subrutinas se definen en la secuencia de comandos de inicialización. No necesitan un espacio de nombres explícito &quot;main::&quot;: `sub my_sub {`  `...`

   `}`

* Pruebe el `$main::search_content_type` antes de realizar cambios en un archivo. La prueba puede ayudarle a evitar realizar cambios irresponsables en archivos binarios, como archivos SWF o archivos PDF:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* El `$main::search_content_type` es el encabezado Content-Type completo que su servidor entrega. A veces puede contener un tipo MIME simple, como &quot;text/html&quot;. O bien, puede contener un tipo MIME seguido de otra información, como la codificación del conjunto de caracteres del documento, como &quot;text/html; charset=iso-8859-1&quot;.
* Para cada tipo de documento que no sea HTML, `$main::search_content_type` puede tomar varios valores. La prueba de cada valor de la secuencia de comandos resulta engorrosa. Por ejemplo, algunos documentos de Word tienen valores de tipo de contenido de &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; o &quot;application/x-msword&quot;. En estos casos, `$main::search_content_class` puede tomar los siguientes valores:

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* En el ejemplo, la prueba `$main::search_content_class` de &quot;palabra&quot; coincidiría con cualquiera de los tres valores posibles de tipo de contenido.
* Si no se imprime nada en STDOUT desde la secuencia de comandos de filtrado, el documento se utiliza exactamente como se descargó. Es decir, si no necesita cambiar nada en un documento, no necesita copiar STDIN en STDOUT para ese documento.
* Si desea eliminar todo el texto de un documento, imprima un archivo STDOUT válido. Por ejemplo, para eliminar por completo todo el texto de un documento HTML, haga lo siguiente: `print "<html></html>";`

## Adición de una secuencia de comandos de inicialización {#task_5A03B8D0C46E4674B7CE88203515803B}

La secuencia de comandos de inicialización es una secuencia de comandos Perl que se ejecuta una vez antes de indizar cualquier documento.

La secuencia de comandos de inicialización se utiliza junto con una secuencia de comandos de filtrado, una secuencia de comandos de finalización y una secuencia de comandos de máscaras URL.

Asegúrese de volver a generar el índice del sitio para que los clientes puedan ver los resultados de la secuencia de comandos de inicialización.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

**Adición de una secuencia de comandos de inicialización**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Initialization Script]**.
1. (Opcional) En la [!DNL Initialization Script] página, en el [!DNL Test URL] campo, introduzca la dirección URL de un documento en el sitio web.

   Haga clic en una opción de prueba para ver los cambios en el texto HTML sin procesar.

   Consulte la tabla de opciones de filtrado en **Adición de un script** de filtrado.

   Haga clic en **[!UICONTROL Test]** para realizar pruebas con las secuencias de comandos de filtrado y las máscaras URL.

   Al hacer clic **[!UICONTROL Test]** no se actualiza ni se guarda la secuencia de comandos de inicialización.
1. En el [!DNL Initialization Script] campo, pegue la secuencia de comandos.
1. (Opcional) Haga clic en **[!UICONTROL Check Syntax]** para realizar una comprobación rápida de la sintaxis de la secuencia de comandos mediante la ejecución de las secuencias de comandos de filtrado, inicialización y finalización.

   **[!UICONTROL Check Syntax]** no actualiza ni guarda la secuencia de comandos.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Si desea obtener una vista previa de los resultados, vuelva a generar el índice del sitio escalonado.

   Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.
1. (Opcional) En la [!DNL Initialization Script] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de la secuencia de comandos de finalización {#concept_AAD6B3B0E7124874AD0947096FC42F47}

Puede utilizar [!DNL Termination Script] para cambiar el contenido de un documento Web antes de indizarlo.

Puede insertar etiquetas HTML, eliminar contenido irrelevante e incluso crear nuevos metadatos HTML basados en la URL, el tipo MIME y el contenido existente de un documento. La secuencia de comandos de inicialización es una secuencia de comandos Perl, que proporciona una potente gestión de cadenas y la flexibilidad de la coincidencia de expresiones regulares. La secuencia de comandos de finalización se utiliza con una secuencia de comandos de inicialización, una secuencia de comandos de filtrado, una secuencia de comandos de finalización, una secuencia de comandos de máscaras URL y una URL de prueba.

La secuencia de comandos de finalización se ejecuta una vez que se indizan todos los documentos. Puede utilizar la secuencia de comandos de finalización para imprimir mensajes de estado desde la secuencia de comandos de filtrado al registro de índice. Puede imprimir los mensajes en STDERR o a través de la `_search_debug_log()` subrutina.

Algunas opciones de línea de comandos GNU diff que puede utilizar mientras está en **[!UICONTROL Expert (diff)]** modo en la página Secuencia de comandos de terminación en etapas son las siguientes:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Opción de línea de comandos GNU diff </p> </th> 
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
   <td colname="col1"> <p> <span class="codeph"> Líneas C </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida de contexto, mostrando líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> Omite los cambios en el caso; considere equivalentes las letras mayúsculas y minúsculas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f </span> </p> </td> 
   <td colname="col2"> <p> Convierte los resultados en una salida similar a una secuencia de comandos de final, pero con cambios en el orden en que aparecen en el archivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> Produce diferencias en formato RCS; como <span class="codeph"> -f </span> excepto que cada comando especifica el número de líneas afectadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, que muestra tres líneas de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -Líneas U </span> </p> </td> 
   <td colname="col2"> <p> Utiliza el formato de salida unificado, mostrando líneas (un entero) de contexto o tres si no se dan líneas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puede utilizar variables locales, variables globales o ambas en estas secuencias de comandos. Todas las variables globales llevan el prefijo &quot;main::&quot;. Cuando se inicia la secuencia de comandos de finalización, su entorno contiene los siguientes identificadores de archivo estándar:

* STDIN: nada (devuelve EOF inmediatamente cuando se lee)
* STDOUT - nada (si los datos se imprimen en STDOUT, se descartan)
* STDERR: los datos impresos en STDERR se imprimen en el registro de índice como error

Además, puede escribir mensajes personalizados en el registro de índice mediante la `_search_debug_log()` subrutina, como en el ejemplo siguiente:

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Estos mensajes aparecen con la palabra `DEBUG` como un prefijo y no se registran como errores.

Para mostrar el número de documentos procesados por la secuencia de comandos de filtrado como una línea de error en el registro de índice, puede utilizar la siguiente secuencia de comandos de finalización:

```
# Print the value of the document counter. 
print STDERR "Total docs: $main::doc_count\n"; 
# Or, using the log subroutine: 
_search_debug_log("Total docs: " . $main::doc_count);
```

Consulte Variables [globales](#global-variables)

### Sugerencias rápidas {#section_5790EA7ACAC046CBA01F759F88E2460F}

* Todas las variables globales llevan el prefijo &quot;main:&quot;: `$main::doc_count = 0;`
* Todas las variables locales se declaran con &quot;my&quot;: `my $i = 0;`
* Las subrutinas se definen en la secuencia de comandos de inicialización. No necesitan un espacio de nombres explícito &quot;main::&quot;: `sub my_sub {`  `...`

   `}`

* Pruebe el `$main::search_content_type` antes de realizar cambios en un archivo. La prueba puede ayudarle a evitar realizar cambios irresponsables en archivos binarios, como archivos SWF o archivos PDF:

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* El `$main::search_content_type` es el encabezado Content-Type completo que su servidor entrega. A veces puede contener un tipo MIME simple, como &quot;text/html&quot;. O bien, puede contener un tipo MIME seguido de otra información, como la codificación del conjunto de caracteres del documento, como &quot;text/html; charset=iso-8859-1&quot;.
* Para cada tipo de documento que no sea HTML, `$main::search_content_type` puede tomar varios valores. La prueba de cada valor de la secuencia de comandos resulta engorrosa. Por ejemplo, algunos documentos de Word tienen valores de tipo de contenido de &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; o &quot;application/x-msword&quot;. En estos casos, `$main::search_content_class` puede tomar los siguientes valores:

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* En el ejemplo, la prueba `$main::search_content_class` de &quot;palabra&quot; coincidiría con cualquiera de los tres valores posibles de tipo de contenido.
* Si no se imprime nada en STDOUT desde la secuencia de comandos de filtrado, el documento se utiliza exactamente como se descargó. Es decir, si no necesita cambiar nada en un documento, no necesita copiar STDIN en STDOUT para ese documento.
* Si desea eliminar todo el texto de un documento, imprima un archivo STDOUT válido. Por ejemplo, para eliminar por completo todo el texto de un documento HTML, haga lo siguiente: `print "<html></html>";`

## Adición de una secuencia de comandos de finalización {#task_F0CFB412871642CFBC88132889C5B6F9}

La secuencia de comandos de finalización es una secuencia de comandos Perl que se ejecuta una vez que se indizan todos los documentos.

La secuencia de comandos de finalización se utiliza junto con una secuencia de comandos de filtrado, una secuencia de comandos de finalización y una secuencia de comandos de máscaras URL.

Asegúrese de volver a generar el índice del sitio para que los clientes puedan ver los resultados de la secuencia de comandos de inicialización.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

**Para agregar una secuencia de comandos de finalización**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Termination Script]**.
1. (Opcional) En la [!DNL Termination Script] página, en el [!DNL Test URL] campo, introduzca la dirección URL de un documento en el sitio web.

   Haga clic en una opción de prueba para ver los cambios en el texto HTML sin procesar.

   Consulte la tabla de opciones de filtrado en **Adición de un script** de filtrado.

   Haga clic en **[!UICONTROL Test]** para realizar pruebas con las secuencias de comandos de filtrado y las máscaras URL.

   Al hacer clic **[!UICONTROL Test]** no se actualiza ni se guarda la secuencia de comandos de finalización.
1. En el [!DNL Termination Script] campo, pegue la secuencia de comandos.
1. (Opcional) Haga clic en **[!UICONTROL Check Syntax]** para realizar una comprobación rápida de la sintaxis de la secuencia de comandos mediante la ejecución de las secuencias de comandos de inicialización, filtrado y finalización.

   **[!UICONTROL Check Syntax]** no actualiza ni guarda la secuencia de comandos.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Si desea obtener una vista previa de los resultados, vuelva a generar el índice del sitio escalonado.

   Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.
1. (Opcional) En la [!DNL Termination Script] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del script de máscaras URL {#concept_384F32EA18F84853A7BA99A04009330B}

Con el filtrado, puede cambiar el contenido de un documento web antes de indexarlo. Puede insertar etiquetas HTML, eliminar contenido irrelevante e incluso crear nuevos metadatos HTML basados en la URL, el tipo MIME y el contenido existente de un documento. La secuencia de comandos de máscaras URL es una secuencia de comandos Perl que proporciona una potente gestión de cadenas y la flexibilidad de la coincidencia de expresiones regulares.

Para cambiar el contenido de los documentos que solo existen en una parte específica del sitio web, puede especificar incluir máscaras URL, excluir máscaras URL o ambas, para definir las páginas adecuadas.

Si desea cambiar solo los documentos de `"https://www.mysite.com/faqs/"`, puede utilizar el siguiente conjunto de máscaras:

```
include https://www.mysite.com/faqs/ 
exclude *
```

También puede utilizar la expresión regular en una secuencia de comandos de máscara URL, como en el ejemplo siguiente:

```
include regexp ^https://www\.mysite\.com.*/faqs/.*$ 
exclude *
```

Consulte Expresiones [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Las máscaras URL con secuencias de comandos se consideran en el orden en que se introdujeron en el [!DNL URL Masks] campo. Cuando una dirección URL de documento coincide con una máscara, ese documento se incluye o excluye en función del tipo de máscara. Si la dirección URL de un documento no coincide con ninguna máscara de dirección URL, el documento solo se incluye si su tipo MIME es &quot;text/html&quot;. Se excluyen todos los demás tipos MIME.

## Adición de una secuencia de comandos de máscara URL {#task_D18F2A496C1C45C997B5DA650AAF5D59}

Especifique la URL, que incluye máscaras y que excluye máscaras para cambiar el contenido de los documentos que solo existen en una parte específica del sitio web.

Antes de que los visitantes vean los efectos de la configuración de las máscaras de URL, vuelva a crear el índice del sitio.

**Adición de una secuencia de comandos de máscara URL**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL URL Masks]**.
1. (Opcional) En la [!DNL URL Masks] página, en el [!DNL Test URL] campo, introduzca una URL de un documento en el sitio web y, a continuación, haga clic en **[!UICONTROL Test]** para probar la URL con las secuencias de comandos y máscaras de filtrado.

   Se descarga el documento de la URL de prueba, que se utiliza como entrada STDIN en el script de filtrado. A continuación, se ejecutan las secuencias de comandos de filtrado, inicialización y finalización. Si hay algún resultado STDOUT del script de filtrado, ese resultado se muestra en una nueva ventana del explorador.

   Al hacer clic **[!UICONTROL Test]** no se actualiza ni se guarda la secuencia de comandos.
1. En el [!DNL URL Masks] campo, introduzca una máscara URL por línea.
1. (Opcional) Haga clic en **[!UICONTROL Check Syntax]** para realizar una comprobación rápida de la sintaxis de las máscaras URL mediante la ejecución de las secuencias de comandos de filtrado, inicialización y finalización.

   **[!UICONTROL Check Syntax]** no actualiza ni guarda la secuencia de comandos.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Si desea obtener una vista previa de los resultados, vuelva a generar el índice del sitio escalonado.

   Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.
1. (Opcional) En la [!DNL URL Masks] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de los tipos de contenido en el filtrado {#concept_E3EFF4A148EA4D21AFD0A5453A00427E}

Permite seleccionar los tipos de contenido que desea filtrar para esta cuenta.

El texto que se encuentra dentro de los tipos de contenido seleccionados se convierte a HTML y, a continuación, se procesa con la secuencia de comandos especificada en Filtrar secuencias de comandos.

Consulte [Acerca del filtrado de secuencias de comandos](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

Los tipos de contenido que puede seleccionar incluyen lo siguiente:

* Documentos PDF
* Documentos de texto
* Películas Adobe Flash
* Archivos de Microsoft Word
* Archivos de Microsoft Office (OpenXML)
* Archivos de Microsoft Excel
* Archivos de Microsoft Powerpoint
* Texto en archivos de música MP3

Antes de que los efectos de la configuración de Tipos de contenido o los cambios en la configuración sean visibles para los clientes, debe volver a generar el índice del sitio.

## Selección de los tipos de contenido que se filtran {#task_C46081FA425A43EC8FDE6EA4A52A170A}

Seleccione los tipos de contenido que desea pasar a la secuencia de comandos especificada en Filtro de secuencias de comandos.

Consulte [Acerca del filtrado de secuencias de comandos](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

**Seleccionar los tipos de contenido que se filtran**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Content Types]**.
1. En la [!DNL Content Types] página, compruebe los tipos de contenido que desea pasar al script de filtro.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Si desea obtener una vista previa de los resultados, vuelva a generar el índice del sitio escalonado.

   Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.
1. (Opcional) En la [!DNL Content Types] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
