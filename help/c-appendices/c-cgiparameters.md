---
description: 'null'
seo-description: 'null'
seo-title: Parámetros de CGI
solution: Target
title: Parámetros de CGI
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: 7b883870bb16284d8070a21547cdb62cc79d7632
workflow-type: tm+mt
source-wordcount: '5490'
ht-degree: 1%

---


# Parámetros de CGI{#cgi-parameters}

## Parámetros de CGI {#concept_F395999090FE4926B38BC73D5E612800}

## Buscar parámetros CGI {#reference_DA27A8B0728246DA94994885E1353890}

Se proporciona el código de formulario de búsqueda que puede copiar y pegar en el HTML del sitio ( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**).

Consulte [Copia del código HTML del formulario de búsqueda en el...](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

También puede definir los parámetros que aparecen en el propio formulario de búsqueda o en una secuencia de comandos. Además de los parámetros que se enumeran a continuación, también puede utilizar los parámetros de búsqueda back-end para controlar la búsqueda.

Consulte Parámetros [CGI de búsqueda](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)back-end.

Las solicitudes de búsqueda constan de una dirección URL base. La dirección URL base indica qué cuenta está buscando el cliente y un conjunto de parámetros CGI (pares clave-valor) que indican cómo devolver los resultados de búsqueda deseados para la cuenta asociada.

La dirección URL base está asociada a una cuenta específica y a un entorno de ensayo o activo. Puede solicitar varios alias para la URL base desde el administrador de cuentas. Por ejemplo, una compañía llamada Megacorp puede tener dos direcciones URL base asociadas con su cuenta: `https://search.megacorp.com` y `https://stage.megacorp.com`. La dirección URL anterior busca en su índice activo y la última URL busca en su índice escalonado.

Se admiten tres formatos de parámetros CGI. De forma predeterminada, su cuenta está configurada para separar parámetros CGI con un punto y coma, como en el ejemplo siguiente:

`https://search.megacorp.com?q=shoes;page=2`

Si lo prefiere, puede hacer que el administrador de cuentas configure su cuenta para que utilice ampersands a fin de separar los parámetros CGI como en el siguiente ejemplo:

`https://search.megacorp.com?q=shoes&page=2`

También se admite un tercer formato, denominado formato SEO, en el que se utiliza una barra diagonal `/` en lugar del separador y un signo igual al del siguiente ejemplo:

`https://search.megacorp.com/q/shoes/page/2`

Cada vez que se utiliza el formato SEO para enviar una solicitud, todos los vínculos de salida se devuelven en el mismo formato.

| Parámetro de búsqueda guiada | Ejemplo | Descripción |
|--- |--- |--- |
| q | `q=string` | Especifica la cadena de consulta para la búsqueda. Este parámetro se asigna al parámetro de búsqueda del `sp_q` servidor.  Consulte Parámetros [CGI de búsqueda](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)back-end. |
| q# | `q#=string` | La faceta (búsqueda dentro de un campo determinado) se realiza mediante los parámetros numerados q y x.  El parámetro q define el término que está buscando en la faceta como se indica en el parámetro x numerado correspondiente.<br>Por ejemplo, si tiene dos facetas con nombres de tamaño y color, puede tener algo como q1=small;x1=size;q2=red;x2=color.  Este parámetro se asigna a los parámetros de búsqueda del `sp_q_exact_#` servidor.  <br>Consulte Parámetros [CGI de búsqueda](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)back-end. |
| x# | `q#=string` | La faceta (búsqueda dentro de un campo determinado) se realiza mediante los parámetros numerados q y x.  El parámetro q define el término que está buscando en la faceta como se indica en el parámetro x numerado correspondiente. <br>Por ejemplo, si tiene dos facetas con nombres de tamaño y color, puede tener algo como q1=small;x1=size;q2=red;x2=color.  Este parámetro se asigna a los parámetros de búsqueda del `sp_x_#` servidor.  <br>Consulte Parámetros [CGI de búsqueda](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)back-end. |
| colección | `collection=string` | Especifica la colección que se usará para la búsqueda.  Este parámetro se asigna al parámetro de búsqueda del `sp_k` servidor.  Consulte Parámetros [CGI de búsqueda](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)back-end. |
| count | `count=number` | Especifica el recuento total de resultados que se muestran.  El valor predeterminado se define en [!UICONTROL Settings ] > [!UICONTROL Searching ] > [!UICONTROL Searches ]. .  Este parámetro se asigna al parámetro de búsqueda del `sp_c` servidor.  Consulte Parámetros [CGI de búsqueda](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)back-end. |
| página | `page=number` | Especifica la página de resultados que se devuelven. |
| clasificación | `rank=field` | Especifica el campo de clasificación que se usará para la clasificación estática.  El campo debe ser un campo de tipo Clasificación con relevancia buena a 0.  Este parámetro se asigna al parámetro `sp_sr` back-end.  Consulte Parámetros [CGI de búsqueda](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)back-end. |
| ordenar | `sort=number` | Especifica el orden.<br>&quot;0&quot; es el valor predeterminado y ordena por puntuación de relevancia; &quot;1&quot; se ordenará por fecha; &quot;-1&quot; no se ordena.  Los usuarios pueden especificar un nombre de campo para el valor del `sp_s` parámetro.  Por ejemplo, `sp_s=title` ordena los resultados según los valores contenidos en el campo de título. Cuando se utiliza un nombre de campo para el valor de un ` sp_s ` parámetro, los resultados se ordenan por ese campo y luego se subordenan por relevancia.  To enable this feature, click [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. En la página Definiciones, haga clic [!UICONTROL Add New Field ] o haga clic en [!UICONTROL Edit ] el nombre de un campo concreto. En la lista [!UICONTROL Sorting ] desplegable, seleccione [!UICONTROL Ascending ] o [!UICONTROL Descending ]. Este parámetro se asigna al parámetro de búsqueda del `sp_s` servidor. <br>Consulte Parámetros [CGI de búsqueda]back-end.(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |

## Parámetros CGI de búsqueda back-end {#reference_582E85C3886740C98FE88CA9DF7918E8}

Normalmente, los clientes interactúan con una capa de presentación denominada Búsqueda guiada. Sin embargo, teóricamente es posible omitir la capa Búsqueda guiada e interactuar con la búsqueda básica del servidor directamente utilizando los parámetros CGI que se describen en esta página.

Puede seleccionar parámetros CGI de búsqueda back-end en la tabla siguiente:
<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>Compatibilidad con una sola consulta </p> </th> 
   <th colname="col03" class="entry"> <p>Compatibilidad con múltiples consultas </p> </th> 
   <th colname="col3" class="entry"> <p>Ejemplos </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>sp_a </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_a= cadena </span> </p> </td> 
   <td colname="col4"> <p>Especifica la cadena de número de cuenta. Este parámetro es obligatorio y debe ser una cadena de número de cuenta válida. Puede encontrar la cadena del número de cuenta en <span class="uicontrol"> Configuración </span> &gt; Opciones de cuenta <span class="uicontrol"> &gt; </span> Configuración de la cuenta <span class="uicontrol"> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_advanced= 0 o 1 </span> </p> </td> 
   <td colname="col4"> <p>Si <span class="codeph"> sp_advanced=1 </span> se envía con una consulta, para el formulario de búsqueda se utiliza todo el código entre la etiqueta <span class="codeph"> &lt;search-if-advanced&gt; </span> y la etiqueta <span class="codeph"> &lt;/search-if-advanced&gt; </span> de la plantilla de búsqueda. Se ignora todo el código entre la etiqueta <span class="codeph"> &lt;search-if-not-advanced&gt; </span> y la etiqueta <span class="codeph"> &lt;/search-if-not-advanced&gt; </span> . Si se envía <span class="codeph"> sp_advanced=0 </span> (o cualquier otro valor), se ignora el bloque de plantilla &lt;search-if-advanced&gt; y se utiliza el bloque de plantilla &lt;search-if-not-advanced&gt;. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_c= número </span> </p> </td> 
   <td colname="col4"> <p>Especifica el recuento total de resultados que se van a mostrar. El valor predeterminado es 10. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>Recopila información contextual para el campo dado. La información recopilada se muestra en los resultados de la búsqueda mediante la etiqueta de plantilla <span class="codeph"> &lt;search-context&gt; </span> . El valor predeterminado es <span class="codeph">body </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d= type </span> </p> </td> 
   <td colname="col4"> <p>Especifica el tipo de búsqueda de intervalo de fechas que se va a realizar. Los valores posibles para el tipo son cualquiera, lo que significa que no se debe realizar una búsqueda de intervalo de fechas, personalizada, lo que indica que se debe utilizar el valor de <span class="codeph"> sp_date_range </span> para determinar las fechas de búsqueda y específico, lo que indica que los valores en <span class="codeph"> sp_inicio_day </span>, <span class="codeph"> sp_inicio_month </span>, <span class="codeph"> sp_inicio_year </span>, <span class="codeph"> sp_end_day </span><span class="codeph"> </span><span class="codeph"> </span> , Flash sp_end_year_month y s. Se utiliza para determinar el intervalo de fechas que se va a buscar. <span class="codeph"> sp_d </span> sólo es necesario si el formulario de búsqueda contiene la opción de buscar por un intervalo personalizado (por medio de <span class="codeph"> sp_date_range </span>) o por un inicio y un intervalo de fechas de finalización específicos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d_#= type </span> </p> </td> 
   <td colname="col4"> <p>Especifica el tipo de búsqueda de intervalo de fechas para la consulta <span class="codeph"> sp_q_# </span> correspondiente. El "#" se sustituye por un número entre 1 y 16 (por ejemplo, <span class="codeph"> sp_d_8 </span>, se aplica a la consulta numerada <span class="codeph"> sp_q_8 </span>). </p> <p>Puede establecer <span class="codeph"> el tipo </span> en cualquiera, lo que significa que no debe realizar una búsqueda de intervalo de fechas, personalizada, lo que indica que el valor de <span class="codeph"> sp_date_range_# </span> se utiliza para determinar las fechas de búsqueda y específicas, lo que indica que los valores en <span class="codeph"> sp_q_min_day_# </span>, <span class="codeph"> sp_q_min_month_# </span>, <span class="codeph"> sp_q_min_year_# </span><span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span> , sp_q_max_day_# , sp_q_max_month_# , y sp__max_year_#  deben utilizarse para determinar el intervalo de fechas. El uso de <span class="codeph"> sp_d_# </span> sólo es necesario si el formulario de búsqueda contiene la opción de buscar por un intervalo personalizado (mediante <span class="codeph"> sp_date_range_# </span>) o por un inicio y un intervalo de fechas de finalización específicos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica un intervalo de fechas predefinido para aplicar a la búsqueda. Los valores buenos o iguales a cero especifican el número de días que se buscarán antes de hoy — por ejemplo, un valor de "0" especifica "hoy", un valor de "1" especifica "hoy y ayer", un valor de "30" especifica "en los últimos 30 días", y así sucesivamente. </p> <p>Los valores por debajo de cero especifican un intervalo personalizado de la siguiente manera: </p> <p>-1 = "Ninguno", lo mismo que especificar sin intervalo de fechas. </p> <p>-2 = "Esta semana", que busca de domingo a sábado de la semana actual. </p> <p>-3 = "Última semana", que busca de domingo a sábado de la semana anterior a la semana actual. </p> <p>-4 = "Este mes", que busca fechas dentro del mes actual. </p> <p>-5 = "Último mes", que busca fechas dentro del mes anterior al mes actual. </p> <p>-6 = "Este año", que busca fechas dentro del año actual. </p> <p>-7 = "Último año", que busca fechas dentro del año anterior al año en curso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica un intervalo de fechas predefinido para aplicar a la consulta <span class="codeph"> sp_q_# </span> correspondiente. El "#" se sustituye por un número entre 1 y 16 (por ejemplo, <span class="codeph"> sp_date_range_8 </span>, se aplica a la consulta numerada <span class="codeph"> sp_q_8 </span>). </p> <p>Los valores buenos o iguales a cero especifican el número de días de búsqueda anteriores a hoy. Por ejemplo, un valor de 0 especifica hoy; un valor de 1 especifica hoy y ayer; un valor de 30 especifica en los últimos 30 días, y así sucesivamente. </p> <p>Los valores por debajo de cero especifican un intervalo personalizado de la siguiente manera: </p> <p>-1 = "Ninguno", lo mismo que especificar sin intervalo de fechas. </p> <p>-2 = "Esta semana", que busca de domingo a sábado de la semana actual. </p> <p>-3 = "Última semana", que busca de domingo a sábado de la semana anterior a la semana actual. </p> <p>-4 = "Este mes", que busca fechas dentro del mes actual. </p> <p>-5 = "Último mes", que busca fechas dentro del mes anterior al mes actual. </p> <p>-6 = "Este año", que busca fechas dentro del año actual. </p> <p>-7 = "Último año", que busca fechas dentro del año anterior al año en curso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica un solo campo en el que se desduplicarán los resultados de la búsqueda. Todos los resultados de duplicado de ese campo se eliminan de los resultados de búsqueda. Por ejemplo, si para <span class="codeph"> sp_dedupe_field=title </span>, solo se muestra el resultado superior de un título determinado en los resultados de la búsqueda (ningún resultado tendrá el mismo contenido de campo de título). Para los campos de varios valores (lista de permitidos), se utiliza todo el contenido del campo para la comparación. Sólo se puede especificar un campo. No se permite un "calificador de tabla" en el nombre del campo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e= número </span> </p> </td> 
   <td colname="col4"> <p>Especifica que la expansión automática de comodines debe realizarse para cualquier palabra de la cadena de consulta con más de caracteres numéricos. En otras palabras, <span class="codeph"> sp_e=5 </span> especifica que las palabras con 5 o más caracteres, como "consulta" o "número", deben expandirse con el carácter comodín '*', lo que equivale a una búsqueda de "consulta*" o "número*". Las palabras con menos caracteres no se expanden, por lo que una búsqueda de "palabra" no tendría expansión automática de comodines. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e_#= número </span> </p> </td> 
   <td colname="col4"> <p>Especifica que la expansión automática de caracteres comodín se produce para cualquier palabra de la cadena de consulta <span class="codeph"> sp_q_# </span> correspondiente con más de caracteres numéricos. En otras palabras, <span class="codeph"> sp_e_2=5 </span> especifica que las palabras con cinco o más caracteres en la cadena de <span class="codeph"> consulta </span> sp_q_2, como "consulta" o "número", deben expandirse con el carácter comodín ' <span class="codeph"> * </span>', lo que equivale a una búsqueda de "consulta*" o "número*". Las palabras con menos caracteres no se expanden, por lo tanto una búsqueda de "palabra" en <span class="codeph"> sp_q_2 </span> no tendría expansión automática de comodines. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>sp_end_day, sp_end_month, sp_end_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_end_day= <i>number</i>,sp_end_month= <i>number</i>, sp_end_year= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Este triplete de valores especifica el intervalo de fechas de finalización de la búsqueda y debe proporcionarse como un conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>sp_f </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_f= cadena </span> </p> </td> 
   <td colname="col4"> <p>Especifica el conjunto de caracteres de las cadenas de parámetros de consulta (como <span class="codeph"> sp_q </span>). Esta cadena siempre debe coincidir con el conjunto de caracteres de la página que contiene el formulario de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>Define una tabla de datos lógica que consta de los campos dados. Por ejemplo, una tabla con el nombre "elementos" que consta de los campos "color", "tamaño" y "precio" se definiría de la siguiente manera: </p> <p> <span class="codeph"> sp_field_table=items:color,tamaño,precio </span> </p> <p>Las tablas lógicas son más útiles junto con los campos que tienen "Listas de permitidos" marcadas (en Configuración <span class="uicontrol"> &gt; </span> Metadatos <span class="uicontrol"> &gt; </span> Definiciones <span class="uicontrol"> </span>). Todos los parámetros CGI y las etiquetas de plantilla que toman un nombre de campo como valor pueden especificar opcionalmente un nombre de tabla seguido de "". antes del nombre del campo (por ejemplo, <span class="codeph"> sp_x_1=tablename.fieldname </span>). </p> <p>Por ejemplo, para realizar una búsqueda de documentos que contengan uno o más elementos "rojos" en el tamaño "grande" (donde los elementos se representan como filas paralelas de metadatos), puede utilizar lo siguiente: </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_i= <span class="varname"> valor </span> </span> </p> </td> 
   <td colname="col4"> <p>Omite la búsqueda cuando se generan informes. </p> <p>Utilice esta consulta para enmascarar determinadas búsquedas en segundo plano, como las búsquedas que creó o las búsquedas que genera un administrador en el centro de miembros. Dado que un usuario final no genera estos tipos de búsquedas, no se muestran en varios informes de Search&amp;Promote de Adobe. </p> <p>Los valores válidos son <span class="codeph"> sp_i=1 </span> y <span class="codeph"> sp_i=2 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>16 </p> </td> 
   <td colname="col2"> <p>sp_k </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_k= cadena </span> </p> </td> 
   <td colname="col4"> <p> Especifica la colección que se usará para la búsqueda. El valor predeterminado no es ninguna colección, lo que significa que la búsqueda debe incluir todo el sitio. </p> <p>Consulte <a href="../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3" type="reference" format="dita" scope="local"> Uso de colecciones en formularios de búsqueda </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>17 </p> </td> 
   <td colname="col2"> <p>sp_l </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_l= cadena </span> </p> </td> 
   <td colname="col4"> <p>Especifica el idioma de las cadenas de parámetros de consulta (como <span class="codeph"> sp_q </span>). La <i> cadena <span class="codeph"> </span></i> debe ser un ID de configuración regional estándar que contenga un código de idioma ISO-639, seguido opcionalmente por un código de país ISO-3166. Por ejemplo, "en" o "en_US" para inglés o "ja" o "ja_JP" para japonés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>18 </p> </td> 
   <td colname="col2"> <p>sp_literal </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_literal= 0 o 1 </span> </p> </td> 
   <td colname="col4"> <p> Al establecer <span class="codeph"> sp_literal=1 </span> se desactivan temporalmente todas las funciones que pueden interpretar las palabras de la consulta. Con este parámetro, solo las palabras literales de la consulta coinciden con los documentos, independientemente de los sinónimos, los formularios de palabras alternativas y la coincidencia de sonido. </p> <p>Tenga en cuenta que <span class="codeph"> sp_literal=0 no </span> tiene significado y se omite si se utiliza. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> Acerca de los diccionarios </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>19 </p> </td> 
   <td colname="col2"> <p>sp_m </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_m= número </span> </p> </td> 
   <td colname="col4"> <p> Especifica si se muestran los resúmenes. 1 es sí, 0 es no. El valor predeterminado es 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>20 </p> </td> 
   <td colname="col2"> <p>sp_n </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_n= número </span> </p> </td> 
   <td colname="col4"> <p> Especifica el número del resultado que inicio los resultados de búsqueda. El valor predeterminado es 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21 </p> </td> 
   <td colname="col2"> <p>sp_not_found_page </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_not_found_page= url </span> </p> </td> 
   <td colname="col4"> <p> Especifica si se redirige a la dirección URL especificada si no hay resultados de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22 </p> </td> 
   <td colname="col2"> <p>sp_p </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p= any/all/phrase </span> </p> </td> 
   <td colname="col4"> <p> Especifica el tipo predeterminado de búsqueda que se va a realizar. El uso de <span class="codeph"> cualquier </span> medio busca documentos que contengan cualquier palabra de la cadena de consulta. El uso de <span class="codeph"> todos </span> significa buscar documentos que contengan todas las palabras de la cadena de consulta. El uso de la <span class="codeph"> frase </span> significa que la cadena de consulta se trata como si fuera una frase citada y se omiten todas las comillas escritas por el usuario. </p> <p>Para <span class="codeph"> frase </span> y <span class="codeph"> todo </span>, la especificación de "+" y "-" antes de las palabras de búsqueda está deshabilitada y esos caracteres se omiten. Si <span class="codeph"> sp_p </span> no está presente, o si está establecido en una cadena vacía o cualquiera, se permiten prefijos de palabras estándar "+" y "-". </p> <p>Consulte la descripción de las sugerencias de búsqueda para obtener más información sobre el uso de más ("+") y menos ("-") en las búsquedas. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">Acerca de las búsquedas </a>. </p> <p>Consulte el formulario de búsqueda avanzada de ejemplo para ver ejemplos sobre el uso del parámetro <span class="codeph"> sp_p </span> . </p> <p>Consulte <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Ejemplo de formulario de búsqueda avanzada </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_p_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p_#= any/all/phrase </span> </p> </td> 
   <td colname="col4"> <p>Especifica el tipo predeterminado de búsqueda que se realizará con la consulta <span class="codeph"> sp_q_# </span> correspondiente. El "#" se sustituye por un número entre 1 y 16 (por ejemplo, <span class="codeph"> sp_p_8 </span> se aplica a la consulta numerada <span class="codeph"> sp_q_8 </span>). El uso de <span class="codeph"> cualquier </span> significa que se devuelven documentos que contienen cualquier palabra de la cadena de consulta. El uso de <span class="codeph"> todos </span> significa documentos de retorno que contienen todas las palabras de la cadena de consulta. El uso de la <span class="codeph"> frase </span> significa tratar la cadena de consulta como si fuera una frase completa (y se omiten todas las comillas escritas por el usuario). </p> <p>Si especifica <span class="codeph"> todo </span> o <span class="codeph"> frase </span>, se omiten los signos más y menos antes de las palabras de búsqueda. Si <span class="codeph"> sp_p_# </span> se omite, o si se define en una cadena vacía o en cualquier <span class="codeph"> , se permiten los prefijos </span>estándar "+" y "-". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>24 </p> </td> 
   <td colname="col2"> <p>sp_pt </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_pt= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p> Especifica el tipo de coincidencia de destinatarios que se va a aplicar. El uso de <span class="codeph"> exacto </span> significa que el destinatario de producción coincide solo en documentos que coinciden exactamente con la cadena de consulta dentro del contenido de destinatario. El uso de <span class="codeph"> equivalentes </span> es igual que exacto, excepto que el orden de las palabras no es importante. El uso de <span class="codeph"> compatible </span> establece automáticamente el tipo de coincidencia de destinatarios en función del valor del parámetro <span class="codeph"> sp_p </span> . El uso de <span class="codeph"> exacto </span> se utiliza si <span class="codeph"> sp_p </span> es <span class="codeph"> todo </span> o <span class="codeph"> frase </span>, de lo contrario <span class="codeph"> equivalente </span> . El valor predeterminado de <span class="codeph"> sp_pt </span> es <span class="codeph"> compatible </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_pt_# </p> </td> 
   <td colname="col3"> <p> <code> sp_pt_#= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica el tipo de coincidencia de destinatarios que se aplicará con la consulta <span class="codeph"> sp_q_# </span> correspondiente. El "#" se sustituye por un número entre 1 y 16 (por ejemplo, <span class="codeph"> sp_p_8 </span> se aplica a la consulta numerada <span class="codeph"> sp_q_8 </span>). El uso de <span class="codeph"> exacto </span> significa que el destinatario de producción coincide solo en documentos que coinciden exactamente con la cadena de consulta dentro del contenido de destinatario. El uso de <span class="codeph"> equivalentes </span> es como <span class="codeph"> exacto </span>, excepto que el orden de las palabras no es importante. El uso de <span class="codeph"> compatible </span> establece automáticamente el tipo de coincidencia de destinatarios en función del valor del parámetro <span class="codeph"> sp_p_# </span> correspondiente: <span class="codeph"> exacto </span> se utiliza si <span class="codeph"> sp_p_# </span> es todo o frase; de lo contrario, se utiliza <span class="codeph"> equivalente </span> . El valor predeterminado de <span class="codeph"> sp_pt_# </span> es <span class="codeph"> compatible </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>26 </p> </td> 
   <td colname="col2"> <p>sp_q </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q= cadena </span> </p> </td> 
   <td colname="col4"> <p> Especifica la cadena de consulta para la búsqueda. Una cadena vacía no produce ningún resultado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>27 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_q_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_#= texto </span> </p> </td> 
   <td colname="col4"> <p>Este parámetro permite crear varias consultas en los formularios de búsqueda. El parámetro <span class="codeph"> sp_q_# </span> contiene la cadena de consulta que se utilizará en la consulta numerada dada. Una solicitud de búsqueda puede hacer referencia a hasta 16 consultas numeradas diferentes ( <span class="codeph"> sp_q_1 </span> a <span class="codeph"> sp_q_16 </span>). </p> <p>Por ejemplo, al enviar el siguiente formulario se devuelven todos los documentos que contienen las palabras "bueno" y "libros". </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>28 </p> </td> 
   <td colname="col2"> <p>sp_q_day, sp_q_month, sp_q_year </p> </td> 
   <td colname="col03"> <p> sp_q _day_#, sp_q _month_#, sp_q_year_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_day= valor entero </span> </p> <p> <span class="codeph"> sp_q_month= valor entero </span> </p> <p> <span class="codeph"> sp_q_year= valor entero </span> </p> <p> <span class="codeph"> sp_q_day_#= valor entero </span> </p> <p> <span class="codeph"> sp_q_month_#= valor entero </span> </p> <p> <span class="codeph"> sp_q_year_#= valor entero </span> </p> </td> 
   <td colname="col4"> <p>Estos parámetros se utilizan para especificar una fecha exacta para una consulta en particular. Los parámetros <span class="codeph"> sp_q_day </span>, <span class="codeph"> sp_q_month </span>y <span class="codeph"> sp_q_year </span> se aplican a la consulta principal ( <span class="codeph"> sp_q </span>). </p> <p>El <span class="codeph"> # </span>parámetro se sustituye por un número entre 1 y 16 (por ejemplo, <span class="codeph"> sp_q_day_6 </span>, que se aplica a la consulta numerada <span class="codeph"> sp_q_6 </span>). De forma predeterminada, se buscan todas las fechas en relación con la hora media de Greenwich. </p> <p>La siguiente sección del código permite al usuario buscar la palabra "naranja" en documentos con fecha de "Ene. 1ro, 2000" en un campo definido por el usuario llamado <span class="codeph"> Fecha de publicación </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>29 </p> </td> 
   <td colname="col2"> <p>sp_q_location </p> </td> 
   <td colname="col03"> <p>sp_q_location_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> <p> <code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> </td> 
   <td colname="col4"> <p>Estos parámetros asocian una ubicación con la consulta principal o numerada. El uso de <span class="codeph"> sp_q_location </span> afecta a la consulta principal, <span class="codeph"> sp_q_location_# </span> (donde <span class="codeph"> # </span> se reemplaza por un número del 1 al 16), afecta a la consulta numerada dada. Estos parámetros se utilizan para realizar búsquedas de proximidad de distancia mínima y/o máxima en comparación con los datos de ubicación indizados para cada página del sitio. El formato del valor determina su interpretación. </p> <p>Un valor en la forma DDD (tres dígitos) se interpreta como un código de área telefónica de EE.UU.; un valor en el formulario DDDD o DDDDD-DDDD se interpreta como un código postal de EE.UU.; y un valor en la forma ±DD.DDDD±DDD.DDDD se interpreta como un par de latitud/longitud. Los signos son obligatorios para cada valor. Por ejemplo, +38.6317+120.5509 especifica la latitud 38.6317, la longitud 120.5509. </p> <p>Consulte <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Acerca de la búsqueda de proximidad </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>30 </p> </td> 
   <td colname="col2"> <p>sp_q_max_relevant_distance </p> </td> 
   <td colname="col03"> <p>sp_q_max_relevant_distance _# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_max_relevant_distance= <i>value</i> </code> </p> <p> <code> sp_q_max_relevant_distance_#= <i>value</i> </code> </p> </td> 
   <td colname="col4"> <p>Estos parámetros controlan el cálculo de relevancia aplicado a las búsquedas de proximidad. El uso de <span class="codeph"> sp_q_max_relevant_distance </span> afecta a la consulta principal, <span class="codeph"> sp_q_max_relevant_distance_# </span> (donde <span class="codeph"> # </span> se sustituye por un número del 1 al 16), afecta a la consulta numerada dada. </p> <p>El valor predeterminado de <span class="codeph"> sp_q_max_relevant_distance </span> es 100. </p> <p>Una puntuación de relevancia perfecta para el componente de proximidad representaría una distancia de 0. Una puntuación de relevancia mínima para el componente de proximidad representaría una distancia justo por encima del valor <span class="codeph"> sp_q_max_relevant_distance_# </span> especificado. </p> <p>Consulte <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Acerca de la búsqueda de proximidad </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>31 </p> </td> 
   <td colname="col2"> <p>sp_q_min_day, sp_q_min_month, sp_q_min_year </p> <p>sp_q_max_day, sp_q_max_month, sp_q_max_year </p> </td> 
   <td colname="col03"> <p>sp_q_min_day_#, sp_q_min_month_#, sp_q_min_year_# </p> <p> sp_q_max_day_#, sp_q_max_month_#, sp_q_max_year_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_min_day=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year=<i>integer value</i> </code> </p> <p> <code> sp_q_min_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year_#=<i>integer value</i> </code> </p> </td> 
   <td colname="col4"> <p>Estos parámetros se utilizan para establecer intervalos de fechas mínimos y máximos para una consulta en particular. Los parámetros <span class="codeph"> sp_q_min_day </span>, <span class="codeph"> sp_q_min_month </span>, <span class="codeph"> sp_q_min_year </span>, <span class="codeph"> sp_q_max_day </span>, <span class="codeph"> sp_q_max_month </span><i></i> <span class="codeph"> </span>ysp_max_year se aplican a la consulta principal ( sp_q ). </p> <p>El <span class="codeph"> # </span>en el nombre del parámetro se sustituye por un número entre 1 y 16 (por ejemplo, <span class="codeph"> sp_q_min_day_6 </span> se aplica a la consulta numerada <span class="codeph"> sp_q_6 </span>). </p> <p>Es legal especificar solamente una fecha mínima, solamente una fecha máxima o tanto una fecha mínima como una fecha máxima. Sin embargo, para un conjunto mínimo o máximo determinado, deben especificarse los tres parámetros de fecha (día, mes y año). De forma predeterminada, se buscan todas las fechas en relación con la hora media de Greenwich. </p> <p>La siguiente sección de código permite al usuario buscar la palabra "naranja" en documentos con una fecha entre el 1 de enero de 2000 y el 31 de diciembre de 2000 en un campo definido por el usuario llamado <span class="codeph"> Fecha de publicación </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>32 </p> </td> 
   <td colname="col2"> <p>sp_q_min, sp_q_max </p> </td> 
   <td colname="col03"> <p>sp_q _min_#, sp_q _max_#, sp_q _exacto_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_min= valor </span> </p> <p> <span class="codeph"> sp_q_max= valor </span> </p> <p> <span class="codeph"> sp_q_min_#= valor </span> </p> <p> <span class="codeph"> sp_q_max_#= valor </span> </p> <p> <span class="codeph"> sp_q_exacto_#=value </span> </p> </td> 
   <td colname="col4"> <p>Estos parámetros especifican un valor mínimo (y/o máximo) que se aplicará a la consulta principal o numerada. El uso de <span class="codeph"> sp_q_min </span>, <span class="codeph"> sp_q_max </span>y <span class="codeph"> sp_q_exacto </span> afecta a la consulta principal ( <span class="codeph"> sp_q </span>). </p> <p>Reemplace <span class="codeph"> # </span>en el nombre del parámetro con un número entre 1 y 16 (por ejemplo, <span class="codeph"> sp_q_min_8 </span> se aplica a la consulta numerada <span class="codeph"> sp_q_8 </span>). </p> <p>El uso de <span class="codeph"> sp_q_exacto_# </span> es abreviado para especificar <span class="codeph"> sp_q_min_# </span> y <span class="codeph"> sp_q_max_# </span> con el mismo valor. Si se especifica <span class="codeph"> sp_q_exacto_# </span> , se omiten los parámetros correspondientes de <span class="codeph"> sp_q_min_# </span> o <span class="codeph"> sp_q_max_# </span> . </p> <p>Los parámetros <span class="codeph"> sp_q_min_# </span>, <span class="codeph"> sp_q_max_# </span> y <span class="codeph"> sp_q_exacto_# </span> pueden especificar opcionalmente varios valores separados por "|". Por ejemplo, para buscar documentos que contengan el valor verde o rojo en el campo "color": <span class="codeph"> ...&amp;sp_q_exacto_1=green|red&amp;sp_x_1=color </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>33 </p> </td> 
   <td colname="col2"> <p>sp_q_nocp </p> </td> 
   <td colname="col03"> <p>sp_q _nocp _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_nocp= 1 o 0 </span> </p> <p> <span class="codeph"> sp_q_nocp_#= 1 o 0 </span> </p> </td> 
   <td colname="col4"> <p>El valor predeterminado del parámetro es <span class="codeph"> 0 </span> , lo que significa que se realizan expansiones de frase común. </p> <p>Cuando se establece en <span class="codeph"> 1 </span> para la consulta de búsqueda correspondiente, no se realizan las expansiones de frases comunes. </p> <p>El uso de <span class="codeph"> sp_q_nocp </span> afecta al parámetro de consulta de búsqueda principal <span class="codeph"> sp_q </span>. Para aplicar este parámetro a una consulta de búsqueda numerada, reemplace <span class="codeph"> # </span> en el nombre del parámetro por el número correspondiente. Por ejemplo, <span class="codeph"> sp_q_nocp_8 </span> se aplica a la consulta de búsqueda numerada <span class="codeph"> sp_q_8 </span>. </p> <p> 
     <!--See also <xref href="c_about_common_phrases.xml#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local">About Common Phrases</xref>--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>34 </p> </td> 
   <td colname="col2"> <p>sp_q_required </p> </td> 
   <td colname="col03"> <p>sp_q_required _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_required= 1 o 0 o -1 </span> </p> <p> <span class="codeph"> sp_q_required_#= 1 o 0 o -1 </span> </p> </td> 
   <td colname="col4"> <p>Este parámetro determina si una coincidencia debe (1), puede (0) o no debe (-1) producirse en la consulta correspondiente para que se devuelva un documento en la página de resultados. </p> <p>El uso de <span class="codeph"> sp_q_required </span> afecta a la consulta principal ( <span class="codeph"> sp_q </span>). </p> <p>Para aplicar a una consulta numerada, reemplace el <span class="codeph"> # </span> en el nombre del parámetro por el número correspondiente (por ejemplo, <span class="codeph"> sp_q_required_8 </span> se aplica a la consulta numerada <span class="codeph"> sp_q_8 </span>). El valor predeterminado del parámetro es 1 (debe coincidir). </p> <p>Para buscar documentos que contengan la palabra "calc" pero NO contengan "mac", "win" o "all" en el campo "platform" definido por el usuario, el formulario de búsqueda HTML podría contener las siguientes líneas: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>35 </p> </td> 
   <td colname="col2"> <p>sp_redirect_if_one_result </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica si se redirige a la dirección URL del resultado de búsqueda si solo hay un resultado de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>36 </p> </td> 
   <td colname="col2"> <p>sp_remitente del reenvío </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_remitente del reenvío= url </span> </p> </td> 
   <td colname="col4"> <p>Especifica la dirección URL de remitente del reenvío para la búsqueda. Útil para las reglas de reescritura de búsqueda donde los resultados de búsqueda se vinculan al mismo sitio que el formulario de búsqueda. </p> <p>El valor predeterminado es el valor HTTP_REMITENTE DEL REENVÍO CGI estándar proporcionado por el explorador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>37 </p> </td> 
   <td colname="col2"> <p>sp_ro </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_ro= <span class="varname"> campo </span>: <span class="varname"> relevancia </span> </span> </p> </td> 
   <td colname="col4"> <p>Permite el control de relevancia, por nombre de campo y tiempo de búsqueda opcional. La <span class="codeph"> cadena "ro" </span> en el nombre del parámetro significa "relevancia". El parámetro acepta uno o más nombres de campo, seguido de dos puntos de carácter, seguido de un valor de relevancia de 0 a 10. </p> <p>Por ejemplo, para establecer el valor de relevancia del nombre de campo "body" en 10, en el momento en que un cliente realice una búsqueda, el parámetro aparecerá de la siguiente manera: </p> <p> <span class="codeph"> sp_ro=body:10 </span> </p> <p>O bien, para especificar varias anulaciones de relevancia de campo en la cadena de parámetro, puede utilizar un delimitador de barra vertical. Por ejemplo, para establecer el valor de relevancia de los nombres de campo "body" y "title" en 9, en el momento en que un cliente realice una búsqueda, el parámetro aparecerá de la siguiente manera: </p> <p> <span class="codeph"> sp_ro=body:9|title:9 </span> </p> <p> <p>Nota:  Especificar un campo que no esté involucrado en la búsqueda asociada no tiene ningún efecto. Por ejemplo, si establece <span class="codeph"> sp_ro=title:10 </span>, pero no se busca en el nombre del <span class="codeph"> campo de </span> título, el parámetro <span class="codeph"> sp_ro </span> no tendrá ningún efecto. En otras palabras, si se especifica un nombre de campo con el parámetro <span class="codeph"> sp_ro </span> , no se buscará automáticamente ese campo; en su lugar, solo anula la configuración de relevancia asociada a ese campo. </p> </p> <p>Consulte <a href="../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3" type="task" format="dita" scope="local"> Edición de campos de etiquetas meta predefinidos o definidos por el usuario </a>. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" type="concept" format="dita" scope="local"> Acerca de las reglas de limpieza de Consultas </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>38 </p> </td> 
   <td colname="col2"> <p>sp_s </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_s= número </span> </p> </td> 
   <td colname="col4"> <p>Especifica el orden. Cero (0) es el valor predeterminado y significa ordenar por puntuación de relevancia. Uno (1) significa ordenar por fecha y -1 significa no ordenar. </p> <p>Puede especificar un nombre de campo para el valor del parámetro <span class="codeph"> sp_s </span> . Por ejemplo, <span class="codeph"> sp_s=title </span> ordena los resultados según los valores contenidos en el campo de título. Cuando se utiliza un nombre de campo para el valor de un parámetro <span class="codeph"> sp_s </span> , los resultados se ordenan por ese campo y luego se subordenan por relevancia. </p> <p>Establezca la opción Ordenar para el campo al que se hace referencia en <span class="uicontrol"> De subida </span> o <span class="uicontrol"> De bajada </span> en Configuración <span class="uicontrol"> &gt; </span> Metadatos <span class="uicontrol"> &gt; </span> Definiciones <span class="uicontrol"> </span> para habilitar esta función. </p> <p>También puede asignar varios campos de ordenación a una sola consulta estableciendo el parámetro <span class="codeph"> sp_s </span> varias veces en el formulario de búsqueda. Las siguientes líneas de plantilla establecen los resultados de búsqueda que se ordenarán primero por nombre del artista, luego por nombre del álbum y, a continuación, por nombre de la pista. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code> </p> <p>También es posible ordenar los datos de campo coincidentes de la tabla especificando un calificador de nombre de tabla antes del nombre del campo, por ejemplo, items.price. Consulte el parámetro <span class="codeph"> sp_field_table </span> para obtener más información sobre la coincidencia de tablas. </p> <p>Si realiza una búsqueda por proximidad, puede ordenar los resultados según la proximidad especificando un "campo de salida de proximidad". </p> <p>Consulte <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Acerca de la búsqueda de proximidad </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>39 </p> </td> 
   <td colname="col2"> <p>sp_sr </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sr= field </span> </p> </td> 
   <td colname="col4"> <p>Especifica el campo de clasificación que se usará para la clasificación estática. El campo debe ser un campo de tipo Clasificación con relevancia buena a 0. Si no se proporciona ningún parámetro <span class="codeph"> sp_sr </span> para la consulta, se selecciona automáticamente un campo de tipo Clasificación. </p> <p>Para deshabilitar la clasificación estática de una consulta en particular, incluya un valor NULL para <span class="codeph"> sp_sr </span> (por ejemplo, <span class="codeph"> &lt;input type="hidden" name="sp_sr" value=""&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>40 </p> </td> 
   <td colname="col2"> <p>sp_sfvl_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_field= string </span> </p> </td> 
   <td colname="col4"> <p>Especifica el nombre de un campo que se utilizará junto con la etiqueta <span class="codeph"> &lt;search-field-value-lista&gt; </span> de la plantilla de búsqueda. </p> <p>Puede especificar varios parámetros <span class="codeph"> sp_sfvl_field </span> . </p> </td> 
  </tr> 
  <tr>
   <td colname="col1"> <p>41 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_count </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_df_count= <span class="varname"> &lt;valor_entero&gt; </span> </span> </p> </td> 
   <td colname="col4"> <p> Solicita hasta <span class="codeph"> &lt;integer_value&gt; <span class="varname"> </span></span> campos de búsqueda-campo-valor-lista <span class="codeph"> </span> dinámica-faceta para esta búsqueda. </p> <p>El valor predeterminado es 0. El valor máximo permitido es el número actual de campos de facetas dinámicas, recuento de campos de facetas dinámicas definido para un índice determinado. Los valores enteros inferiores a 0 se tratan como 0. Los valores enteros especificados arriba <span class="codeph"> dynamic-facet-field-count </span> se limitan al recuento de campos de facetas <span class="codeph"> dinámicas </span>. Se omiten los valores no enteros; se tratan como el valor predeterminado. </p> <p>La búsqueda de una fracción dada se limita con un valor máximo permitido <span class="codeph"> sp_sfvl_df_count </span> del valor de recuento de campos de facetas <span class="codeph"> dinámicas de esta fracción </span> . Al combinar los resultados de la fracción, el valor máximo efectivo de <span class="codeph"> sp_sfvl_df_count </span> es el máximo de sp_sfvl_df_count real <span class="codeph"> </span> en todas las divisiones. </p> <p>Consulte <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> Configuración de facetas dinámicas </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>42 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_exclude </p> </td> 
   <td colname="col03"> <p> </p> </td>
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_exclude= &lt; <span class="varname"> nombre_campo </span>&gt;[|&lt; <span class="varname"> nombre_campo </span> </span>&gt;|... </p> </td> 
   <td colname="col4"> <p> Especifica una lista de campos de facetas dinámicas específicos para excluir de la consideración de esta búsqueda. </p> <p>De forma predeterminada, se tienen en cuenta todos los campos de facetas dinámicas. </p> <p>Consulte <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> Configuración de facetas dinámicas </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>43 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_include </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_include= &lt; <span class="varname"> nombre_campo </span>&gt;[|&lt; <span class="varname"> nombre_campo </span> </span>&gt;|... </p> </td> 
   <td colname="col4"> <p> Especifica una lista de campos de facetas dinámicas específicos para incluir en los resultados de búsqueda. </p> <p> <p>Nota:  El parámetro <span class="codeph"> sp_sfvl_df_count </span> determina el número total de campos de facetas dinámicas que se devolverán, incluido cualquier especificado mediante <span class="codeph"> sp_sfvl_df_include </span>. Es decir, el uso de <span class="codeph"> sp_sfvl_df_include </span> no permite que el recuento total de campos de facetas dinámicas devueltos supere <span class="codeph"> sp_sfvl_df_count </span>. </p> </p> <p>Consulte <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> Configuración de facetas dinámicas </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>44 </p> </td> 
   <td colname="col2"> <p>sp_staged </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_staged= 0 o 1 </span> </p> </td> 
   <td colname="col4"> <p>Si <span class="codeph"> sp_staged=1 </span> se envía con una consulta, la consulta que se ejecuta es una búsqueda por etapas. </p> <p>Una búsqueda por etapas utiliza todos los componentes que se encuentran actualmente por etapas, incluidos el índice y las plantillas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>45 </p> </td> 
   <td colname="col2"> <p>sp_inicio_day, sp_inicio_month, sp_inicio_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_inicio_day= número </span> </p> <p> <span class="codeph"> sp_inicio_month= número </span> </p> <p> <span class="codeph"> sp_inicio_year= número </span> </p> </td> 
   <td colname="col4"> <p>Este triplete de valores especifica el intervalo de fechas de inicio de la búsqueda y se proporciona como un conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>46 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_ sugerir _q </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_offer_q= número </span> </p> </td> 
   <td colname="col4"> <p>El parámetro <span class="codeph"> sp_offer_q </span> determina qué <span class="codeph"> parámetro sp_q[_#] </span> utilizar con el servicio Sugerir. </p> <p>El valor predeterminado de <span class="codeph"> sp_offer_q </span> es 0, lo que significa que el motor de búsqueda utiliza el valor de <span class="codeph"> sp_q </span> para determinar las sugerencias. </p> <p>Establezca <span class="codeph"> sp_offer_q=1 </span> para utilizar el valor de <span class="codeph"> sp_q_1 </span> para determinar las sugerencias, etc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>47 </p> </td> 
   <td colname="col2"> <p>sp_t </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_t= cadena </span> </p> </td> 
   <td colname="col4"> <p>Especifica la plantilla de transporte que se va a utilizar. </p> <p>Este parámetro es útil si desea controlar la apariencia de los resultados de búsqueda principales en el sitio web mediante el uso de distintas plantillas de transporte de búsqueda para cada área de la cuenta de búsqueda. </p> <p>La plantilla de transporte predeterminada es "search". </p> <p>Consulte <a href="../c-appendices/c-templates.md#reference_12AAB3B9F4C74C11956F1DBA95714C2F" type="reference" format="dita" scope="local"> Administración de varias plantillas de transporte para el sitio web </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>48 </p> </td> 
   <td colname="col2"> <p>sp_trace </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_trace= 0 o 1 </span> </p> </td> 
   <td colname="col4"> <p>Cuando se configura como <span class="codeph"> sp_stage=1 </span>, habilita la capacidad de seguimiento de búsqueda principal en el simulador. </p> <p>Consulte <a href="../c-about-simulator.md#concept_020AA6751E32421A96A3455508364C7E" format="dita" scope="local"> Acerca del simulador </a>. </p> <p> <p>Nota:  Si no se especifica este parámetro, la búsqueda principal no recopila la información de seguimiento y las etiquetas de plantilla de búsqueda principal relacionadas no tienen salida. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>49 </p> </td> 
   <td colname="col2"> <p>sp_w, sp_w_control </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_w= <i>sound-alike-enable</i> </code> </p> <p> <code> sp_w_control=<i>sound-alike-control</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica que la coincidencia de sonido similar debe habilitarse o deshabilitarse para esta consulta en particular. </p> <p>Se omite sp_w_control para "Exact". La coincidencia de ambos sonidos está deshabilitada. </p><p>Se omite sp_w_control para "Alike". Coincidencia de sonido similar habilitada</p><p>sp_w_control para Cualquiera es 1. La coincidencia de ambos sonidos está deshabilitada. </p><p>El sp_w_control para Cualquiera es cualquier otra cosa. La coincidencia de ambos sonidos está habilitada. </p>El <span class="codeph"> parámetro sp_w_control </span> permite crear una casilla de verificación con una redacción negativa o positiva para el control del usuario final de la coincidencia de sonido. </p> <p>Si se utiliza <span class="codeph"> sp_w_control=0 </span> , se utiliza una casilla de verificación con una redacción negativa para establecer el parámetro <span class="codeph"> sp_w </span> como en el siguiente ejemplo: </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code> </p> <p>Si se utiliza <span class="codeph"> sp_w_control=1 </span> , se utiliza una casilla de verificación con una redacción positiva para establecer el parámetro <span class="codeph"> sp_w </span> como se indica a continuación: </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code> </p> <p>Consulte el formulario de búsqueda avanzada de ejemplo para obtener más ejemplos sobre el uso de los parámetros <span class="codeph"> sp_w_control </span> y <span class="codeph"> sp_w </span> . </p> <p>Consulte <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Ejemplo de formulario de búsqueda avanzada </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>50 </p> </td> 
   <td colname="col2"> <p>sp_x </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x= field </span> </p> </td> 
   <td colname="col4"> <p>Especifica los campos en los que se buscará la cadena de consulta. por cualquier medio, busque todos los campos. title significa buscar solo campos de título. desc significa buscar solo los campos de descripción del documento. key significa buscar sólo palabras clave de documento. body significa buscar solo texto principal. alt significa buscar solo texto alternativo. url significa buscar solamente los valores de la dirección URL. destinatario significa buscar sólo palabras clave de destinatario. En cualquiera de estos casos, se omiten las especificaciones del usuario de los prefijos de campo "text:", "desc:", "keys:", "body:", "alt:", "url:" y "destinatario:" dentro del parámetro <span class="codeph"> sp_q </span> correspondiente. Si <span class="codeph"> sp_x </span> no está presente o si está establecido en una cadena vacía o cualquiera, se permiten los prefijos de campo de usuario estándar. Consulte la descripción de las sugerencias de búsqueda para obtener más información sobre los prefijos de campo. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">Acerca de las búsquedas </a>. </p> <p>Consulte la descripción del formulario de búsqueda avanzada de ejemplo para ver ejemplos de uso del parámetro <span class="codeph"> sp_x </span> . </p> <p>Consulte <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Ejemplo de formulario de búsqueda avanzada </a>. </p> <p>Puede crear consultas que busquen en todos los campos definidos como <span class="uicontrol"> Buscar por defecto </span> en Opciones <span class="uicontrol"> &gt; </span> Metadatos <span class="uicontrol"> &gt; </span> Definiciones <span class="uicontrol"> estableciendo </span> sp_x=cualquiera <span class="codeph"> </span>. Los campos predefinidos y los definidos por el usuario pueden utilizarse como el valor del parámetro <span class="codeph"> sp_x </span> . </p> <p>También puede asignar varios campos a una sola consulta estableciendo varias veces el parámetro <span class="codeph"> sp_x </span> . Las siguientes líneas de plantilla permiten a los usuarios consulta los campos "título" y "autor" para "Buenos libros". </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>51 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_x_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x_#= field-name </span> </p> </td> 
   <td colname="col4"> <p>Este parámetro especifica qué campo buscar en la consulta <span class="codeph"> sp_q_# </span> correspondiente. El <span class="codeph"> # <span class="codeph"> </span> se sustituye por un número entre 1 y 16 (por ejemplo, </span> sp_x_8 <span class="codeph"> </span>). El campo field-name es cualquier campo predefinido o definido por el usuario. </p> <p>Si no se proporciona ningún parámetro <span class="codeph"> sp_x_# </span> para una consulta numerada concreta, esa consulta buscará todos los campos definidos como <span class="uicontrol"> Buscar por defecto </span> tal como se define en Configuración <span class="uicontrol"> &gt; </span> Metadatos <span class="uicontrol"> &gt; </span> Definiciones <span class="uicontrol"> </span> . </p> <p>Por ejemplo, al enviar el siguiente formulario se devuelven todos los documentos que contienen la palabra "bueno" que también contienen la palabra "Fitzgerald" en el campo "autor": </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code> </p> <p>Puede asociar varios nombres de campo con una consulta concreta o una consulta numerada proporcionando más de una instancia del mismo parámetro <span class="codeph"> sp_x </span> o <span class="codeph"> sp_x_# </span> en una sola solicitud de búsqueda. </p> <p>Por ejemplo, para buscar la palabra "flor" en los campos "cuerpo" y "claves", puede crear un formulario de búsqueda con la siguiente información: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo típico de uso de parámetros CGI de búsqueda back-end {#section_260012BBC2514CC9A8E02E53DE8B41EE}

Las siguientes consultas de vínculos inicio una búsqueda utilizando &quot;Música&quot; como consulta de búsqueda y utilizan todos los parámetros predeterminados. Tenga en cuenta que la dirección URL está dividida en dos líneas para facilitar la lectura. En el HTML, este vínculo debe estar en una sola línea.

```
<a href="https://search.atomz.com/search/?sp_q=Music&sp_a=sp99999999"> 
Testing...</a>
```

La misma funcionalidad se define más generalmente con un formulario:

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q" value="Music"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
</form>
```

Normalmente, debe utilizar parámetros predeterminados al iniciar una búsqueda. De este modo, se muestra la primera página, ordenada por relevancia, y permite al cliente elegir otras páginas y otras opciones. Si el formulario de búsqueda del sitio incluye opciones para las colecciones, pase el nombre de la colección como parámetro.

## Ejemplo detallado del uso de parámetros CGI de búsqueda back-end {#section_5FA3C620D5124FB2AB28857F8D8473F6}

Las siguientes consultas de formulario muestran `25` los resultados empezando por el resultado `10`. No se muestran los resúmenes, el orden es por fecha y se utiliza la colección denominada `support` . Sólo se devuelven los documentos con fecha de los últimos 30 días.

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
<input type=hidden name=sp_n value=10> 
<input type=hidden name=sp_c value=25> 
<input type=hidden name=sp_m value=0> 
<input type=hidden name=sp_s value=1> 
<input type=hidden name=sp_k value="support"> 
<input type=hidden name=sp_date_range value=30> 
</form>
```

