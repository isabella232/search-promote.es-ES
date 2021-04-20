---
description: Siempre que cambie su sitio web, puede ejecutar un script o programa solicitando que el robot de búsqueda ejecute un índice usando control remoto.
solution: Target
title: Acerca del control remoto para la indexación
topic: Index,Site search and merchandising
uuid: 20e230c6-5c1a-4bf4-bff3-b8236d14ab21
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 1%

---


# Acerca del control remoto para la indexación{#about-remote-control-for-indexing}

Siempre que cambie su sitio web, puede ejecutar un script o programa solicitando que el robot de búsqueda ejecute un índice usando control remoto.

## Uso del control remoto para indexar {#concept_C79B322190E84106A434E5C6D4A4118F}

La solicitud de indexación de control remoto suele proceder de un script o un programa que se encuentra en el servidor.

El robot realiza los mismos pasos de indexación que si se hubieran iniciado manualmente desde el menú [!DNL Index]. Para enviar una solicitud de control remoto, se configuran las cadenas de contraseña y respuesta necesarias.

## Cómo realizar una solicitud de control remoto {#section_42FAB2BAB25A4E24BEA69566C6D1C70F}

Para realizar una solicitud de control remoto, utilice los siguientes ejemplos de formato en función de la ubicación del centro de datos:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Ubicación del centro de datos </p> </th> 
   <th colname="col2" class="entry"> <p>Ejemplo </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Londres </p> </td> 
   <td colname="col2"> <p> <code> https://center.lon5.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>América del Norte </p> </td> 
   <td colname="col2"> <p> <code> https://center.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Singapur </p> </td> 
   <td colname="col2"> <p> <code> https://center.sin2.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

o

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Cadena y valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_a= sp99999999  </span> </p> </td> 
   <td colname="col2"> <p> Su número de cuenta. </p> <p>Puede encontrar su número de cuenta en <span class="uicontrol"> <b>Configuración</b> </span> &gt; <span class="uicontrol"> <b>Opciones de cuenta</b> </span> &gt; <span class="uicontrol"> <b>Configuración de cuenta</b> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_lines= N  </span> </p> </td> 
   <td colname="col2"> <p>Permite comprobar el estado de un rastreo de índice en ejecución. </p> <p> <span class="codeph">  N  </span> es un número entero positivo o  <span class="codeph"> todo  </span>. Si se trata de un valor numérico, las últimas líneas <span class="codeph"> N </span> del archivo de registro de índice correspondiente se incluyen en la respuesta JSON. </p> <p>Si el valor es <span class="codeph"> todo </span>, se devuelve el archivo completo. </p> <p>Si el valor es <span class="codeph"> 0 </span>, no se devuelve información de registro. Este valor es el predeterminado para una consulta de estado de índice en ejecución. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= op  </span> </p> </td> 
   <td colname="col2"> <p>Permite especificar una de las siguientes operaciones de indexación que desea ejecutar: </p> <p> 
     <ul id="ul_6CA190AC41694BC293FC7C6BABA629FE"> 
      <li id="li_EFC76E31D47E473F9A56B2EBA8A97CA1"> <span class="codeph"> full_index  </span> <p>El robot de búsqueda ejecuta un índice completo de su sitio web. </p> </li> 
      <li id="li_A9ACE21718804A21B3DA7B84AB6729D3"> <span class="codeph"> incremental_index  </span> <p>El robot de búsqueda ejecuta un índice incremental utilizando la configuración que se establece en <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Incremental Index</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
      <li id="li_722FE409AE454AD48ACE95C4CDC7A00B"> <span class="codeph"> vertical_index  </span> <p>El robot de búsqueda ejecuta una actualización vertical utilizando la configuración que se establece en <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Vertical Update</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> <p>Consulte <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Acerca de la actualización vertical</a>. </p> </li> 
      <li id="li_A40B513CE17043A4925CE3D4DE0B48A4"> <span class="codeph"> script_index  </span> <p>El robot de búsqueda ejecuta un índice incremental utilizando el archivo de texto especificado en <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Índice </b> </span> &gt; <span class="uicontrol"> <b>Configuración</b></span>. </p> </li> 
      <li id="li_A0BC7F1373B14393997BAB7690FD3EF7"> <span class="codeph"> full_staged_index  </span> <p>El robot de búsqueda ejecuta un índice de ensayo completo de su sitio web. </p> </li> 
      <li id="li_47753E358457443A95B384A278FACA83"> <span class="codeph"> incremental_staged_index  </span> <p>El robot de búsqueda ejecuta un índice escalonado incremental utilizando la configuración que se establece en <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Incremental Index</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
      <li id="li_C8B5F8F1208E438ABEFDF9129A6B14A3"> <span class="codeph"> vertical_staged_index  </span> <p>El robot de búsqueda ejecuta una actualización vertical escalonada utilizando la configuración establecida en <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Vertical Update</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
     </ul> </p> <p>Nota:  Para utilizar Actualizaciones verticales, es posible que deba activarlo en su cuenta por parte del representante de cuentas de Adobe o por parte de la asistencia técnica de Adobe. </p> <p>Consulte <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Acerca de la actualización vertical </a>. </p> <p>Puede anexar <span class="codeph"> _saved </span> a cualquiera de los valores <span class="codeph"> sp_operation </span> anteriores para que el robot de búsqueda intente utilizar contenido guardado. Por ejemplo, puede especificar lo siguiente: </p> <p> <code class="syntax html"> sp_operation=full_index_saved </code> </p> <p>o </p> <p> <code class="syntax html"> sp_operation=full_staged_index_saved </code> </p> <p>O bien, puede anexar <span class="codeph"> _status </span> a cualquiera de los valores <span class="codeph"> sp_operation </span> anteriores para solicitar un informe de estado para la operación actual o la más reciente. Por ejemplo, puede especificar lo siguiente: </p> <p> <code class="syntax html"> sp_operation=full_index_status </code> </p> <p>o </p> <p> <code class="syntax html"> sp_operation=full_staged_index_status </code> </p> <p>y los resultados se devuelven como un objeto JSON. Incluya <span class="codeph"> sp_lines=N </span> para incluir N líneas del archivo de registro asociado. Si N es negativo, se incluyen las últimas N líneas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= pushlive  </span> </p> </td> 
   <td colname="col2"> <p> Permite insertar de forma remota un índice escalonado. </p> <p>Se ignora cualquier intento de anexar <span class="codeph"> _saved </span> a la operación push. </p> <p>Cuando se ejecuta una operación <span class="codeph"> pushlive </span>, se devuelve al servidor una cadena de texto OK, Priority o Error response. Especifique estas cadenas de respuesta en la página <span class="wintitle"> Control remoto </span> . </p> <p>Consulte <a href="../c-about-index-menu/c-about-remote-control-for-indexing.md#task_57C296258404448DA7A5ADC9B7232391" format="dita" scope="local"> Configuración del control remoto para la indexación</a>. </p> <p>Si inserta en directo cuando no hay ningún índice de ensayo, no sucede nada y se devuelve la cadena de respuesta OK. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_password= xxxxxx  </span> </p> </td> 
   <td colname="col2"> <p>La contraseña del control remoto. </p> </td> 
  </tr> 
 </tbody> 
</table>

La búsqueda devuelve datos en forma de una respuesta HTTP adecuada. La respuesta completa está compuesta por un estado HTTP, encabezados de respuesta HTTP, una línea en blanco y la cadena de respuesta.

Por ejemplo, supongamos que realiza la siguiente solicitud de control remoto:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index
```

La siguiente es la respuesta del servidor:

```
Status: 200 OK 
Content-type: text/plain 
OK
```

O bien, suponga que realiza la siguiente solicitud de estado de control remoto:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status
```

La respuesta del servidor puede tener el siguiente aspecto:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:58:58-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "status": 1, 
    "message": "ok" 
}
```

Para obtener las diez primeras líneas del listado de registros asociado a esta operación de índice, junto con su estado, se utiliza la siguiente consulta:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=10
```

La respuesta del servidor:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:59:30-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "offset": 672, 
    "lines": [ 
        "07/25 16:40:07 PST   ======== Starting manual crawl of account sp99999999. ========", 
        "07/25 16:40:08 PST   Loading existing data", 
        "07/25 16:40:08 PST   Downloading entrypoint https://www.atomz.com/", 
        "07/25 16:40:08 PST   Robots.txt exclude mask: https://www.atomz.com/snap", 
        "07/25 16:40:08 PST   Exclude mask: regexp ^https://www.atomz.com/$", 
        "07/25 16:40:08 PST   Include mask: https://www.atomz.com/", 
        "07/25 16:40:08 PST   Downloading https://www.atomz.com/style.css", 
        "07/25 16:40:09 PST   Ignoring https://www.atomz.com/style.css, document type 'text/css'.", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/privacy.html", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/terms.html" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

Tenga en cuenta el valor `offset`. Este valor identifica la posición de desplazamiento del archivo en el archivo de registro en el que la lectura dejó de funcionar. Para leer las *siguientes* diez líneas del archivo, debe incluir, en este ejemplo, `&sp_offset=672` en la solicitud enviada al servidor.

Con `sp_offset`, puede desplazarse por un archivo de registro.

Para obtener las *last* diez líneas del registro, junto con el estado , especifique el recuento como un número negativo. Por ejemplo, especifique `sp_lines=` con un valor de `-10` como en el siguiente:

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=-10
```

La respuesta del servidor:

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T11:01:14-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "lines": [ 
        "07/25 16:40:20 PST   End Time: 07/25/2017 16:40:20 PST", 
        "07/25 16:40:20 PST   Elapsed Time: 13 seconds", 
        "07/25 16:40:20 PST   Pages Crawled: 3 pages", 
        "07/25 16:40:20 PST   Pages Indexed: 3 pages", 
        "07/25 16:40:20 PST   Words/Bytes Indexed: 2373 words/ 20618 bytes", 
        "07/25 16:40:20 PST   Errors: 0", 
        "07/25 16:40:20 PST   *** Index Summary ***", 
        "07/25 16:40:20 PST   Total Pages: 3", 
        "07/25 16:40:20 PST   --------------------------------------------------------------------", 
        "07/25 16:40:20 PST   ======== Finish manual crawl of account sp99999999: Done. ========" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

Tenga en cuenta que no hay ningún valor `offset` devuelto aquí, ya que esta operación ha finalizado al final del archivo y no hay más líneas que leer.

## Configuración del control remoto para indexar {#task_57C296258404448DA7A5ADC9B7232391}

Siempre que cambie su sitio web, puede usar Control remoto para ejecutar un script o programa desde su servidor, solicitando que el robot de búsqueda ejecute un índice.

**Para configurar el control remoto para la indexación**

1. En el menú del producto, haga clic en **[!UICONTROL Index]** > **[!UICONTROL Remote Control]**.
1. En la página [!DNL Remote Control], configure cada opción de campo de configuración para poder enviar una solicitud de indexación desde el servidor automáticamente para indexar el sitio web.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>Opción </p> </th> 
    <th colname="col2" class="entry"> <p>Descripción </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Contraseña de control remoto </p> </td> 
    <td colname="col2"> <p>Especifique la contraseña del control remoto. </p> <p> Las contraseñas distinguen entre mayúsculas y minúsculas, tienen al menos seis caracteres de longitud y deben incluir al menos una letra. Se recomienda incluir al menos un número. </p> <p>No use la contraseña de inicio de sesión de búsqueda/comercialización del sitio. </p> <p>La contraseña se utiliza en cada solicitud de control remoto. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Cadena de respuesta OK </p> </td> 
    <td colname="col2"> <p>Permite especificar una cadena de texto de respuesta OK si la operación de índice solicitada comienza correctamente. En estos casos, el robot de búsqueda devuelve la cadena de respuesta OK al servidor. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Cadena de respuesta de prioridad </p> </td> 
    <td colname="col2"> <p>Si hay otra operación de indexación en curso cuando se realiza la solicitud remota, el robot de búsqueda no puede realizar el índice solicitado. En estos casos, la cadena de texto Priority response se devuelve al servidor. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Cadena de respuesta de error </p> </td> 
    <td colname="col2"> <p>Permite especificar una cadena de texto de respuesta de error Si la contraseña es incorrecta o si se produce otro error. En estos casos, el robot de búsqueda devuelve la cadena de respuesta de error al servidor. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Changes]**.
