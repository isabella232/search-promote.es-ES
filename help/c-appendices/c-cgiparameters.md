---
description: Obtenga información sobre cómo utilizar varios parámetros CGI.
solution: Target
title: Parámetros de CGI
topic: Apéndices, búsqueda de sitios y comercialización
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1943'
ht-degree: 1%

---


# Parámetros CGI{#cgi-parameters}

## Parámetros CGI {#concept_F395999090FE4926B38BC73D5E612800}

## Buscar parámetros CGI {#reference_DA27A8B0728246DA94994885E1353890}

Se proporciona código de formulario de búsqueda que puede copiar y pegar en el HTML del sitio ( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**).

Consulte [Copia del código HTML del formulario de búsqueda en el...](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

También puede definir los parámetros que se enumeran en el propio formulario de búsqueda o desde una secuencia de comandos. Además de los parámetros que se enumeran a continuación, también puede utilizar los parámetros de búsqueda back-end para controlar la búsqueda.

Consulte [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

Las solicitudes de búsqueda constan de una dirección URL base. La dirección URL base indica qué cuenta está buscando el cliente y un conjunto de parámetros CGI (pares clave-valor) que indican cómo devolver los resultados de búsqueda deseados para la cuenta asociada.

La dirección URL base está asociada a una cuenta específica y a un entorno de ensayo o lanzamiento. El administrador de cuentas puede solicitar varios alias para la URL base. Por ejemplo, una empresa llamada Megacorp puede tener dos direcciones URL base asociadas a su cuenta: `https://search.megacorp.com` y `https://stage.megacorp.com`. La URL anterior busca su índice activo y la segunda URL busca su índice por etapas.

Se admiten tres formatos de parámetros CGI. De forma predeterminada, su cuenta está configurada para separar los parámetros CGI con un punto y coma, como en el siguiente ejemplo:

`https://search.megacorp.com?q=shoes;page=2`

Si lo prefiere, puede hacer que su administrador de cuentas configure su cuenta para que utilice el símbolo &amp; para separar los parámetros CGI como en el siguiente ejemplo:

`https://search.megacorp.com?q=shoes&page=2`

También se admite un tercer formato, denominado formato SEO, en el que se utiliza una barra diagonal `/` en lugar del separador y el signo igual como en el siguiente ejemplo:

`https://search.megacorp.com/q/shoes/page/2`

Cada vez que se utiliza el formato SEO para enviar una solicitud, todos los vínculos de salida se devuelven en el mismo formato.

| Parámetro de búsqueda guiada | Ejemplo | Descripción |
|--- |--- |--- |
| q | `q=string` | Especifica la cadena de consulta para la búsqueda. Este parámetro se asigna al parámetro de búsqueda back-end `sp_q` .  Consulte [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| q# | `q#=string` | La faceta (búsqueda dentro de un campo determinado) se realiza mediante parámetros q y x numerados.  El parámetro q define el término que está buscando en la faceta como se indica en el parámetro x numerado correspondiente.<br>Por ejemplo, si tiene dos facetas con nombres tamaño y color, puede tener algo como q1=pequeño;x1=tamaño;q2=rojo;x2=color.  Este parámetro se asigna a los parámetros de búsqueda back-end `sp_q_exact_#`.  <br>Consulte  [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| x# | `q#=string` | La faceta (búsqueda dentro de un campo determinado) se realiza mediante parámetros q y x numerados.  El parámetro q define el término que está buscando en la faceta como se indica en el parámetro x numerado correspondiente. <br>Por ejemplo, si tiene dos facetas con nombres tamaño y color, puede tener algo como q1=pequeño;x1=tamaño;q2=rojo;x2=color.  Este parámetro se asigna a los parámetros de búsqueda back-end `sp_x_#`.  <br>Consulte  [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| colección | `collection=string` | Especifica la colección que se usará para la búsqueda.  Este parámetro se asigna al parámetro de búsqueda back-end `sp_k` .  Consulte [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| count | `count=number` | Especifica el recuento total de resultados que se muestran.  El valor predeterminado se define en [!UICONTROL Settings ] > [!UICONTROL Searching ] > [!UICONTROL Searches ]. .  Este parámetro se asigna al parámetro de búsqueda back-end `sp_c` .  Consulte [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| página | `page=number` | Especifica la página de resultados que se devuelven. |
| rank | `rank=field` | Especifica el campo de clasificación que se utilizará para la clasificación estática.  El campo debe ser un campo de tipo Clasificación con relevancia buena a 0.  Este parámetro se asigna al parámetro back-end `sp_sr` .  Consulte [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| sort | `sort=number` | Especifica el orden.<br>&quot;0&quot; es el valor predeterminado y se ordena por puntuación de relevancia; &quot;1&quot; se clasifica por fecha; &quot;-1&quot; no se ordena.  Los usuarios pueden especificar un nombre de campo para el valor del parámetro `sp_s`.  Por ejemplo, `sp_s=title` ordena los resultados según los valores contenidos en el campo de título. Cuando se utiliza un nombre de campo para el valor de un parámetro ` sp_s ` , los resultados se ordenan por ese campo y luego se subordenan por relevancia.  Para habilitar esta función, haga clic en [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. En la página Definiciones , haga clic [!UICONTROL Add New Field ] o haga clic [!UICONTROL Edit ] para un nombre de campo determinado. En la lista desplegable [!UICONTROL Sorting ], seleccione [!UICONTROL Ascending ] o [!UICONTROL Descending ]. Este parámetro se asigna al parámetro de búsqueda back-end `sp_s` . <br>Consulte  [Parámetros CGI de búsqueda back-end].(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |

## Parámetros CGI de búsqueda back-end {#reference_582E85C3886740C98FE88CA9DF7918E8}

Normalmente, los clientes interactúan con una capa de presentación denominada Búsqueda guiada. Sin embargo, teóricamente es posible omitir la capa Búsqueda guiada e interactuar con la búsqueda principal del servidor directamente utilizando los parámetros CGI que se describen en esta página.

Puede seleccionar parámetros CGI de búsqueda backend de la siguiente tabla:
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
   <td colname="col3"> <p> <code>sp_a= string </code> </p> </td> 
   <td colname="col4"> <p>Especifica la cadena del número de cuenta. Este parámetro es obligatorio y debe ser una cadena de número de cuenta válida. Puede encontrar la cadena del número de cuenta en <span class="uicontrol"> Configuración </span> &gt; <span class="uicontrol"> Opciones de cuenta </span> &gt; <span class="uicontrol"> Configuración de cuenta </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_advanced= 0 or 1 </code> </p> </td> 
   <td colname="col4"> <p>Si <code>sp_advanced=1 </code> se envía con una consulta, todo el código entre la etiqueta <code>&lt;search-if-advanced&gt; </code> y la etiqueta <code>&lt;/search-if-advanced&gt; </code> en la plantilla de búsqueda se utiliza para el formulario de búsqueda. Se ignorará todo el código entre la etiqueta <code>&lt;search-if-not-advanced&gt; </code> y la etiqueta <code>&lt;/search-if-not-advanced&gt; </code>. Si se envía <code>sp_advanced=0 </code> (o cualquier otro valor), se ignora el bloque de plantilla &lt;search-if-advanced&gt; y se utiliza el bloque de plantilla &lt;search-if-not-advanced&gt; . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_c= number </code> </p> </td> 
   <td colname="col4"> <p>Especifica el recuento total de resultados que se van a mostrar. El valor predeterminado es 10. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>Recopila información contextual para el campo dado. La información recopilada se muestra en los resultados de búsqueda mediante la etiqueta de plantilla <code>&lt;search-context&gt; </code>. El valor predeterminado es <code>body </code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_d= type </code> </p> </td> 
   <td colname="col4"> <p>Especifica el tipo de búsqueda de intervalo de fechas que se va a realizar. Los valores posibles de tipo son cualquiera, lo que significa que no realice búsquedas de intervalos de fechas, personalizadas, lo que indica que el valor de <code>sp_date_range </code> debe utilizarse para determinar las fechas de búsqueda y específicas, lo que indica que los valores de <code>sp_start_day </code>, <code>sp_start_month </code>, <code>sp_start_year </code>, <code>sp_end_day </code>, <code>sp_end_month </code> y <code>sp_end_year </code> se utilizan para determinar el intervalo de fechas que se buscará. <code>sp_d </code> solo es necesario si el formulario de búsqueda contiene la opción de buscar por un intervalo personalizado (a modo de  <code>sp_date_range </code>) o por un intervalo de fechas de inicio y finalización específico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <code>sp_d_#= type </code> </p> </td> 
   <td colname="col4"> <p>Especifica el tipo de intervalo de fechas que se busca para la consulta <code>sp_q_# </code> correspondiente. El "#" se sustituye por un número entre 1 y 16 (por ejemplo, <code>sp_d_8 </code>, se aplica a la consulta numerada <code>sp_q_8 </code>). </p> <p>Puede establecer <code>type </code> en cualquier, lo que significa que no realice búsquedas de intervalos de fechas personalizadas, lo que indica que el valor de <code>sp_date_range_# </code> se utiliza para determinar las fechas de búsqueda y específico, lo que indica que los valores de <code>sp_q_min_day_# </code>, <code>sp_q_min_month_# </code>, <code>sp_q_min_year_# </code>, <code>sp_q_max_day_# </code>, <code>sp_q_max_month_# </code> y <code>sp_q_max_year_# </code> deben utilizarse para determinar el intervalo de fechas. El uso de <code>sp_d_# </code> solo es necesario si el formulario de búsqueda contiene la opción de buscar por un intervalo personalizado (mediante <code>sp_date_range_# </code>) o por un intervalo de fechas de inicio y finalización específico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica un intervalo de fechas predefinido que se aplicará a la búsqueda. Los valores buenos que son iguales o iguales a cero especifican el número de días que se buscarán antes de hoy; por ejemplo, un valor de "0" especifica "hoy", un valor de "1" especifica "hoy y ayer", un valor de "30" especifica "en los últimos 30 días", etc. </p> <p>Los valores por debajo de cero especifican un intervalo personalizado de la siguiente manera: </p> <p>-1 = "Ninguno", del mismo modo que se especifica sin intervalo de fechas. </p> <p>-2 = "Esta semana", que busca de domingo a sábado de la semana actual. </p> <p>-3 = "Última semana", que busca de domingo a sábado de la semana anterior a la semana actual. </p> <p>-4 = "Este mes", que busca fechas dentro del mes actual. </p> <p>-5 = "Último mes", que busca fechas dentro del mes anterior al mes actual. </p> <p>-6 = "Este año", que busca fechas dentro del año actual. </p> <p>-7 = "Último año", que busca fechas dentro del año anterior al año actual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica un intervalo de fechas predefinido para aplicar a la consulta <code>sp_q_# </code> correspondiente. El "#" se sustituye por un número entre 1 y 16 (por ejemplo, <code>sp_date_range_8 </code>, se aplica a la consulta numerada <code>sp_q_8 </code>). </p> <p>Los valores buenos o iguales a cero especifican la cantidad de días que se buscarán antes de hoy. Por ejemplo, un valor de 0 especifica hoy; un valor de 1 especifica hoy y ayer; un valor de 30 especifica en los últimos 30 días, etc. </p> <p>Los valores por debajo de cero especifican un intervalo personalizado de la siguiente manera: </p> <p>-1 = "Ninguno", del mismo modo que se especifica sin intervalo de fechas. </p> <p>-2 = "Esta semana", que busca de domingo a sábado de la semana actual. </p> <p>-3 = "Última semana", que busca de domingo a sábado de la semana anterior a la semana actual. </p> <p>-4 = "Este mes", que busca fechas dentro del mes actual. </p> <p>-5 = "Último mes", que busca fechas dentro del mes anterior al mes actual. </p> <p>-6 = "Este año", que busca fechas dentro del año actual. </p> <p>-7 = "Último año", que busca fechas dentro del año anterior al año actual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>Especifica un solo campo en el que se van a desduplicar los resultados de búsqueda. Todos los resultados duplicados en ese campo se eliminan de los resultados de búsqueda. Por ejemplo, si para <code>sp_dedupe_field=title </code>, solo se muestra el resultado superior de un título determinado en los resultados de búsqueda (no hay dos resultados que tengan un contenido de campo de título idéntico). Para los campos de tipo multivalor (lista de permitidos), se utiliza todo el contenido del campo para la comparación. Solo se puede especificar un campo. No se permite un "calificador de tabla" en el nombre del campo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_e= number </code> </p> </td> 
   <td colname="col4"> <p>Especifica que la expansión automática de caracteres comodín debe realizarse para cualquier palabra de la cadena de consulta con más de caracteres numéricos. En otras palabras, <code>sp_e=5 </code> especifica que las palabras con 5 o más caracteres, como "consulta" o "número", deben expandirse con el carácter comodín '*', lo que hace que la búsqueda sea equivalente a la búsqueda de "consulta*" o "número*". Las palabras con menos caracteres no se expanden, por lo que la búsqueda de "palabra" no tendría expansión automática de caracteres comodín. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <code>sp_e_#= number </code> </p> </td> 
   <td colname="col4"> <p>Especifica que la expansión automática de caracteres comodín tiene lugar para cualquier palabra de la cadena de consulta <code>sp_q_# </code> correspondiente con más de caracteres numéricos. En otras palabras, <code>sp_e_2=5 </code> especifica que las palabras con cinco o más caracteres en la cadena de consulta <code>sp_q_2 </code>, como "consulta" o "número", deben expandirse con el carácter comodín ' <code>* </code>', lo que hace que la búsqueda sea equivalente a la búsqueda de "consulta*" o "número*". Las palabras con menos caracteres no se expanden, por lo que una búsqueda de "palabra" en <code>sp_q_2 </code> no tendría expansión automática de comodín. </p> </td> 
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
   <td colname="col3"> <p> <code>sp_f= string </code> </p> </td> 
   <td colname="col4"> <p>Especifica el conjunto de caracteres de las cadenas de parámetros de consulta (como <code>sp_q </code>). Esta cadena siempre debe coincidir con el conjunto de caracteres de la página que contiene el formulario de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>Define una tabla de datos lógica que consta de los campos dados. Por ejemplo, una tabla denominada "elementos" que consta de los campos "color", "tamaño" y "precio" se definiría de la siguiente manera: </p> <p> <code>sp_field_table=items:color,size,price </code> </p> <p>Las tablas lógicas son más útiles junto con los campos que tienen activada la opción "Listas de permitidos" (en <span class="uicontrol"> Configuración </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Definiciones </span>). Todos los parámetros de CGI y las etiquetas de plantilla que toman un nombre de campo como valor pueden especificar opcionalmente un nombre de tabla seguido de "." antes del nombre del campo (por ejemplo, <code>sp_x_1=tablename.fieldname </code>). </p> <p>Por ejemplo, para realizar una búsqueda de documentos que contengan uno o más elementos "rojos" de tamaño "grande" (donde los elementos se representan como filas paralelas de metadatos), puede utilizar lo siguiente: </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p></td><td colname="col4"><p></p><p></p><p><code>sp_i=1 </code><code>sp_i=2 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_k= string </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_l= string </code></p></td><td colname="col4"><p><code>sp_q </code><code>string </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_literal= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_literal=1 </code></p><p><code>sp_literal=0 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_m= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_n= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_not_found_page= url </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p= any/all/phrase </code></p></td><td colname="col4"><p><code>any </code><code>all </code><code>phrase </code></p><p><code>phrase </code><code>all </code><code>sp_p </code></p><p></p><p></p><p><code>sp_p </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p_#= any/all/phrase </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>any </code><code>all </code><code>phrase </code></p><p><code>all </code><code>phrase </code><code>sp_p_# </code><code>any </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>exact </code><code>equivalent </code><code>compatible </code><code>sp_p </code><code>exact </code><code>sp_p </code><code>all </code><code>phrase </code><code>equivalent </code><code>sp_pt </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt_#= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>exact </code><code>equivalent </code><code>exact </code><code>compatible </code><code>sp_p_# </code><code>exact </code><code>sp_p_# </code><code>equivalent </code><code>sp_pt_# </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q= string </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_#= text </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_q_1 </code><code>sp_q_16 </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_day= integer value </code></p><p><code>sp_q_month= integer value </code></p><p><code>sp_q_year= integer value </code></p><p><code>sp_q_day_#= integer value </code></p><p><code>sp_q_month_#= integer value </code></p><p><code>sp_q_year_#= integer value </code></p></td><td colname="col4"><p><code>sp_q_day </code><code>sp_q_month </code><code>sp_q_year </code><code>sp_q </code></p><p><code># </code><code>sp_q_day_6 </code><code>sp_q_6 </code></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p><p><code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p></td><td colname="col4"><p><code>sp_q_location </code><code>sp_q_location_# </code><code># </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_max_relevant_distance= <i>value</i> </code></p><p><code> sp_q_max_relevant_distance_#= <i>value</i> </code></p></td><td colname="col4"><p><code>sp_q_max_relevant_distance </code><code>sp_q_max_relevant_distance_# </code><code># </code></p><p><code>sp_q_max_relevant_distance </code></p><p><code>sp_q_max_relevant_distance_# </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p><p></p></td><td colname="col03"><p></p><p></p></td><td colname="col3"><p><code> sp_q_min_day=<i>integer value</i> </code></p><p><code> sp_q_min_month=<i>integer value</i> </code></p><p><code> sp_q_min_year=<i>integer value</i> </code></p><p><code> sp_q_max_day=<i>integer value</i> </code></p><p><code> sp_q_max_month=<i>integer value</i> </code></p><p><code> sp_q_max_year=<i>integer value</i> </code></p><p><code> sp_q_min_day_#=<i>integer value</i> </code></p><p><code> sp_q_min_month_#=<i>integer value</i> </code></p><p><code> sp_q_min_year_#=<i>integer value</i> </code></p><p><code> sp_q_max_day_#=<i>integer value</i> </code></p><p><code> sp_q_max_month_#=<i>integer value</i> </code></p><p><code> sp_q_max_year_#=<i>integer value</i> </code></p></td><td colname="col4"><p><code>sp_q_min_day </code><code>sp_q_min_month </code><code>sp_q_min_year </code><code>sp_q_max_day </code><code>sp_q_max_month </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_day_6 </code><code>sp_q_6 </code></p><p></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_min= value </code></p><p><code>sp_q_max= value </code></p><p><code>sp_q_min_#= value </code></p><p><code>sp_q_max_#= value </code></p><p><code>sp_q_exact_#=value </code></p></td><td colname="col4"><p><code>sp_q_min </code><code>sp_q_max </code><code>sp_q_exact </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_8 </code><code>sp_q_8 </code></p><p><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code></p><p><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_nocp= 1 or 0 </code></p><p><code>sp_q_nocp_#= 1 or 0 </code></p></td><td colname="col4"><p><code>0 </code></p><p><code>1 </code></p><p><code>sp_q_nocp </code><code>sp_q </code><code># </code><code>sp_q_nocp_8 </code><code>sp_q_8 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_required= 1 or 0 or -1 </code></p><p><code>sp_q_required_#= 1 or 0 or -1 </code></p></td><td colname="col4"><p></p><p><code>sp_q_required </code><code>sp_q </code></p><p><code># </code><code>sp_q_required_8 </code><code>sp_q_8 </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_referrer= url </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>ro </code></p><p></p><p><code>sp_ro=body:10 </code></p><p></p><p><code>sp_ro=body:9|title:9 </code></p><p><p><code>sp_ro=title:10 </code><code>title </code><code>sp_ro </code><code>sp_ro </code></p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_s= number </code></p></td><td colname="col4"><p></p><p><code>sp_s </code><code>sp_s=title </code><code>sp_s </code></p><p></p><p><code>sp_s </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code></p><p><code>sp_field_table </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sr= field </code></p></td><td colname="col4"><p><code>sp_sr </code></p><p><code>sp_sr </code><code>&lt;input type="hidden" name="sp_sr" value=""&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sfvl_field= string </code></p></td><td colname="col4"><p><code>search-field-value-list</code></p><p><code>sp_sfvl_field </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>search-field-value-list </code></p><p><code>dynamic-facet-field-count </code><code>dynamic-facet-field-count </code></p><p><code>sp_sfvl_df_count </code><code>dynamic-facet-field-count </code><code>sp_sfvl_df_count </code><code>sp_sfvl_df_count </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p><p><code>sp_sfvl_df_count </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_count </code></p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_staged= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_staged=1 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_start_day= number </code></p><p><code>sp_start_month= number </code></p><p><code>sp_start_year= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_suggest_q= number </code></p></td><td colname="col4"><p><code>sp_suggest_q </code><code>sp_q[_#] </code></p><p><code>sp_suggest_q </code><code>sp_q </code></p><p><code>sp_suggest_q=1 </code><code>sp_q_1 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_t= string </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_trace= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_stage=1 </code></p><p></p><p><p></p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_w= <i>sound-alike-enable</i> </code></p><p><code> sp_w_control=<i>sound-alike-control</i> </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p><p></p><code>sp_w_control </code></p><p><code>sp_w_control=0 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control=1 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control </code><code>sp_w </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x= field </code></p></td><td colname="col4"><p><code>sp_q </code><code>sp_x </code></p><p></p><p><code>sp_x </code></p><p></p><p><code>sp_x=any </code><code>sp_x </code></p><p><code>sp_x </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x_#= field-name </code></p></td><td colname="col4"><p><code>sp_q_# </code><code> # </code><code>sp_x_8 </code></p><p><code>sp_x_# </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code></p><p><code>sp_x </code><code>sp_x_# </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code></p></td></tr></tbody></table>

## Un ejemplo típico del uso de parámetros CGI de búsqueda back-end {#section_260012BBC2514CC9A8E02E53DE8B41EE}

Las siguientes consultas de vínculos inician una búsqueda utilizando &quot;Música&quot; como consulta de búsqueda y utilizan todos los parámetros predeterminados. Tenga en cuenta que la dirección URL está dividida en dos líneas para facilitar la lectura. En su HTML, este vínculo debe estar en una línea.

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

Normalmente, se deben usar parámetros predeterminados al iniciar una búsqueda. De este modo, se muestra la primera página, se ordena por relevancia y permite al cliente elegir otras páginas y otras opciones. Si el formulario de búsqueda del sitio incluye opciones para las colecciones, pase el nombre de la colección como parámetro.

## Un ejemplo detallado del uso de parámetros CGI de búsqueda back-end {#section_5FA3C620D5124FB2AB28857F8D8473F6}

Las siguientes consultas de formulario muestran `25` resultados que comienzan por el resultado `10`. No se muestran los resúmenes, el criterio de ordenación es por fecha y se utiliza la colección denominada `support`. Solo se devuelven los documentos con fecha de los últimos 30 días.

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

