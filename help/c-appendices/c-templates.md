---
description: 'null'
seo-description: 'null'
seo-title: Plantillas
solution: Target
title: Plantillas
topic: Appendices,Site search and merchandising
uuid: 78299032-dc23-4dfe-b68f-cd57b2b6d7d8
translation-type: tm+mt
source-git-commit: ca4156f80d7dbb85d2d56b6caf7c0f560299d86e
workflow-type: tm+mt
source-wordcount: '15139'
ht-degree: 2%

---


# Plantillas{#templates}

## Plantillas {#concept_A5CFB6BD805D49459A96219AF1B17842}

## Etiquetas de plantilla de presentación {#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64}

Una lista de las etiquetas y los atributos de búsqueda y comercialización del sitio para las plantillas de presentación.


Una plantilla de presentación es un archivo HTML que incluye etiquetas de plantilla de presentación que define la búsqueda y comercialización del sitio. Estas etiquetas indican el formato de los resultados de búsqueda que ven los clientes.

Consulte [Acerca de las plantillas](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

Puede seleccionar entre los siguientes grupos de etiquetas de presentación:

* [Declaraciones](../c-appendices/c-templates.md#section_82C5CA734D2941EB858FEFE3B695D2EC)
* [Resultados](../c-appendices/c-templates.md#section_06F249C9F6AE4B0F8C32117E19DCC905)
* [Facetas](../c-appendices/c-templates.md#section_EA4C5678D5864B89BAB4D0DFE62A4624)
* [Ruta de exploración](../c-appendices/c-templates.md#section_9B39B71FA6EC49FA8D88AD8A3BA987F7)
* [Menús](../c-appendices/c-templates.md#section_1D489ADF041F4351A66E5D5742125CA8)
* [Pagenav](../c-appendices/c-templates.md#section_2EE397635C514BBC8D668278EA314F35)
* [Búsquedas recientes](../c-appendices/c-templates.md#section_8CD907521F584257B475595B01A5964B)
* [Quizás quiso decir](../c-appendices/c-templates.md#section_C1EB3B9D8E1242798A6E04609D1E3543)
* [Autocompletar](../c-appendices/c-templates.md#section_897316BEE1454E839A56B565CA4AF018)
* [Tienda](../c-appendices/c-templates.md#section_A33E25DB5E67404A823BD9618665B773)
* [Zonas](../c-appendices/c-templates.md#section_B9B3179E000C42D492E1541F2FE44CB5)
* [Indicadores de bucle](../c-appendices/c-templates.md#section_387322CA0AA843A2ACF2795C328673E9)
* [Idioma varios](../c-appendices/c-templates.md#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C)

## Declaraciones {#section_82C5CA734D2941EB858FEFE3B695D2EC}

Las declaraciones son etiquetas de declaración guiada especiales que se pueden definir en la parte superior de una plantilla de presentación de nivel superior. Se omiten todas las declaraciones posteriores, incluidas las declaraciones de las plantillas incluidas.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-content-type-header content="content-type"&gt; </span> </p> </td> 
   <td colname="col2"> <p>De forma predeterminada, la plantilla de presentación se devuelve con un tipo MIME de text/html. Puede cambiar qué tipo de contenido se utiliza con esta etiqueta. </p> <p>Declare esta etiqueta lo más alto posible en la plantilla de presentación. No agregue otro texto en la misma línea con esta etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml-declare [charset="charset"]&gt; </span> </p> </td> 
   <td colname="col2"> <p> Si devuelve XML, puede utilizar esta etiqueta para crear la declaración XML. Convierta esta etiqueta en la primera línea de la plantilla de presentación. Cuando se utiliza esta etiqueta, el tipo de contenido se establece automáticamente en text/xml, a menos que se sobrescriba con <span class="codeph"> &lt;guided-content-type-header&gt; </span> en la primera línea. Si no especifica un charset, el valor predeterminado es UTF-8. Esta etiqueta tiene el siguiente resultado en el documento XML: </p> <p> <span class="codeph"> &lt;?xml version="1.0" encoding="charset-name" standalone="yes" ?&gt; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Resultados {#section_06F249C9F6AE4B0F8C32117E19DCC905}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-results [gsname="searchname"]&gt;&lt;/guided-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>La etiqueta guided-results define los límites de un bucle de resultados. Se puede acceder a cualquier conjunto de resultados especificando un <span class="codeph"> atributo gsname </span> . Si no se proporciona <span class="codeph"> gsname </span> , se muestran los resultados de búsqueda predeterminados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-link [gsname="fieldname"] [Enable="value"]+&gt;&lt;/guided-result-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Para crear un vínculo a un resultado determinado, utilice la <span class="codeph"> etiqueta guided-result-link </span> . Al definir un atributo <span class="codeph"> gsname </span> , puede utilizar un campo del índice en lugar de la etiqueta estándar "loc" que hace referencia a la "dirección URL de búsqueda". También se pueden pasar otros atributos, como clase y destinatario, que se muestran en la etiqueta de anclaje resultante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng 1/31/13--> <span class="codeph"> &lt;guided-result-img gsname="fieldname" [Enable="value"]+&gt; </span> </p> </td> 
   <td colname="col2"> <p>La etiqueta <span class="codeph"> &lt;guided-result-img&gt; </span> ayuda a crear etiquetas de imagen en lugar de incrustar variables dentro de una etiqueta <span class="codeph"> img </span> sin procesar. </p> <p>Especifique el campo que se usará para la ruta de la imagen en el atributo <span class="codeph"> gsname </span> . El resultado es una <span class="codeph"> etiqueta img </span> con cualquier atributo HTML estándar que haya definido y pasado por ella. Por lo tanto, el siguiente ejemplo: </p> <p> <code class="syntax html"> &lt;guided-result-img&nbsp;gsname="thumbnail" 
      &nbsp;class="thumb"&nbsp;border="0"/&gt; </code> </p> <p>becomes: </p> <p> <code class="syntax html"> &lt;img&nbsp;src="prod8172.jpg"&nbsp;class="thumb" 
      &nbsp;border="0"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 1/31/13; search-eng version does not have [escape...] Added ijson on 8/28/2015--> <span class="codeph"> &lt;guided-result-field gsname="fieldname" [escape="html|url|js|json|ijson|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p> Cualquier parte de la información que se va a presentar en los resultados se muestra como una etiqueta <span class="codeph"> &lt;guided-result-field&gt; </span> (excepto cuando se utilizan etiquetas de generación automática como la <span class="codeph"> &lt;guided-result-img&gt; </span> ). </p> <p>Especifique el nombre del campo de índice de búsqueda en <span class="codeph"> gsname </span>. La cadena exacta que se pasa se muestra en la plantilla. </p> <p>Puede especificar una opción de escape si desea que este campo se escape de forma distinta a la especificada en la plantilla de transporte. </p> <p>Esta codificación se aplica sobre cualquier codificación especificada en la plantilla de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <span class="codeph"> &lt;guided-if[-not]-result-field gsname="field-name&gt;&lt;/guided-if-result-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas condicionales es verdadero si hay contenido en el campo específico que se va a mostrar. Si no hay contenido, la condición es false. Puede utilizar las etiquetas para decidir si el HTML circundante se muestra o no si no existe un valor, o si se muestra una imagen diferente, etc. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"&nbsp;/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"&nbsp;/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <code> &lt;guided-if[-not]-result-wrap&gt; 
      &lt;guided-else-result-wrap&gt; 
      &lt;/guided-if[-not]-result-wrap&gt; </code> </p> </td> 
   <td colname="col2"> <p>Al mostrar los resultados en columnas, esta etiqueta se utiliza para identificar si el resultado actual marca el final de una columna. </p> <p>Cuando la condición booleana es verdadera, se agrega HTML al final del resultado para finalizar la fila y inicio una nueva. Cuando es la última, no se inicia una nueva fila. </p> <p>Consulte <span class="codeph"> &lt;guided-if-not-last&gt; </span> para obtener más información sobre esa etiqueta. </p> <p> <code class="syntax html"> &lt;guided-if-result-wrap&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&lt;/guided-if-result-wrap&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-results-found [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve un 1 si la solicitud de búsqueda back-end devolvió resultados y 0 si no lo hizo. Si no se especifica <span class="codeph"> gsname </span> , la etiqueta asume la búsqueda principal. Esta etiqueta es útil para pasar lógica a rutinas de JavaScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-total [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve el número total de resultados en el conjunto de resultados especificado. Supone la búsqueda predeterminada cuando no se da <span class="codeph"> gsname </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-lower [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve el número de resultado del resultado inferior de la página para el conjunto de resultados especificado. Supone la búsqueda predeterminada cuando no se da <span class="codeph"> gsname </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-results-top [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve el número de resultado del resultado superior de la página para el conjunto de resultados especificado. Supone la búsqueda predeterminada cuando no se da <span class="codeph"> gsname </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-results-found&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Muestra el contenido cuando se encuentran los resultados. O bien, no muestra ningún HTML de resultados cuando no se encuentran los resultados. </p> <p> <code class="syntax html"> &lt;guided-if-results-found&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-results&nbsp;gsname="products"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-results&gt; 
      &lt;guided-else-results-found&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;No&nbsp;results&nbsp;were&nbsp;found. 
      &lt;/guided-if-results-found&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-title/&gt; </span> </p> </td> 
   <td colname="col2"> <p>La etiqueta <span class="codeph"> &lt;guided-result-title&gt; </span> proporciona el valor del campo de plantilla de transporte de título especificado con la etiqueta <span class="codeph"> &lt;title&gt; </span> Transport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-description/&gt; </span> </p> </td> 
   <td colname="col2"> <p>La etiqueta <span class="codeph"> &lt;guided-result-description&gt; </span> proporciona el valor del campo de plantilla de transporte de descripción especificado con la etiqueta de transporte <span class="codeph"> &lt;description&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-loc/&gt; </span> </p> </td> 
   <td colname="col2"> <p>La etiqueta &lt; <span class="codeph"> guided-result-loc&gt; </span> da valor al campo de plantilla de transporte loc especificado con la etiqueta de transporte <span class="codeph"> &lt;loc&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-result-field&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>True si hay contenido en el campo específico que se va a mostrar. Si no hay contenido, la condición es false. Utilice las etiquetas para decidir si se muestra o no el HTML circundante si no existe un valor, o si se muestra una imagen diferente, etc. </p> <p> <code class="syntax html"> &lt;guided-if-result-field&nbsp;gsname="thumbnail"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-result-img&nbsp;gsname="thumbnail"&nbsp;class="thumb"/&gt; 
      &lt;guided-else-result-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;img&nbsp;src="nothumb.jpg"&nbsp;class="nothumb"/&gt; 
      &lt;/guided-if-result-field&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table gsname="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta proporciona un bucle a través de la tabla de atributos definida en la plantilla de transporte con <span class="codeph"> &lt;attribute_table&gt; </span> etiqueta de transporte. Hay <span class="codeph"> &lt;guided-result-attribute-table-field&gt; </span> etiqueta para mostrar valores de campo de tabla de atributos. También es posible utilizar una etiqueta <span class="codeph"> de campo de resultados guiados sin formato </span> dentro del bucle para mostrar otros campos de resultados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-result-attribute-table-field gsname="fieldname" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Muestra el campo de tabla de atributos tal como se define en la plantilla de transporte. </p> <p> 

    ...
    
    &amp;lt;ul&amp;gt;
    
    &amp;lt;guided-result-attribute-table&amp;nbsp;gsname=&quot;downloads&quot;&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;lt;li&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp; nbsp;&amp;nbsp;&amp;lt;a&amp;nbsp;href=&quot;&amp;lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_link&quot;&amp;nbsp;/&amp;gt;&quot;&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;nbsp;nbsp;nbsp;nbsp;nbsp;sp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;guided-result-attribute-table-field&amp;nbsp;gsname=&quot;download_title&quot;&amp;nbsp;/&amp;gt;
    &amp;nbsp;&amp; nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/a&amp;gt;&amp;nbsp;(&amp;lt;guided-result-field&amp;nbsp;gsname=&quot;title&quot;/&amp;gt;)
    &amp;nbsp;&amp;lt;/li&amp;gt;
    &amp;lt;/guided-result-attribute-table&amp;gt;
    
    &amp;lt;/ul&amp;gt;
    
    ...
    
    &amp;lt;/guided-results&amp;gt; &lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release in October 2014--> <span class="codeph"> &lt;guided-trace [gsname="searchname"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae la información de seguimiento encontrada dentro de los datos de seguimiento dentro de la sección general de la salida de datos JSON por la plantilla de transporte para la búsqueda dada. </p> <p>Si no se proporciona ningún nombre de búsqueda, <span class="codeph"> se </span> asume el valor predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30, 2014)--> <span class="codeph"> &lt;guided-result-trace/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae el contenido JSON encontrado en los resultados &gt; rastrea información de la salida de datos JSON por la plantilla de transporte para el resultado de búsqueda actual. </p> <p>Esta etiqueta solo es válida dentro del bucle <span class="codeph"> &lt;guided-results&gt;&lt;/guided-results&gt; </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facetas {#section_EA4C5678D5864B89BAB4D0DFE62A4624}

Las facetas son componentes de navegación que permiten explorar en profundidad los resultados de búsqueda. Puede utilizar las etiquetas facetas para mostrar varias facetas en la plantilla de presentación. Las facetas se hacen referencia por su nombre.

Consulte [Acerca de las facetas](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Consulte [Acerca de Barra de faceta](../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB).

Consulte [Acerca de las facetas](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)dinámicas.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 02/27/2014--> <span class="codeph"> &lt;guided-dynamic-facets&gt;&lt;/guided-dynamic-facets&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--NEW 2/2/2014--> <p>Contexto de bucle para cualquier faceta dinámica para una búsqueda determinada. </p> <p>La etiqueta de plantilla de presentación <span class="codeph"> &lt;guided-facet&gt; </span> se edita para que el atributo gsname se proporcione automáticamente en el contexto de bucle <span class="codeph"> &lt;guided-dynamic-facets&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-display-name gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la etiqueta de visualización de la faceta. </p> <p>Si la faceta utiliza la etiqueta <span class="codeph"> &lt;display-name&gt; </span> en la plantilla de transporte, el contenido de esa etiqueta se convierte en la etiqueta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-rail&gt;&lt;/guided-facet-rail&gt; </span> </p> </td> 
   <td colname="col2"> <p> Define una sección de la plantilla de presentación que se utiliza como patrón de repetición para cada faceta del carril de facetas. </p> <p> Cada faceta que pertenece al carril de facetas utiliza esta sección para evaluar su salida. </p> <p>A continuación se muestra un ejemplo de carril de facetas: </p> <p> <code class="syntax html"> &lt;guided-facet-rail&gt; 
      &nbsp;&nbsp;&lt;guided-facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-display-name/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;... 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet&gt; 
      &nbsp;&nbsp;&lt;/guided-facet-rail&gt; </code> </p> <p>Tenga en cuenta que las etiquetas siguientes no necesitan el atributo <span class="codeph"> gsname </span> cuando se encuentra dentro de la etiqueta <span class="codeph"> &lt;guided-facet-rail&gt; </span> , ya que el valor se determina de forma dinámica en el momento de la búsqueda y se sustituye correctamente: </p> 
    <ul id="ul_5B5ACAFD2B8848DDB27471AB9DA7BE6E"> 
     <li id="li_5A07E78D51FE4708879DD742C877FFFF">guided-facet </li> 
     <li id="li_B875DCACD7AB4FC890A456A6939AB657">guided-facet-display-name </li> 
     <li id="li_B70450749E864DE7BA401E3CD6EF5EB3">guided-facet-total-count </li> 
     <li id="li_DECDF5EF6FF7454F86C236D322F2BFEA">guided-facet-undo-link </li> 
     <li id="li_176949227AC14E8CA643A419E10F7B5A">guided-facet-undo-path </li> 
     <li id="li_B32D981281744462BC680F6EFEAC0069">guided-facet-Behavior </li> 
    </ul> <p>Los criterios de ordenación de la <span class="wintitle"> página Barra de facetas </span> determinan la posición de las facetas. Puede elegir el orden en la lista desplegable Ordenar métodos de facetas. </p> <p> 
     <!--NEW 02/27/2014-->Esta etiqueta puede aceptar opcionalmente un valor de atributo gsname de <span class="codeph"> _dynamic_facets </span>, que proporciona un contexto de bucle para cualquier faceta dinámica de esta búsqueda. Este carril de facetas predefinido también está expuesto en la interfaz de usuario de reglas comerciales para la acción <span class="codeph"> de la faceta X en el carril de facetas '_dynamic_facets' a la posición Y </span>". </p> <p>Consulte <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">Acerca de Barra de faceta </a>. </p> <p>Consulte también <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Acerca de las facetas dinámicas </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match current search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet gsname=" <span class="varname"> facetname </span>" height=" <span class="varname"> 60px </span>" width=" <span class="varname"> 120px </span>"&gt;&lt;/guided-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Utilice la <span class="codeph"> etiqueta de faceta guiada </span> para definir un área dentro de la cual todas las etiquetas de facetas se relacionan con una faceta específica. Esta etiqueta es también una etiqueta booleana que oculta todo el contenido si no hay valores en la faceta. En ese caso, no tiene sentido obtener los valores de faceta). </p> <p>Los atributos de altura y ancho son opcionales y las dimensiones se especifican en píxeles (px). El Generador de reglas visuales (VRB) utiliza estos dos atributos y muestra un cuadro de puntos como un marcador de posición interactivo cuando la faceta está oculta. </p> <p> Cuando el nombre para mostrar está en la faceta y la faceta está oculta, el nombre también se oculta. Sin embargo, si el nombre está fuera de la faceta, puede ocultar el nombre solo si <span class="codeph"> la etiqueta de zona </span> o una etiqueta <span class="codeph"> guiada-si-faceta-visible </span> está envuelta alrededor de ella. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-long [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-long&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta condicional es verdadera cuando el número de valores de faceta está por encima del umbral de longitud definido en la configuración. Utilícelo para mostrar una faceta como un elemento de interfaz de usuario diferente (como una lista truncada o un cuadro de desplazamiento) cuando la lista sea demasiado larga. </p> <p> <code class="syntax xml"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-option&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/select&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>También puede utilizar esta condición fuera del contexto de un bloque con faceta guiada con nombre <span class="codeph"></span> haciendo referencia a una faceta específica directamente mediante el uso del atributo <span class="codeph"> gsname </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-selected [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-selected&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta condicional es verdadera cuando se hace clic en la faceta al menos una vez y se selecciona un valor de faceta. Se utiliza para mostrar u ocultar las etiquetas HTML o gs en función de si se ha hecho clic en una faceta. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>También puede utilizar esta condición fuera del contexto de un bloque con faceta guiada con nombre <span class="codeph"></span> haciendo referencia a una faceta específica directamente mediante el uso del atributo <span class="codeph"> gsname </span> . </p> <p> <code> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-if[-not]-facet-single [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-single&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta condicional es verdadera cuando solo hay un valor de faceta. Utilice la etiqueta para cambiar la visualización de la faceta cuando no tenga capacidad para refinar los resultados. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>También puede utilizar esta condición fuera del contexto de un bloque con faceta guiada con nombre <span class="codeph"></span> haciendo referencia a una faceta específica directamente mediante el uso del atributo <span class="codeph"> gsname </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Added 7/15/2014--> <span class="codeph"> &lt;guided-if[-not]-facet-multiselect [gsname="facetname"]&gt;&lt;/guided-if[-not]-facet-multiselect&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta condicional es verdadera cuando la faceta es de selección múltiple. Utilice la etiqueta para cambiar la visualización de la faceta dentro de las etiquetas <span class="codeph"> &lt;guided-facet-rail&gt; </span> o <span class="codeph"> &lt;guided-dynamic-facets&gt; </span> . </p> <p> 

    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;nbsp;&amp;lt;guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;guided-else-facet-multiselect&amp;gt;
    &amp;nbsp;...
    &amp;nbsp;&amp;lt;/guided-if-facet-multiselect&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;...
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet&amp;gt;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;lt;/guided-facet-rail&amp;gt; &lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-values [gsname=" <span class="varname"> facetname </span>"]&gt;&lt;/guided-facet-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Es la etiqueta del repetidor de bucle de valor de faceta. Puede definirlo dentro del contexto de un bloque con faceta guiada <span class="codeph"> con nombre </span> , en cuyo caso puede omitir el <span class="codeph"> <span class="varname"> gsname </span> </span>. O bien, puede definirlo fuera de cualquier <span class="codeph"> bloque de faceta guiada </span> , pero requeriría el <span class="codeph"> atributo <span class="varname"> gsname </span> </span> para identificar qué conjunto de valores de faceta se muestran. </p> <p>También puede utilizar esta etiqueta para mostrar los valores de faceta fuera del contexto de un bloque con faceta guiada <span class="codeph"> con nombre </span> . Puede hacer referencia a una faceta específica directamente mediante el <span class="codeph"> atributo <span class="varname"> gsname </span></span> . </p> <p> <code class="syntax html"> &lt;script&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;registerFacetValues('category',&nbsp;'&lt;guided-facet-values&nbsp;gsname="category"&gt;&lt;guided-facet-value/&gt;,&lt;/guided-facet-values&gt;'); 
      &lt;/script&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-value [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae la cadena del valor de faceta actual. </p> <p>De forma predeterminada, el valor es HTML escaped. Puede utilizar la opción de escape para cambiar la forma en que se escapa el valor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--In search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-count/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae el número de resultados que coinciden con el valor de faceta actual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW, brought in from search-eng version, 1/31/13--> <span class="codeph"> &lt;guided-facet-value-link [Enable="value"]+&gt;&lt;/guided-facet-value-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un vínculo alrededor de la cadena de valor de faceta en el que el visitante del sitio puede hacer clic. La ruta se genera automáticamente para reducir los resultados según el valor de faceta actual. Admite pasar cualquier atributo directamente a la etiqueta de anclaje. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-value-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-value-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <code> &lt;guided-if-facet-value-selected&gt; 
      &lt;guided-else-facet- 
      value-selected&gt; 
      &lt;/guided-if-facet-value-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Cambia la visualización del valor de faceta cuando está seleccionado. Si ya se ha elegido, en la mayoría de los casos ya no es vinculable. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value/&gt;&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt;&nbsp;&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> 

    &amp;lt;/guided-if[-not]-facet-value-fantasma&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Cambia la visualización del valor de faceta cuando es un valor fantasma. Cuando un valor de faceta es un valor fantasma, suele mostrarse en cursiva para indicar que falta el valor o que está en "fantasma". </p> <p>El siguiente fragmento de código es un ejemplo de un bloque de facetas: </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;b&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/b&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;i&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(0)&lt;/i&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="link"&gt;&lt;guided-facet-value&nbsp;/&gt;&lt;/guided-facet-link&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;) 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-ghost&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-value-selected&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version 1/31/13--> <span class="codeph"> &lt;guided-facet-undo-link gsname=" <span class="varname"> facetname </span>"&gt;&lt;/guided-facet-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Muestra un vínculo de deshacer para una faceta determinada. Si hay facetas de selección múltiple, este vínculo anula la selección de todos los valores de faceta determinados. Póngale un nombre a la faceta. Si la faceta no está seleccionada actualmente, el vínculo es la ruta actual. </p> <p>El siguiente es un ejemplo del uso de esta etiqueta: </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-undo-link&nbsp;gsname="category"&gt;Undo&nbsp;Category&lt;/guided-facet-undo-link&gt; 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-long [gsname="facetname"]&gt; 
      &lt;guided-else-facet-long&gt;&lt;/guided-if-facet-long&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta condicional es verdadera cuando el número de valores de faceta está por encima del umbral de longitud definido en la configuración. Utilícelo para mostrar una faceta como un elemento de interfaz de usuario diferente (como una lista truncada o un cuadro de desplazamiento) cuando la lista sea demasiado larga. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="long_facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;div&nbsp;class="facet"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-long&gt; 
      &nbsp;&lt;/guided-facet&gt; </code> </p> <p>También puede utilizar esta condición fuera del contexto de un bloque con faceta guiada con nombre <span class="codeph"> , </span> haciendo referencia a una faceta específica directamente mediante el uso del <span class="codeph"> atributo <span class="varname"> gsname </span> </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-long&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;very&nbsp;long! 
      &lt;/guided-if-facet-long&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-selected [gsname="facetname"]&gt; 
      &lt;guided-else-facet-selected&gt;&lt;/guided-if-facet-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta condicional es verdadera cuando se hace clic en la faceta al menos una vez y se selecciona un valor de faceta. Se puede utilizar para mostrar u ocultar etiquetas HTML o gs en función de si se hace clic en una faceta. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This&nbsp;facet&nbsp;has&nbsp;been&nbsp;selected.&nbsp;&nbsp;You&nbsp;can&nbsp;no&nbsp;longer&nbsp;refine&nbsp;it. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-selected&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-selected&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>También puede utilizar esta condición fuera del contexto de un bloque con faceta guiada con nombre <span class="codeph"></span> haciendo referencia a una faceta específica directamente mediante el uso del atributo <span class="codeph"> gsname </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-selected&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The&nbsp;category&nbsp;facet&nbsp;is&nbsp;selected! 
      &lt;/guided-if-facet-selected&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-single [gsname="facetname"]&gt; 
      &lt;guided-else-facet-single&gt;&lt;/guided-if-facet-single&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta condicional es verdadera cuando solo hay un valor de faceta. Se puede utilizar para cambiar la visualización de la faceta cuando no tiene capacidad para refinar los resultados. </p> <p> <code class="syntax html"> &lt;guided-facet&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Facet&nbsp;is&nbsp;not&nbsp;refinable. 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-else-facet-single&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-facet-single&gt; 
      &lt;/guided-facet&gt; </code> </p> <p>También puede utilizar esta condición fuera del contexto de un bloque con faceta guiada con nombre <span class="codeph"> , </span> haciendo referencia a una faceta específica directamente mediante el uso del <span class="codeph"> atributo <span class="varname"> gsname </span> </span> . </p> <p> <code class="syntax html"> &lt;guided-if-facet-single&nbsp;gsname="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;There&nbsp;is&nbsp;only&nbsp;one&nbsp;value&nbsp;in&nbsp;the&nbsp;category&nbsp;facet! 
      &lt;/guided-if-facet-single&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-has-values [gsname="facetname"]&gt; 
      &lt;guided-else-facet-has-values&gt;&lt;/guided-if-facet-has-values&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta condición permite comprobar si la faceta especificada tiene algún valor. Puede utilizarla para mostrar otra faceta en lugar de una vacía. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-total-count gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae el número total de resultados que están dentro de una faceta determinada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value gsname=" <span class="varname"> valor de faceta personalizado asociado </span>" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae la cadena de un valor que está asociado con la faceta. Puede tener 0 o más campos asociados a una faceta. No es habitual tener campos asociados y, para ello, puede configurar la plantilla de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-facet-value gsname=" <span class="varname"> valor de faceta personalizado asociado </span>"/&gt;&lt;guided-else-facet-value&gt;&lt;/guided-if-facet-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Comprueba si el valor de faceta tiene un valor de campo asociado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-link [Enable=" <span class="varname"> value </span>"]+&gt;&lt;/guided-facet-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un vínculo alrededor de la cadena de valor de faceta en el que el cliente puede hacer clic. La ruta se genera automáticamente para reducir los resultados según el valor de faceta actual. Admite pasar cualquier atributo directamente a la etiqueta de anclaje. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;class="facetlink"&gt;&lt;guided-facet-value/&gt;&lt;/guided-facet-link&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-path [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea su propio vínculo a un valor de faceta. </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-lt/&gt;a&nbsp;href="&lt;guided-facet-value-path/&gt;"&lt;guided-gt/&gt;&lt;guided-facet-value/&gt;&lt;/a&gt; 
      &lt;/guided-facet-values&gt; </code> </p> <p>De forma predeterminada, el valor es URL escapada. Sin embargo, puede agregar otra capa de codificación especificando qué modo de escape desea utilizar mediante el parámetro escape. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-children&gt;&lt;/guided-facet-value-children&gt; </span> </p> </td> 
   <td colname="col2"> <p>A medida que <span class="codeph"> &lt;guided-facet-values&gt; </span> se repite por cada valor de faceta, esta etiqueta repite todos los valores secundarios de una faceta anidada. Dentro de esta etiqueta, utilice las etiquetas de facetas típicas para crear vínculos, crear vínculos de deshacer y mostrar valores de facetas. Esta etiqueta debe estar dentro de <span class="codeph"> &lt;guided-facet-values&gt; </span> porque no hay bucles anidados. </p> <p>A continuación se muestra un ejemplo de uso de esta etiqueta: </p> <p> <code class="syntax html"> &lt;guided-facet-values&gt; 
      &nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&lt;guided-if-facet-value-has-children&gt; 
      &nbsp;&nbsp;&nbsp;&lt;guided-facet-value-children&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-facet-link&nbsp;title='&lt;guided-facet-value&nbsp;/&gt;'&gt;&lt;guided-facet-value&nbsp;/&gt;&nbsp;(&lt;guided-facet-count&nbsp;/&gt;)&lt;/guided-facet-link&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-facet-value-children&gt; 
      &nbsp;&nbsp;&lt;/guided-if-facet-value-has-children&gt; 
      &lt;/guided-facet-values&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-has-children&gt; 
      &lt;guided-else-facet- 
      value-has-children&gt; 
      &lt;/guided-if-facet-value-has-children&gt; </code> </p> </td> 
   <td colname="col2"> <p>Comprueba si el valor de faceta actual tiene valores secundarios. Se recomienda usar antes de usar las etiquetas <span class="codeph"> &lt;guided-facet-value-children&gt; </span> . La cláusula "else" es opcional. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-over-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-over-length-threshold&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Determina si el valor de faceta actual dentro del bucle facet-values está por encima del umbral de longitud. Normalmente se utiliza para mostrar solo valores por debajo del umbral en una faceta larga (a menos que el usuario haya seleccionado previamente un vínculo "Ver más" que se muestra debajo de la faceta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;guided-else[-not]-facet-value-equals-length-threshold&amp;gt;
    
    &amp;lt;/guided-if[-not]-facet-value-equals-length-threshold&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Determina si el valor de faceta actual dentro del bucle facet-values es igual al umbral de longitud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-link&gt;&lt;/guided-facet-value-undo-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Muestra un vínculo de deshacer para un valor de faceta seleccionado determinado. Utilícelo para mostrar un vínculo de deshacer junto a un valor de faceta seleccionado. Debido a que este vínculo de deshacer sólo deshace ese valor seleccionado en particular, difiere de <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> que anula la selección de todos los valores seleccionados. </p> <p> <p>Nota:  Si la faceta no tiene un comportamiento de selección múltiple, los dos vínculos de deshacer tienen el mismo comportamiento. Es decir, la faceta solo puede tener un valor seleccionado. </p> </p> <p>Si la faceta no está seleccionada actualmente, el vínculo es la ruta actual. Utilice esta etiqueta únicamente dentro de un <span class="codeph"> bucle </span> guided-facet-values. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>30 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-value-undo-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cree su propio vínculo de deshacer valor de faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>31 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-undo-path gsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cree su propio vínculo de deshacer facetas. </p> <p> Similar a la etiqueta <span class="codeph"> &lt;guided-facet-undo-link&gt; </span> con la diferencia de que le proporciona la ruta sin procesar para crear su propio vínculo de deshacer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>32 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-facet-value-matches facetname="facetname" value="value"&gt;&lt;guided-else-facet-value-matches&gt; 
      &lt;/guided-if-facet-value-matches&gt; </code> </p> </td> 
   <td colname="col2"> <p>Muestre HTML condicionalmente cuando la faceta dada tenga el valor "value" seleccionado o único. Este conjunto de etiquetas se utiliza a menudo para mostrar una faceta en función del valor seleccionado en otra faceta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>33 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-facet-Behavigsname=" <span class="varname"> facetname </span>"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Determinar el comportamiento de una faceta, como normal, persistente o de selección múltiple. Resulta útil para los clientes que reciben resultados XML y desean cambiar dinámicamente la forma en que se muestra la faceta en función de su comportamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>34 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-facet[-not]-visible&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>El contenido que envuelve esta etiqueta se oculta o se muestra en función del estado de visibilidad de la faceta. Si una regla comercial oculta o revela la faceta directamente, cualquier contenido dentro de la faceta se oculta o se revela. No es necesario que estas etiquetas se ajusten alrededor de la faceta. </p> <p> Un uso común de esta etiqueta es ocultar el nombre para mostrar cuando el nombre está fuera de la faceta. Al ajustar esta etiqueta alrededor del nombre para mostrar, el nombre desaparecerá cuando la faceta esté oculta. </p> <p>Esta etiqueta reemplaza la zona y tiene muchos de los mismos beneficios de rendimiento que el uso de zonas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ruta de exploración {#section_9B39B71FA6EC49FA8D88AD8A3BA987F7}

Consulte [Acerca de las rutas de exploración](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb [gsname=" <span class="varname"> breadcrumbname </span>"]&gt;&lt;/guided-breadcrumb&gt; </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta de bucle de la ruta de exploración. Cualquier contenido entre las etiquetas de apertura y de cierre se repite para cada número de consulta del estado actual. </p> <p>Si <span class="codeph"> se omite <span class="varname"> gsname </span> </span> , se utiliza la ruta de exploración denominada "default". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-link [gsname="goto|remove|drop"] [attr="value"]+&gt;&lt;/guided-breadcrumb-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un vínculo en la ruta de exploración. El comportamiento predeterminado es el comportamiento "goto". Si el vínculo se comporta de forma diferente, utilice el <span class="codeph"> atributo <span class="varname"> gsname </span> </span> opcional para especificar "remove" o "drop". Cualquier atributo incluido en la etiqueta se pasa a la etiqueta de anclaje resultante. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&nbsp;gsname="remove"&nbsp;class="bc_link"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>La etiqueta value imprime el valor transformado de la iteración de ruta de exploración actual. Solo se utiliza en el contexto de un <span class="codeph"> bloque de </span> rutas guiadas. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-breadcrumb-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>La etiqueta genera una etiqueta para un valor de ruta de exploración que detalla qué faceta se seleccionó para generar ese elemento de ruta de exploración. Solo se utiliza en el contexto de un <span class="codeph"> bloque de </span> rutas guiadas. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;:&nbsp;&lt;guided-breadcrumb-value/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to search-eng version, 2/1/2013--> <code> &lt;guided-if-breadcrumb-label&gt; 
      &lt;guided-else- 
      breadcrumb-label&gt; 
      &lt;guided-if-breadcrumb-label /&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta condicional se utiliza para mostrar contenido condicionalmente si el valor actual de la ruta de exploración tiene una etiqueta. Solo se utiliza para mostrar etiquetas y contenido relacionado cuando existe una etiqueta. Solo se utiliza en el contexto de un <span class="codeph"> bloque de </span> rutas guiadas. </p> <p> <code class="syntax html"> &lt;guided-breadcrumb&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-label/&gt;: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-if-breadcrumb-label&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-breadcrumb-value/&gt;&lt;/guided-breadcrumb-link&gt; 
      &lt;/guided-breadcrumb&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-breadcrumb-path [gsname="goto|remove|drop"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Se utiliza para crear su propio vínculo de ruta de exploración. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Menús {#section_1D489ADF041F4351A66E5D5742125CA8}

Consulte [Acerca de los menús](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu gsname="menuname"&gt;&lt;/guided-menu&gt; </span> </p> </td> 
   <td colname="col2"> <p>Es la etiqueta del repetidor de bucle de valor de menú. Utilice el atributo <span class="codeph"> gsname </span> para identificar qué conjunto de elementos de menú se muestra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-link [Enable="value"]+&gt;&lt;/guided-menu-item-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Proporciona la dirección URL para refinar la búsqueda actual del elemento de menú. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-option [Enable="value"]+ /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Normalmente, un menú se muestra en un control de selección de una plantilla. Esta etiqueta facilita la construcción del control seleccionado, ya que genera el código HTML para generar la opción para el control seleccionado. </p> <p>Por ejemplo, el siguiente bloque de código: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &lt;guided-menu&nbsp;gsname="sort"&gt; 
      &lt;guided-menu-item-option/&gt; 
      &lt;/guided-menu&gt; 
      &lt;/select&gt; </code> </p> <p>Puede generar HTML como el siguiente: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sort"&nbsp;onchange="gcGo(this);"&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=relevance;sp_sfvl_field=product-type|category|size;"&nbsp;selected="selected"&gt;Sort&nbsp;by&nbsp;Relevance&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=avail-code;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Availability&lt;/option&gt; 
      &nbsp;&nbsp;&lt;option&nbsp;value="?sort=price;sp_sfvl_field=product-type|category|size;"&gt;Sort&nbsp;by&nbsp;Price&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-value /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la cadena del valor asociado al menú. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-label /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la cadena de la etiqueta asociada al menú. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-menu-item-path /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la cadena de ruta. Utilice la etiqueta si desea agregar un parámetro a la ruta y crear un vínculo personalizado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-menu-item-selected&gt; 
      &lt;guided-else-menu- 
      item-selected&gt; 
      &lt;/guided-if-menu-item-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Devuelve un 1 o 0 que indica si el elemento de menú actual está seleccionado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagenav {#section_2EE397635C514BBC8D668278EA314F35}

Las etiquetas de navegación de la página se pueden utilizar para crear un conjunto de vínculos que permitan al usuario pasar de página en los resultados de la búsqueda.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-pages&gt;&lt;/guided-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta de bucle para la navegación de la página. Cualquier contenido entre las etiquetas de apertura y de cierre se iterará para cada página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link [tari="value"]+&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un vínculo en la navegación de la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-link gsname="first|prev|next|last|viewall|viewpages" [attr="value"]+&gt;&lt;/guided-page-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un vínculo a la primera, anterior, siguiente o última página. También puede crear un vínculo para vista de todas las páginas en una página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-number /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Devuelve una cadena con el número de página actual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if-page-selected&gt; 
      &lt;guided-else-page- 
      selected&gt; 
      &lt;/guided-if-page-selected&gt; </code> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas condicionales es true si se selecciona la página que está actualmente iterada. Generalmente se utiliza para mostrar de manera diferente el número de página en el control de navegación de la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-prev&gt; 
      &lt;guided-else-page- 
      prev&gt; 
      &lt;/guided-if[-not]-page-prev&gt; </code> </p> </td> 
   <td colname="col2"> <p> Este conjunto de etiquetas condicionales es true si la página actual tiene una página anterior. Generalmente se utiliza para mostrar un vínculo anterior en la navegación de la página, cuando tiene sentido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-next&gt; 
      &lt;guided-else-page- 
      next&gt; 
      &lt;/guided-if[-not]-page-next&gt; </code> </p> </td> 
   <td colname="col2"> <p> Este conjunto de etiquetas condicionales es true si la página actual tiene una página siguiente. Generalmente se utiliza para mostrar un vínculo anterior en la navegación de la página, cuando tiene sentido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewall&gt; 
      &lt;guided-else-page- 
      viewall&gt; 
      &lt;/guided-if[-not]-page-viewall&gt; </code> </p> </td> 
   <td colname="col2"> <p> Cuando una búsqueda devuelve un gran conjunto de resultados, es posible que no desee oferta la capacidad de vista de todos los resultados. Por lo tanto, puede utilizar este conjunto de etiquetas condicionales para determinar cuándo mostrar el vínculo Vista todo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-page-viewpages&gt; 
      &lt;guided-else-page- 
      viewpages&gt; 
      &lt;/guided-if[-not]-page-viewpages&gt; </code> </p> </td> 
   <td colname="col2"> <p>Puede utilizar este conjunto de etiquetas condicionales para determinar cuándo mostrar el vínculo Páginas de Vista. Generalmente se utiliza para permitir que un cliente realice vistas en determinadas páginas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> 

    &amp;lt;guided-else-page-link&amp;gt;
    &amp;lt;/guided-if[-not]-page-link&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Comprueba si la navegación de la página tiene una primera página, una página anterior, una página siguiente, etc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matched search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-page-total /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Devuelve una cadena con el número total de páginas de resultados de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-pagination gsname= 
      "pagination_name"&gt;&lt;/guided-pagination&gt; </code> </p> </td> 
   <td colname="col2"> <p>Utilice la <span class="codeph"> etiqueta de paginación guiada </span> para definir un área en la que todas las etiquetas de paginación se relacionan con una configuración de paginación específica en caso de que tenga pocas opciones de navegación definidas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> 

    next|last|viewall|viewpages]/&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Crea su propio vínculo en la navegación de la página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-high-eq-last&gt; 
      &lt;guided-else-page- 
      high-eq-last&gt; 
      &lt;/guided-if-page-high-eq-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Comprueba si la página más alta de la navegación de la página es igual al número total de páginas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-page-low-eq-first&gt; 
      &lt;guided-else-page-low-eq-first&gt; &lt;/guided-if-page-low-eq-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Comprueba si la página más baja en la navegación de la página es igual a la misma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-page-is-multipage&gt; &lt;guided-else-page-is-multipage&gt; &lt;/guided-if-page-is-multipage&gt; </span> </p> </td> 
   <td colname="col2"> <p>Prueba si hay una sola página de resultados o varias páginas de resultados. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Búsquedas recientes {#section_8CD907521F584257B475595B01A5964B}

Puede utilizar las etiquetas de búsqueda recientes para crear un conjunto de vínculos que permitan al usuario ejecutar rápidamente una búsqueda anterior, como en el ejemplo siguiente:

```
<guided-if-recent-searches> 
    <span>Recent Searches</span><br/> 
    <guided-recent-searches> 
        <guided-recent-searches-link><guided-recent-searches-value></guided-recent-searches-link><br/> 
    </guided-recent-searches> 
    <guided-recent-searches-clear-link>Clear Recent Searches</guided-recent-searches-clear-link> 
</guided-if-recent-searches>
```

Consulte [Configuración de búsquedas](../c-about-design-menu/t-configuring-recent-searches.md#task_E9E8ACA04C90484F8AFD5262167B2562)recientes.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches&gt;&lt;/guided-recent-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta de bucle para búsquedas recientes. Cualquier contenido entre las etiquetas de apertura y de cierre se iterará para cada página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-recent-searches-link [attr="value"]+&gt; 
      &lt;/guided-recent-searches-link&gt; </code> </p> </td> 
   <td colname="col2"> <p>Permite crear un vínculo a una búsqueda reciente. Admite el paso de cualquier atributo HTML directamente a la etiqueta de anclaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite capturar la ruta de URL relativa para una búsqueda reciente, dentro de un <span class="codeph"> bucle </span> de búsqueda guiada-reciente. Normalmente, utilizaría <span class="codeph"> guided-last-search-link </span>. Sin embargo, si desea crear su propio vínculo, puede utilizar esta etiqueta. A continuación se muestra un ejemplo: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;a&amp;nbsp;href="&lt;guided_recent_searches_path&gt;"&gt;&lt;guided-recent-searches-value&gt;&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-value&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite capturar el término de consulta asociado con una búsqueda reciente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-link [tari="valor"]+&gt;&lt;/guided-recent-searches-clear-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Le permite oferta a sus clientes para que puedan borrar las búsquedas guardadas recientemente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recent-searches-clear-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la ruta que <span class="codeph"> &lt;guided-recent-searches-clear-link&gt; </span> utiliza para que pueda crear su propio vínculo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 

    &amp;lt;/guided-if-recent-searches&amp;gt; &lt;/code> &lt;/p> &lt;/td>
<td colname="col2"> <p>Permite mostrar las búsquedas recientes cuando un cliente ha realizado una búsqueda reciente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Quizás quiso decir {#section_C1EB3B9D8E1242798A6E04609D1E3543}

Puede utilizar las etiquetas Quiso decir para crear un conjunto de vínculos a sugerencias cuando una búsqueda no arroje resultados y el término Buscar no esté en el diccionario de la cuenta. A continuación se muestra un ejemplo del uso de etiquetas Quiso decir:

```
<guided-if-suggestions> 
    <span>Did You Mean?</span><br/> 
    <guided-suggestions> 
        <guided-suggestion-link><guided-suggestion/></guided-suggestion-link><br/> 
    </guided-suggestions> 
</guided-if-suggestions>
```

Consulte [Acerca de ¿quiso decir?](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E).

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-recommendations&gt;&lt;/guided-recommendations&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta es la etiqueta de bucle para realizar bucles sobre las sugerencias. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Matches search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-recommendations-link [attr="value"]+&gt;&lt;/guided-sugesesv-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Crea un vínculo a una sugerencia determinada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Newly added from search-eng version, 2/1/2013--> <span class="codeph"> &lt;guided-recommendations-value /&gt; </span> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-suggestions&gt;&lt;guided-else[-not]- 
      suggestions&gt;&lt;/guided-if[-not]-suggestions&gt; </code> </p> </td> 
   <td colname="col2"> <p>Permite probar si hay alguna sugerencia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recommendations-path/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la cadena de ruta a la sugerencia. Puede utilizarla para crear su propia etiqueta de anclaje. Normalmente, <span class="codeph"> se utiliza el vínculo guiado-sugerencia- </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recommendations/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Una sugerencia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recommendations-result-count/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Recuento de resultados de la sugerencia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-autosearch&gt; 
      &lt;guided-else[-not]-suggestion-autosearch&gt; 
      &lt;/guided-if[-not]-suggestion-autosearch&gt; </code> </p> </td> 
   <td colname="col2"> <p>Permite probar si la búsqueda automática por sugerencia no arrojó ningún resultado, en caso de que esta función esté activada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-recommendations-original-consulta/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la consulta original si se realizó una búsqueda automática. </p> <p>Ejemplo de uso: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-autosearch&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt; 
      &lt;/guided-if-suggestion-autosearch&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-suggestion-low-results&gt; 
      &lt;guided-else[-not]-suggestion-low-results&gt; 
      &lt;/guided-if[-not]-suggestion-low-results&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta condición es verdadera si hay sugerencias debido a un recuento bajo de resultados, en caso de que esta función esté activada. </p> <p>A continuación se muestra un ejemplo de uso de esta etiqueta: </p> <p> <code class="syntax html"> &lt;guided-if-suggestion-low-results&gt; 
      &nbsp;&nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;guided-query-param&nbsp;gsname="q"&nbsp;/&gt;. 
      &nbsp;&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion&nbsp;/&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt; 
      &lt;/guided-if-suggestion-low-results&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Autocompletar {#section_897316BEE1454E839A56B565CA4AF018}

Las etiquetas siguientes se pueden utilizar para agregar el llenado automático al formulario de búsqueda. Las etiquetas head-content y form-content son necesarias para que la función de autocompletar sea correcta. Se recomienda utilizar las etiquetas en lugar de codificar el Javascript y CSS de autocompletar en la plantilla de presentación. El motivo es que las etiquetas permiten a las plantillas captar cualquier ID de caché de derrota nueva cada vez que se cambia la configuración de autocompletar sin necesidad de actualizar manualmente la plantilla.

Consulte [Acerca de la finalización](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578)automática.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-autocomplete&gt; &lt;guided-else-autocomplete&gt; &lt;/guided-if-autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p>Detecta si la función de autocompletar está activada. Puede utilizar las etiquetas para elegir el encabezado y el contenido del formulario necesarios para la realización automática. A su vez, esto le permite activar y desactivar la función sin tener que modificar las plantillas de presentación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-css/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Se utiliza en el encabezado de la plantilla de presentación y se sustituye por la secuencia de comandos CSS adecuada que incluye para el autocompletado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-form-content/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Se utiliza en el formulario de búsqueda (entre las etiquetas <span class="codeph"> &lt;form&gt; </span> y <span class="codeph"> &lt;/form&gt; </span> ) de la plantilla de presentación en lugar de codificar las etiquetas de autocompletado del formulario. Las etiquetas se reemplazan por el HTML adecuado que es necesario para que funcione el llenado automático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-ac-javascript/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Genera los vínculos al JavaScript de finalización automática. Para un mejor rendimiento, se recomienda colocar esta etiqueta cerca de la parte inferior de la página antes de la etiqueta "body" de cierre. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Store {#section_A33E25DB5E67404A823BD9618665B773}

Utilice las etiquetas siguientes para probar y mostrar la tienda en la que se encuentra un usuario.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-store/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae la tienda actual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store-defined&gt; &lt;guided-else-store-defined&gt; &lt;/guided-if-store-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Detecta si el usuario está en una tienda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-store gsname="store"&gt; &lt;guided-else-store&gt; &lt;/guided-if-store&gt; </span> </p> </td> 
   <td colname="col2"> <p>Detecta si el usuario está en el almacén especificado por el parámetro <span class="codeph"> gsname </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zonas {#section_B9B3179E000C42D492E1541F2FE44CB5}

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-zone gsname="zone area" [search="associated search"] [facet="facet asociado"] [width="xx" height="yy"]&gt; </span> </p> </td> 
   <td colname="col2"> <p>Puede ajustar cualquier contenido en etiquetas de zona para crear una zona fuera de esa área. Esto le permite utilizar reglas comerciales para mostrar la zona según sea necesario. De forma predeterminada, las zonas siempre se muestran. Puede utilizar los parámetros opcionales de búsqueda y faceta para indicar qué búsqueda o faceta está asociada a la zona. Esta funcionalidad permite que el software omita las búsquedas o facetas cuando una zona está oculta, lo que mejora el rendimiento en tiempo de búsqueda. Los atributos de altura y ancho son opcionales y se utilizan para configurar cómo se muestra el marcador de posición en el Generador de reglas visuales cuando se elimina una zona. </p> <p> Utilice la <span class="codeph"> etiqueta guiada-si-facet[-no]-visible </span> en lugar de la zona donde sea posible. Simplifica la plantilla de presentación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-zone gsname="zone area"&gt; &lt;guided-else-zone&gt; &lt;/guided-if-zone&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas permite realizar pruebas si se está mostrando una zona. Resulta útil cuando tiene contenido en otra parte de la página que solo desea mostrar cuando se muestra la zona. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Indicadores de bucle {#section_387322CA0AA843A2ACF2795C328673E9}

Puede utilizar cada uno de los siguientes indicadores de bucle en cualquiera de estos bloques de bucle:

* guided-results
* guided-facet-values
* guía-ruta
* guided-menu-items
* páginas guiadas

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-first&gt;&lt;guided-else[-not]-first&gt; 
      &lt;/guided-if[-not]-first&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta condición es verdadera cuando la iteración actual es la primera iteración del bucle. Esto no significa necesariamente el primer resultado o la primera página, sino la primera que se muestra. Si el visitante del sitio está en la página 2 de un conjunto de resultados que es 10 por página, la primera iteración es el resultado 11. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-last&gt;&lt;guided-else[-not]-last&gt; 
      &lt;/guided-if[-not]-last&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta condición es verdadera cuando la iteración actual es la última iteración del bucle. Esto no significa necesariamente el último resultado o la última página, sino la última que se muestra en el contexto actual (página). Si el visitante del sitio se encuentra en la página 1 de un conjunto de resultados que contiene 200 resultados pero solo tiene 10 resultados por página, la última iteración será el resultado 10 en lugar del resultado 200. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng version, 2/1/2013--> <code> &lt;guided-if[-not]-odd&gt;&lt;guided-else[-not]-odd&gt; 
      &lt;/guided-if[-not]-odd&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta condición es verdadera cuando la iteración actual es una iteración impar del bucle (frente a una iteración par). Esto resulta útil para mostrar distintos colores de fila. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta condición es verdadera cuando la iteración actual es una iteración par del bucle (frente a una iteración impar). Esto resulta útil para mostrar distintos colores de fila. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta condición es verdadera cuando la iteración actual es una iteración par del bucle. Esto resulta útil para mostrar distintos colores de fila. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Incluye el texto entre ellos si la iteración actual no es ni la primera ni la última. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Incluye el texto entre ellos si la iteración actual es la primera o la última. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Un entero (a partir de 0) cuyo valor aumenta para cada iteración del bucle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-loop-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Un entero (comenzando desde 1) cuyo valor aumenta para cada iteración del bucle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Idioma varios {#section_BFE8DC98E26F4D7BB60FEC54D9A5DC6C}

Las siguientes etiquetas están disponibles para permitirle realizar tareas más avanzadas con la plantilla, como crear su propia minifaceta.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-current-path [escape="html|url|js|json|0"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Proporciona la ruta actual que se utiliza. Generalmente se utiliza para crear un vínculo que agrega un nuevo parámetro a la búsqueda existente. De forma predeterminada, la ruta es URL escapada. Puede especificar qué modo de escape desea utilizar mediante el parámetro escape. </p> <p>Ejemplo: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path&nbsp;/&gt;&amp;lang=fr"&gt; 
      French&nbsp;Version </code> </p> <p>En este ejemplo, una regla de procesamiento de búsqueda utiliza lang para seleccionar la versión en francés. </p> <p>La ruta de acceso actual siempre tiene al menos un parámetro de consulta. Si no existen otros parámetros de consulta, se establece en <span class="codeph"> q=* </span> , lo que facilita la adición de más parámetros. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> Ruta base </span> </p> </td> 
   <td colname="col2"> <p> Si desea crear un vínculo mediante la ruta base, utilice <span class="codeph"> / </span> en el inicio de su <span class="codeph"> href </span> y agregue parámetros. </p> <p> <code class="syntax html"> &lt;a&nbsp;href="/"&gt;All&nbsp;Products&lt;/a&gt; 
      Would&nbsp;create&nbsp;a&nbsp;link&nbsp;"All&nbsp;Products"&nbsp;to&nbsp;your 
      basepath,&nbsp;for&nbsp;example&nbsp;https://search.mycompany.com/ 
       </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> 
     <!--Updated to match search-eng, 2/1/2013--> <span class="codeph"> &lt;guided-consulta-param gsname="parámetro_consulta" [escape="html|url"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite capturar el valor existente de un parámetro de consulta que se encuentra en la dirección URL. Si el parámetro no existe, esta etiqueta devuelve una cadena vacía. Si no especifica una opción de escape, la cadena devuelta será HTML escapado automáticamente, puede especificar HTML o URL escapando. </p> <p>Ejemplo: </p> <p> 

    &amp;lt;guided-consulta-param&amp;nbsp;gsname=&quot;q&quot;&amp;nbsp;/&amp;gt;
    da&amp;nbsp;you&amp;nbsp;nbsp;value&amp;nbsp;nbsp;nbsp;pantalones
    
    &amp;lt;guided-consulta-param&amp;nbsp;nbsp;gssp;name=&quot;lang&quot;&amp;nbsp;/&amp;gt;
    da&amp;nbsp;you&amp;nbsp;the&amp;nbsp;value&amp;nbsp;en
    
    &amp;lt;guided-consulta-param&amp;nbsp;gsname=&quot;test&quot;&amp;nbsp;/&amp;gt;
    s &amp;nbsp;you&amp;nbsp;an&amp;nbsp;empty&amp;nbsp;string
    &amp;nbsp;
    &amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;nbsp;&amp;sp; nbsp;; &lt;/code> &lt;/p> &lt;/td>
</tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-consulta-param-name gsname="param#" offset="offset_number"/&gt; </span> </p> </td> 
   <td colname="col2"> <p>La búsqueda guiada tiene la noción de un número de consulta, que se utiliza en el control de la ruta de exploración. <span class="codeph"> guided-consulta-param-name </span> permite definir parámetros como parte de un vínculo en la plantilla de presentación en el que Búsqueda guiada determina el número de consulta correcto para usted. El <span class="codeph"> gsname </span> tiene una "x", que la búsqueda guiada reemplaza por el número correcto. El valor de desplazamiento puede ser 0 - 15, donde 0 indica que se utiliza el siguiente número de consulta disponible. Un 1 indica que desea agregar 1 a él, y así sucesivamente. </p> <p>Combinado con <span class="codeph"> guided-current-path </span>, puede crear su propio vínculo mini facet o permitir un nivel de exploración adicional. </p> <p>Ejemplo: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="q#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="x#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category"&nbsp;&gt;Category:Men&lt;/a&gt;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </code> </p> <p> <code class="syntax html"> &lt;a&nbsp;href="&lt;guided-current-path 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=mens&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=category&amp;&lt;guided-query-param-name&nbsp;gsname="sp_q_exact_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=Jeans&amp;&lt;guided-query-param-name&nbsp;gsname="sp_x_#"&nbsp;offset="1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/&gt;=product-type"&nbsp;&gt;Cat:Men&nbsp;-&nbsp;Product:Jeans&lt;/a&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-include gsfile="filename" /&gt; </span> </p> </td> 
   <td colname="col2"> <p> Permite incluir otros archivos de plantilla. Esta funcionalidad significa que puede crear varias plantillas usando subplantillas como módulos. </p> <p>En el siguiente ejemplo, se incluyen los <span class="filepath"> archivos de rutas de exploración </span> y <span class="filepath"> facetas </span> : </p> <p> <code class="syntax html"> &lt;guided-include&nbsp;gsfile='breadcrumbs.tmpl'&nbsp;/&gt; 
      &lt;guided-include&nbsp;gsfile='facets.tmpl'&nbsp;/&gt; </code> </p> <p>Las inclusiones dinámicas no son compatibles. En otras palabras, <span class="codeph"> gsfile </span> no puede ser una variable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p> Identifica cuánto tiempo tardó la búsqueda. El valor de tiempo de búsqueda devuelto se especifica en ms. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-fall-through-searches&gt; </span> </p> </td> 
   <td colname="col2"> <p> Devuelve el recuento de búsquedas de núcleos que se utilizan para generar la página de resultados de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW 1/17/2013--> <span class="codeph"> &lt;guided-if-fall-through-search&gt;&lt;/guided-if-fall-through-search&gt; </span> </p> </td> 
   <td colname="col2"> <p>Prueba si el recuento de búsquedas principales es bueno a uno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-even&gt;&lt;guided-else[-not]-even&gt; 
      &lt;/guided-if[-not]-even&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta condición es verdadera cuando la iteración actual es una iteración par del bucle (frente a una iteración impar). Esto resulta útil para mostrar distintos colores de fila. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-alt&gt;&lt;guided-else[-not]-alt&gt; 
      &lt;/guided-if[-not]-alt&gt; </code> </p> </td> 
   <td colname="col2"> <p>Esta condición es verdadera cuando la iteración actual es una iteración par del bucle. Esto resulta útil para mostrar distintos colores de fila. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-inner&gt;&lt;guided-else[-not]-inner&gt; 
      &lt;/guided-if[-not]-inner&gt; </code> </p> </td> 
   <td colname="col2"> <p>Incluye el texto entre ellos si la iteración actual no es ni la primera ni la última. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if[-not]-outer&gt;&lt;guided-else[-not]-outer&gt; 
      &lt;/guided-if[-not]-outer&gt; </code> </p> </td> 
   <td colname="col2"> <p>Incluye el texto entre ellos si la iteración actual es la primera o la última. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <code> &lt;guided-if-first-search&gt;&lt;guided-else-first-search&gt; 
      &lt;/guided-if-first-search&gt; </code> </p> </td> 
   <td colname="col2"> <p>Le permite comprobar si está en la búsqueda inicial o no (la consulta fue el resultado de una búsqueda desde el cuadro de búsqueda). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-search-url/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Puede utilizar esta etiqueta en la plantilla para guardar la acción del formulario de búsqueda codificada. Detecta cuándo se encuentra en el entorno de ensayo o activo y cambia en consecuencia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-consulta-param-defined gsname="consulta_parameter"&gt; &lt;guided-else-consulta-param-defined&gt; &lt;/guided-if-consulta-param-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas permite probar qué parámetros CGI están definidos en la ruta de búsqueda. Puede probar los valores de los parámetros solo si están definidos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-next-consulta-number [gsname="offset"] /&gt; </span> </p> </td> 
   <td colname="col2"> <p>El motor de búsqueda guiada que impulsa la plantilla tiene la noción de números de consulta flotantes donde cada nuevo vínculo que genera el motor, utiliza el siguiente número de consulta disponible. Esta etiqueta permite obtener el siguiente número de consulta o desplazamientos para poder crear vínculos personalizados que profundizan en el conjunto de resultados. El desplazamiento le permite desplazarse al siguiente número de consulta. Por ejemplo, si ha seleccionado una faceta, el siguiente número de consulta es 2, con un desplazamiento de 1, el número de consulta devuelto es 3. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-custom-var gsname="custom_variable" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite capturar el valor existente de una variable personalizada que definen las reglas de procesamiento. Si no especifica una opción de escape, la cadena devuelta será HTML escapado automáticamente, puede especificar <span class="codeph"> html </span>, url <span class="codeph"> , </span>js <span class="codeph"> o </span>0 <span class="codeph"> </span>. Si utiliza una regla de procesamiento para copiar un parámetro CGI entrante en una variable personalizada y, a continuación, muestra o utiliza esa variable en la plantilla con el carácter de escape establecido en ninguno o js, puede crear una vulnerabilidad XSS en la búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-custom-var-defined gsname="custom_variable"&gt; &lt;guided-else-custom-var-defined&gt; &lt;/guided-if-custom-var-defined&gt; </span> </p> </td> 
   <td colname="col2"> <p>Habilita la prueba si se define una variable personalizada en las reglas de procesamiento (limpieza de consultas, procesamiento previo a la búsqueda y procesamiento posterior a la búsqueda). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-general-field gsname="searchname" field="fieldname" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite mostrar el contenido de un campo general definido en la plantilla de transporte. Si no especifica una opción de escape, la cadena devuelta se codifica en el formato especificado en la plantilla de transporte para ese campo. Especificar una opción de escape se aplica sobre cualquier formato que esté codificando el campo como en la plantilla de transporte. Puede especificar <span class="codeph"> html </span>, <span class="codeph"> url </span>, <span class="codeph"> js </span>, <span class="codeph"> json </span>o <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-general-field gsname="searchname" field="field-name"&gt; &lt;guided-else-general-field&gt; &lt;/guided-if-general-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Habilita la prueba si existe el contenido de un campo general, tal como se define en la plantilla de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-cookie-value gsname="cookie_name" [escape="html|url|js|json|0"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite capturar el valor de una cookie, suponiendo que la cookie esté disponible. Si no especifica una opción de escape, la cadena devuelta será HTML escapado automáticamente, puede especificar <span class="codeph"> html </span>, url <span class="codeph"> , </span>js <span class="codeph"> , </span>json <span class="codeph"> o </span>0 <span class="codeph"> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-cookie gsname="cookie_name"&gt; &lt;guided-else-cookie&gt; &lt;/guided-if-cookie&gt; </span> </p> </td> 
   <td colname="col2"> <p>Habilita la prueba si existe una cookie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>23 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-banner gsname="banner area" [escape="html|url|js|json|0"] [width="xx" height="yy"]/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae la pancarta de un área determinada. Los atributos opcionales de anchura y altura se utilizan en el Generador de reglas visuales para habilitar la visualización de un marcador de posición significativo que permita a los usuarios seleccionar un letrero. De forma predeterminada, las pancartas no se escapan. En su lugar, desea insertar HTML en la plantilla de presentación. Sin embargo, si está creando una plantilla JSON, considere la posibilidad de utilizar la opción de escape js. </p> <p>Ejemplo: </p> <p> <code class="syntax html"> &lt;guided-banner&nbsp;gsname="top"&nbsp;width="400px" 
      &nbsp;height="50px"/&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>24 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-banner-set gsname="banner area"&gt; &lt;guided-else-banner-set&gt; &lt;/guided-if-banner-set&gt; </span> </p> </td> 
   <td colname="col2"> <p>Habilita la prueba si se ha establecido un área de pancarta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>25 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-simulator-mode&gt; &lt;guided-else-simulator-mode&gt; &lt;/guided-if-simulator-mode&gt; </span> </p> </td> 
   <td colname="col2"> <p>Permite detectar cuándo está viendo la búsqueda en el simulador o en el Generador de reglas visuales. Normalmente se utiliza para mostrar información de depuración adicional. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>26 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-tnt-business-rules&gt; &lt;guided-else-tnt-business-rules&gt; &lt;/guided-if-tnt-business-rules&gt; </span> </p> </td> 
   <td colname="col2"> <p>Le permite detectar si tiene reglas comerciales que hagan referencia a una <span class="keyword"> campaña de Adobe Target </span> . Normalmente se utiliza como parte de la integración con <span class="keyword"> Adobe Target </span> para evitar que se produzcan visitas a los servidores de <span class="keyword"> Destinatario </span> cuando no es necesario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>27 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-redirect/&gt; </span> </p> </td> 
   <td colname="col2"> <p>De forma predeterminada, las redirecciones se realizan automáticamente. Sin embargo, si ha configurado la búsqueda/comercialización del sitio para devolver una respuesta XML o JSON a la aplicación Web, puede elegir analizar la respuesta 302/301 en la aplicación Web o hacer que la redirección se le pase como parte del conjunto de resultados. Si está pasando la redirección como parte del conjunto de resultados, esta etiqueta se puede utilizar en la plantilla para generar la ubicación de redirección. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>28 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-if-redirect&gt; &lt;guided-else-redirect&gt; &lt;/guided-if-redirect&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cuando haya configurado la búsqueda/comercialización del sitio para devolver redirecciones en el conjunto de resultados, este conjunto de etiquetas se puede utilizar para determinar si hay una redirección a la salida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>29 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-lt/&gt; &lt;guided-gt/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas permite incrustar etiquetas de plantilla guiadas en los atributos HTML. </p> <p>Ejemplo: </p> <p> <code class="syntax html"> &lt;guided-lt/&gt;div&nbsp;&lt;guided-if-facet-long&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;style="height:&nbsp;125px;&nbsp;overflow: 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;auto;"&lt;/guided-if-facet-long&gt;&lt;guided-gt/&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Etiquetas de plantilla de transporte {#reference_227D199F5A7248049BE1D405C0584751}

Las plantillas de transporte son plantillas XML que pasan datos de la búsqueda back-end a la capa de presentación Búsqueda guiada.

<!-- 

r_transport_template_tags.xml

 -->

En la capa de presentación, puede tener una sola plantilla de presentación que presente los resultados de varias búsquedas. Cada búsqueda podría utilizar la misma plantilla de transporte o una plantilla de transporte personalizada para pasar los datos a la capa de presentación.

Dado que la plantilla de transporte solo se utiliza para pasar datos a la capa de presentación, no tiene ningún código HTML que se ocupe de mostrar los resultados de búsqueda. La plantilla de transporte utiliza etiquetas XML de plantilla de transporte para pasar los resultados de búsqueda y rellenar los componentes de Búsqueda guiada, como facetas, rutas de exploración y menús. Dentro de estas etiquetas se utilizan etiquetas de plantilla de búsqueda estándar para mostrar los valores reales.

Consulte [Edición de una presentación o una plantilla](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transporte.

Consulte [Buscar etiquetas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de plantilla.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Etiqueta de plantilla de transporte </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>Las etiquetas XML raíz que utiliza la capa de presentación para detectar lo que se analiza a partir de la plantilla de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>Las etiquetas rodean las etiquetas de plantilla de búsqueda que proporcionan datos de resumen basados en el conjunto de resultados. Normalmente, estas etiquetas contienen etiquetas de búsqueda para el número total de resultados, el resultado inferior y el resultado más alto. Puede definir cualquier número de campos globales adicionales que desee con la <span class="codeph"> etiqueta de campo general </span> , como en el siguiente ejemplo: </p> <p> <code class="syntax html"> &lt;general&gt; 
      &nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Las etiquetas se envuelven alrededor de los resultados de búsqueda, para que la búsqueda guiada sepa dónde buscarlos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>Las etiquetas se envuelven alrededor de cada resultado de búsqueda, de modo que la búsqueda guiada reconoce dónde termina y inicio el contenido de un único resultado de búsqueda, como en el siguiente ejemplo: </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Le permite recorrer en bucle cada elemento en una lista de varios valores para un único resultado. Utilice solo esta etiqueta dentro de un resultado. Su propósito es permitirle iterar los atributos que pertenecen a un campo de resultado, como en el siguiente ejemplo: </p> <code class="syntax html"> &lt;results&gt; 
     &nbsp;&nbsp;&lt;search-results&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
     &nbsp;&nbsp;&lt;/search-results&gt; 
     &lt;/results&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facets&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>Pasa los resultados que rellenan las facetas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <!--NEW 2/27/2014--> <span class="codeph"> &lt;dynamic-facet&gt;&lt;/dynamic-facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> Puede designar una faceta como una faceta dinámica y como miembro de un carril de facetas. Sin embargo, su tratamiento es independiente con respecto a las etiquetas de plantilla de presentación relacionadas. </p> <p>En otras palabras, no se permite anidar un contexto de bucle de carril de faceta dentro de un contexto de bucle de faceta dinámica, o viceversa. </p> <p>En el caso de las facetas dinámicas y con barras, solo las facetas dinámicas que se devolvieron para una búsqueda determinada son visibles dentro del contexto de bucle de carril de facetas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p> Cada faceta tiene sus propias etiquetas de faceta donde el parámetro name coincide con el nombre de faceta. Las etiquetas de búsqueda se utilizan dentro de las etiquetas de facetas para los valores de facetas, como en el siguiente ejemplo: </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; 
     &lt;/facets&gt; </code> <p> Las cuentas que utilizan facetas asignadas pueden utilizar la etiqueta dinámica y la etiqueta display-names. Ambas etiquetas ayudan a facilitar la asignación entre facetas con asignación y facetas reales al crear reglas comerciales. </p> <code class="syntax html"> &lt;facets&gt; 
     &nbsp;&nbsp;&lt;facet&nbsp;name="facet_values01"&gt; 
     &nbsp;&lt;dynamic&gt;1&lt;/dynamic&gt; 
     &nbsp;&lt;display-names&gt;&lt;search-field-value-list&nbsp;name="facet_names01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/display-names&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="facet_values01"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
     &nbsp;&nbsp;&lt;/facet&gt; </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field separator=","&gt; </span> </p> </td> 
   <td colname="col2"> <p>El <span class="codeph"> atributo separator </span> permite cambiar el delimitador que se utiliza al generar datos de campo de visualización de búsqueda para listas. El valor predeterminado es una coma. </p> <p>Generalmente, el delimitador que utilice debe ser algo que no aparezca fácilmente en el contenido del campo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;sugerencias&gt;&lt;/recommendations&gt; </span> </p> </td> 
   <td colname="col2"> <p> Ajuste las sugerencias Quiso decir con etiquetas para que la búsqueda guiada reconozca qué nodos XML contienen sugerencias. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">Acerca de ¿quiso decir?</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;sugerencia&gt;&lt;/sugerencia&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ajuste cada sugerencia ¿Quiso decir? con etiquetas, como en el siguiente ejemplo: </p> <code class="syntax html"> &lt;search-if-suggestions&gt; 
     &nbsp;&nbsp;&lt;suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/suggestion&gt; 
     &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
     &nbsp;&nbsp;&lt;/suggestions&gt; 
     &lt;/search-if-suggestions&gt; </code> <p>Consulte <a href="../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E" type="concept" format="dita" scope="local">Acerca de ¿quiso decir?</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Buscar etiquetas de plantilla {#reference_F7AA3FF602314E42842BBC740D2CA1A4}

Una plantilla de búsqueda es un archivo HTML que incluye etiquetas de plantilla que define la búsqueda o comercialización del sitio. Estas etiquetas indican el formato de los resultados de búsqueda. La siguiente referencia contiene una breve descripción de cada etiqueta de plantilla de búsqueda y sus atributos.

<!-- 

r_search_template_tags.xml

 -->

>[!NOTE]
>
>Utilice únicamente etiquetas de plantilla de búsqueda en archivos de plantilla de transporte (.tpl).

Puede seleccionar entre los siguientes grupos de etiquetas de plantilla de búsqueda y material de referencia.

Las etiquetas que solo son válidas dentro del bucle de resultados incluyen lo siguiente:

* [Acerca de las etiquetas de bucle Results](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)
* [Etiquetas de cadena de bucle de resultados](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Etiquetas condicionales de bucle de resultados](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Etiquetas de vínculos de anclaje de bucle de resultados](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Etiquetas condicionales de posición de bucle](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

Las etiquetas válidas en toda la plantilla incluyen lo siguiente:

* [Etiquetas de lista de valor de campo](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1)
* [Etiquetas de bucle de lista de valor de campo](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E)
* [Sugerir etiquetas](../c-appendices/c-templates.md#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC)
* [Etiquetas de cadena de plantilla](../c-appendices/c-templates.md#section_67E3D529661F4F03A1FF469D9D658CAF)
* [Etiquetas de vínculos de anclaje de plantilla](../c-appendices/c-templates.md#section_3A51D27616C541E2B818CC52B2B856BA)
* [Etiquetas condicionales de plantilla](../c-appendices/c-templates.md#section_18D9BC66DE484881932FD2F7EA9D170D)
* [Etiquetas de control de formulario de plantilla](../c-appendices/c-templates.md#section_45AFC414ACA74825B72FEAA8456F8DD2)

Buscar temas de referencia de plantilla

* [Cadenas de formato de fecha](../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4)
* [Identificadores de idioma](../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911)
* [Especificación del encabezado HTTP de tipo de contenido](../c-appendices/c-templates.md#section_AEED823E9938448A9EDB2F286D9CFD90)
* [Especificación de un conjunto de caracteres en una plantilla HTML](../c-appendices/c-templates.md#section_E0D1816ABB5846BEBE9C26D5980CCBE6)
* [Especificación de un conjunto de caracteres en una plantilla XML](../c-appendices/c-templates.md#section_17DC31CDCC104F5F8081466B41A96E9D)
* [Inclusión de una plantilla de búsqueda dentro de otra](../c-appendices/c-templates.md#section_7D1FCD3D9E2340C291E354C9720E8BC0)

## Acerca de las etiquetas de bucle Results {#section_D4DC7B4560144663972E8DBC3369C629}

La etiqueta de bucle de resultados es el eje del sistema de plantillas. Cuando se encuentra la etiqueta durante una búsqueda, se repite el código HTML y otras etiquetas entre las etiquetas de bucle de resultados inicial y final, reemplazando cualquier otra etiqueta con los resultados de búsqueda.

`<search-results> ... </search-results>`

Las etiquetas de bucle de resultados rodean el HTML que muestra los resultados de la búsqueda. El HTML entre las etiquetas se repite para cada resultado y se muestra en la página.

Las etiquetas siguientes solo son válidas dentro del bucle de resultados:

* [Etiquetas de cadena de bucle de resultados](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)
* [Etiquetas condicionales de bucle de resultados](../c-appendices/c-templates.md#section_35C367969E384A06A9865E388F1F9360)
* [Etiquetas de vínculos de anclaje de bucle de resultados](../c-appendices/c-templates.md#section_C5FAEF520E9E42ADAD1F90651922AA02)
* [Etiquetas condicionales de posición de bucle](../c-appendices/c-templates.md#section_E0C29DDA09E043C9A396F36334F05EBB)

## Etiquetas de cadena de bucle de resultados {#section_80D68334E8D04A33937A6E58ABAAA320}

Las etiquetas siguientes devuelven una cadena.

Consulte [Acerca de las etiquetas](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)de bucle Results.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve el índice numérico del resultado actual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-title length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve el título de la página del resultado actual. El atributo length opcional se utiliza para limitar la longitud de las cadenas mostradas, con un valor predeterminado de 80 caracteres. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-bodytext length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve el texto principal comenzando desde la parte superior de la página. Los términos relevantes se muestran en negrita. El atributo length opcional se utiliza para limitar la longitud de las cadenas mostradas, con un valor predeterminado de 80 caracteres. El atributo de codificación es opcional y puede codificar caracteres de salida con codificación HTML (predeterminado), codificación Javascript, codificación Perl o ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-description length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Devuelve la descripción del resultado actual. Si la etiqueta meta description existe y el atributo content no está vacío, se muestra ese texto. De lo contrario, se muestra el principio del texto principal de la página. El atributo length opcional se utiliza para limitar la longitud de las cadenas mostradas, con un valor predeterminado de 80 caracteres. </p> <p>El atributo de codificación opcional <span class="codeph"> </span> controla si el resultado es HTML codificado, JavaScript codificado, Perl codificado, URL codificado o no codificado, para que se muestre en la página de resultados. El valor predeterminado de <span class="codeph"> codificación </span> es <span class="codeph"> html </span>. Normalmente, no es necesario especificar el atributo de codificación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-score rank="dynamic/static/dynamic-raw/static-raw/final-raw" Precision="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la puntuación del resultado actual, que es un número entre 0 y 100. Si ha definido un campo de clasificación en <span class="uicontrol"> Opciones </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Definiciones </span>, puede mostrar la clasificación de página dinámica configurando el atributo de clasificación en dinámico ( <span class="codeph"> &lt;search-score="dynamic"&gt; </span>). Puede mostrar la clasificación de página estática estableciendo el atributo de clasificación en estático ( <span class="codeph"> &lt;search-score rank="static"&gt; </span>). Puede utilizar el atributo de precisión opcional para especificar el número de lugares decimales que desea mostrar. El valor predeterminado es 0, que muestra la puntuación entera). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-date length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la fecha del resultado actual. El valor de texto opcional "ninguno" se muestra si no hay ninguna fecha asociada al resultado actual. Si no se proporciona el valor "ninguno" opcional, se muestra el texto "Sin fecha" si no hay ninguna fecha asociada al resultado actual. </p> <p>El atributo "date-format" toma una cadena de formato de fecha de estilo UNIX como "%A, %B %d, %Y" (para "lunes, 25 de julio de 2016"). "gmt" tiene el valor predeterminado "sí" y controla si la parte de tiempo de la cadena de fecha debe aparecer en GMT ("sí") o en la zona horaria de la cuenta ("no"). </p> <p>El atributo "language" controla las convenciones de idioma y configuración regional de la cadena de fecha de salida. "0" (valor predeterminado) significa "Usar idioma de la cuenta". "2" significa "Usar lenguaje de Documento". El valor "language" "1" está reservado para uso futuro. Cualquier otro valor de "idioma" se interpreta como un identificador de idioma específico; por ejemplo, "en_US" significa "inglés (Estados Unidos)". </p> <p>El atributo length opcional se utiliza para limitar la longitud de las cadenas mostradas, con un valor predeterminado de 80 caracteres. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-size&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve el tamaño del resultado actual en bytes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la dirección URL del resultado actual. </p> <p>Utilice el atributo <span class="codeph"> length opcional </span> para limitar la longitud de las cadenas mostradas, con un valor predeterminado de caracteres ilimitados. </p> <p>El <span class="codeph"> atributo de codificación </span> es opcional y puede codificar caracteres de salida con codificación HTML, codificación Javascript, codificación Perl o ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-url-path-consulta length="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la ruta y las partes de consulta, incluido el signo de interrogación de la dirección URL del resultado actual. </p> <p>Utilice el atributo <span class="codeph"> length opcional </span> para limitar la longitud de las cadenas mostradas, con un valor predeterminado de caracteres ilimitados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-context length="XX" encoding="html/javascript/json/perl/url/none" &gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la siguiente línea de contexto para el término de búsqueda. Los términos relevantes se muestran en negrita. Llame esta etiqueta repetidamente para mostrar más de una línea de contexto para el resultado actual. </p> <p>Utilice el atributo <span class="codeph"> length opcional </span> para limitar la longitud de las cadenas mostradas, con un valor predeterminado de 80 caracteres. El atributo <span class="codeph"> length </span> se omite si esta etiqueta está encerrada en conjuntos de etiquetas <span class="codeph"> &lt;search-if-context&gt; </span> o <span class="codeph"> &lt;search-if-any-context&gt; </span> que contienen un atributo length. </p> <p>El <span class="codeph"> atributo de codificación </span> es opcional y puede codificar caracteres de salida con codificación HTML (predeterminado), codificación Javascript, codificación Perl o ninguno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field name="field-name" length="XX" none="text" date-format="date-format-string" gmt="yes/no" language="0/2/language-id" encoding="html/javascript/json/perl/url/none" quote="yes/no" comas="yes/no" unit="miles/kilómetros" separator"|"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta avanzada muestra el contenido del campo de metadatos (url, título, desc, claves, destinatario, cuerpo, alt, fecha, charset, idioma o campos definidos en <span class="uicontrol"> Opciones </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; Definiciones) especificado en el atributo <span class="codeph"> name </span> , para el resultado actual. Por ejemplo: </p> <p> <span class="codeph"> &lt;search-display-field name="title" length="70" none="no title"&gt; </span> </p> <p>Genera el título de la página para un resultado de búsqueda. Si se especifica el atributo <span class="codeph"> none </span> opcional, su valor se muestra en la página de resultados sólo si no hay contenido asociado al campo. </p> <p>Los atributos <span class="codeph"> date-format </span>, <span class="codeph"> gmt </span> y <span class="codeph"> language </span> solo son relevantes si el tipo de contenido del campo especificado es <span class="codeph"> date </span>. </p> <p>El atributo <span class="codeph"> date-format </span> toma una cadena de formato de fecha de estilo UNIX como <span class="codeph"> %A, %B %d, %Y </span> (para lunes 25 de julio de 2016). <span class="codeph"> gmt </span> tiene el valor predeterminado <span class="codeph"> sí </span> y controla si la porción horaria de la cadena de fecha se muestra en GMT ( <span class="codeph"> sí </span>) o en la zona horaria de la cuenta ( <span class="codeph"> no </span>). </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Cadenas</a>de formato de fecha. </p> <p>El <span class="codeph"> atributo language </span> controla las convenciones de idioma y configuración regional de la cadena de fecha de salida. <span class="codeph"> 0 </span> (valor predeterminado) significa "Usar idioma de la cuenta". <span class="codeph"> 2 </span> significa "Usar lenguaje de Documento". El <span class="codeph"> idioma </span> valor <span class="codeph"> 1 </span> está reservado para uso futuro). Cualquier otro <span class="codeph"> valor de idioma </span> se interpreta como un identificador de idioma específico, por ejemplo, <span class="codeph"> en_US </span> significa "Inglés (Estados Unidos)". </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identificadores</a>de idioma. </p> <p>El atributo <span class="codeph"> length opcional </span> se utiliza para limitar la longitud de las cadenas mostradas, con un valor predeterminado de 80 caracteres. </p> <p>El atributo de codificación opcional <span class="codeph"> </span> controla si el resultado es HTML codificado, JavaScript codificado, Perl codificado, URL codificado o no codificado, para que se muestre en la página de resultados. El valor predeterminado de <span class="codeph"> codificación </span> es <span class="codeph"> html </span>. Normalmente, no es necesario especificar el atributo de codificación. </p> <p>El atributo <span class="codeph"> de comillas </span> opcional controla si los elementos individuales resultantes están rodeados de comillas dobles (o comillas simples, si <span class="codeph"> encoding=perl </span>). El valor predeterminado de <span class="codeph"> comillas </span> es <span class="codeph"> no </span>. </p> <p>El atributo opcional <span class="codeph"> comas </span> controla si la salida de elementos individuales está separada por comas. El valor predeterminado de <span class="codeph"> comas </span> es <span class="codeph"> sí </span>. El atributo <span class="codeph"> comas </span> se ignora en los campos que no son de tipo lista. </p> <p>El atributo opcional <span class="codeph"> Units </span> controla las unidades de distancia aplicadas a un campo de salida de búsqueda de proximidad. El valor predeterminado de <span class="codeph"> las unidades </span> se determina a partir de la configuración "Unidades predeterminadas" del campo de tipo ubicación asociado con el campo de salida de búsqueda de proximidad dado. </p> <p>Consulte <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Acerca de la búsqueda</a>de proximidad. </p> <p>El atributo <span class="codeph"> separador </span> opcional define el carácter único, o delimitador, que se inserta entre los valores del resultado de los campos de tipo lista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-values name="field-name"&gt;...&lt;search-display-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta crea un bucle para enumerar valores de campo de metadatos (url, título, desc, claves, destinatario, cuerpo, alt, fecha, charset y idioma o campos definidos en <span class="uicontrol"> Opciones </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Definiciones </span>) para el resultado actual. No anide esta etiqueta dentro de otra etiqueta <span class="codeph"> &lt;search-display-field-values&gt; </span> . El <span class="codeph"> atributo name </span> especifica el nombre del campo que contiene los valores que se van a enumerar. Esta etiqueta resulta más útil con los campos en los que se ha activado el atributo <span class="uicontrol"> Listas de permitidos </span> (en <span class="uicontrol"> Opciones </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Definiciones </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta genera el valor del campo de metadatos (url, título, desc, claves, destinatario, cuerpo, alt, fecha, charset y idioma o campos definidos en <span class="uicontrol"> Opciones </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Definiciones </span>) para la iteración del bucle <span class="codeph"> &lt;search-display-field-values&gt; </span> actual. Esta etiqueta solo es válida dentro de un bucle <span class="codeph"> &lt;search-display-field-values&gt; </span> . Los atributos <span class="codeph"> date-format </span>, <span class="codeph"> gmt </span> y <span class="codeph"> language </span> solo son relevantes si el tipo de contenido del nombre del campo especificado en la etiqueta <span class="codeph"> &lt;search-display-field-values&gt; </span> que lo rodea es <span class="codeph"> date </span>. El atributo <span class="codeph"> date-format </span> toma una cadena de formato de fecha de estilo UNIX como <span class="codeph"> "%A </span>, <span class="codeph"> %B </span> %d <span class="codeph"> , </span>%Y <span class="codeph"> </span>" (para "lunes, 25 de julio de 2016"). El atributo <span class="codeph"> gmt </span> tiene el valor predeterminado de <span class="codeph"> sí </span> y controla si la porción horaria de la cadena de fecha se muestra en GMT ( <span class="codeph"> sí </span>) o en la zona horaria de la cuenta ( <span class="codeph"> no </span>). </p> <p>El <span class="codeph"> atributo language </span> controla las convenciones de idioma y configuración regional de la cadena de fecha de salida. <span class="codeph"> 0 </span> (valor predeterminado) significa "Usar idioma de la cuenta". Cualquier otro <span class="codeph"> valor de idioma </span> se interpreta como un identificador de idioma específico, por ejemplo, <span class="codeph"> en_US </span> significa "Inglés (Estados Unidos)". </p> <p>El atributo de codificación opcional <span class="codeph"> </span> controla si el resultado es HTML codificado, JavaScript codificado, Perl codificado, URL codificado o no codificado, para que se muestre en la página de resultados. El valor predeterminado de <span class="codeph"> codificación </span> es <span class="codeph"> html </span>. Normalmente, no es necesario especificar el atributo de codificación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-count name="field-name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae el número total de valores en el resultado actual para el campo de metadatos (url, título, desc, claves, destinatario, cuerpo, alt, fecha, charset, idioma o campos definidos en <span class="uicontrol"> Opciones </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Definiciones </span>) especificado con el atributo name. Esta etiqueta puede aparecer en cualquier parte del bucle de resultados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-display-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae el contador ordinal (1, 2, 3, etc.) para la iteración actual del bucle <span class="codeph"> &lt;search-display-field-values&gt; </span> . Esta etiqueta solo es válida dentro de un bucle <span class="codeph"> &lt;search-display-field-values&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-fields&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inicia un contexto de bucle para los campos de faceta dinámica devueltos para esta búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-dynamic-facet-field-name&gt; </span> </p> </td> 
   <td colname="col2"> <p>Extrae el nombre del campo de faceta dinámica actual para esta iteración de bucle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-result-trace encoding="html/javascript/ json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Proporciona información relacionada con la ubicación del resultado actual, por ejemplo, cualquier acción basada en resultados que afecte a la posición del resultado. </p> <p>El formato de salida de esta etiqueta es JSON como en el siguiente ejemplo: </p> <p> <code> { 
      &nbsp;&nbsp;"sliceID":&nbsp;5, 
      &nbsp;&nbsp;"indexID":&nbsp;5894, 
      &nbsp;&nbsp;"finalScore":&nbsp;98.5, 
      &nbsp;&nbsp;"dynamicScore":&nbsp;15.3, 
      &nbsp;&nbsp;"staticScore":&nbsp;55.456, 
      &nbsp;&nbsp;"position":&nbsp;1, 
      &nbsp;&nbsp;"rbtaActionListID":&nbsp;117, 
      &nbsp;&nbsp;"rbtaActionID":&nbsp;57 
      } </code> </p> 
    <!--<p> Results added to the results set by way of <codeph>rbta</codeph> have a "naturalPosition" value of -1. </p>--> <p>El <span class="codeph"> atributo de codificación </span> es opcional; el valor predeterminado es <span class="codeph"> html </span>. </p> <p> <p>Nota:  Esta etiqueta solo tiene resultados si <span class="codeph"> sp_trace=1 </span> se especifica con los parámetros de consulta de búsqueda principales. </p> </p> <p>Consulte la fila 48 de la tabla que se encuentra en los parámetros <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"></a>CGI de búsqueda back-end. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Etiquetas condicionales de bucle de resultados {#section_35C367969E384A06A9865E388F1F9360}

Las siguientes etiquetas incluyen condicionalmente el HTML entre ellas.

Consulte [Acerca de las etiquetas](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)de bucle Results.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-title&gt;... &lt;/search-if-title&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-title&gt; ... &lt;/search-if-not-title&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el HTML entre ellas si la siguiente llamada a <span class="codeph"> &lt;search-title&gt; </span> devuelve (o no devuelve) texto del título del documento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-description length="XX"&gt;... /search-if-description&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-description&gt; ... &lt;/search-if-not-description&gt; </span> </p> </td> 
   <td colname="col2"> <p> Estas etiquetas incluyen el HTML entre ellas si la siguiente llamada a <span class="codeph"> &lt;search-description&gt; </span> devuelve (o no devuelve) texto de la descripción del documento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bodytext&gt; ... &lt;/search-if-bodytext&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bodytext&gt; ... &lt;/search-if-not-bodytext&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el HTML entre ellas si la siguiente llamada a <span class="codeph"> &lt;search-bodytext&gt; </span> devuelve (o no devuelve) texto del cuerpo del documento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-context length="XX"&gt;... &lt;/search-if-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-context&gt; ... &lt;/search-if-not-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el HTML entre ellas si la siguiente llamada a <span class="codeph"> &lt;search-context&gt; </span> devuelve (o no devuelve) una cadena de contexto no vacía. El atributo length anula el atributo length en cualquier etiqueta <span class="codeph"> &lt;search-context&gt; </span> adjunta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-any-context length="XX"&gt; ... /search-if-any-context&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-any-context&gt; ... &lt;/search-if-not-any-context&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el HTML entre ellas si hay (o no) una cadena de contexto asociada al resultado. El atributo length anula el atributo length en cualquier etiqueta <span class="codeph"> &lt;search-context&gt; </span> adjunta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-score lower="XX" top="yy" rank="dynamic/static/dynamic-raw/static-raw/final-raw"&gt;&gt; ... &lt;/search-if-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-score lower=XX top=yy rank="dynamic/static"&gt; ... &lt;/search-if-not-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el HTML entre ellas si la puntuación del resultado actual está (o no) entre XX y AA. Resulta útil para añadir viñetas o gráficos para mostrar la relevancia del resultado. Si ha definido un campo de tipo clasificación en <span class="uicontrol"> Opciones </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Definiciones </span>, puede comprobar la clasificación de la página dinámica estableciendo el atributo de clasificación en dinámico ( <span class="codeph"> &lt;search-if-score="dynamic" lower=XX top=YY&gt; </span>). Puede comprobar la clasificación de la página estática estableciendo el atributo de clasificación en estático ( <span class="codeph"> &lt;search-if-score="static" lower=XX top=YY&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field name="field-name" value="value"&gt; ... &lt;/search-if-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field name="field-name" value="value"&gt; ... &lt;/search-if-not-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas avanzadas incluyen el HTML entre ellas en función de si el campo especificado en el atributo "name" tiene contenido o no. Si se especifica el atributo opcional "value", las etiquetas incluyen el HTML entre ellas en función de si el valor dado coincide (o no coincide) con el valor del campo en el resultado actual. Estas etiquetas solo funcionan dentro del bucle de resultados (entre las etiquetas <span class="codeph"> &lt;search-results&gt; </span> y <span class="codeph"> &lt;/search-results&gt; </span> ). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Etiquetas de vínculos de anclaje de bucle de resultados {#section_C5FAEF520E9E42ADAD1F90651922AA02}

Consulte [Acerca de las etiquetas](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)de bucle Results.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-link destinatario="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX" &gt;... &lt;/search-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este par de etiquetas crea un vínculo de anclaje alrededor del HTML entre ellas. Cuando se hace clic en el vínculo, se muestra la página de resultados. Un atributo de destinatario opcional especifica la ventana con nombre en la que los navegadores compatibles con marcos deben mostrar la página de resultados. </p> <p>Establezca el atributo hbx-enable en "yes" para aprovechar los análisis disponibles a través de HBX. Establezca hbx-linkid-name en el nombre de un campo de metadatos que desee rastrear. Por ejemplo, para rastrear los resultados de búsqueda por número de SKU, establezca hbx-linkid-name en el nombre del campo Meta-data que contiene información de SKU. </p> <p>Los campos de tipo de fecha no son compatibles actualmente. El valor de hbx-linkid-name se anexa al ID del vínculo en el anclaje generado. El valor del atributo hbx-linkid-none se anexa al ID del vínculo siempre que el campo Meta-data con nombre esté vacío. El valor de hbx-linkid-length limita el número de caracteres recuperados y mostrados desde la etiqueta Meta. El número predeterminado de caracteres es 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-smart-link destinatario="frame-name" hbx-enable="yes/no" hbx-linkid-name="field-name" hbx-linkid-none="text" hbx-linkid-length="XX"&gt;... &lt;/search-smart-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este par de etiquetas es similar al <span class="codeph"> &lt;search-link&gt; ... &lt;/search-link&gt; </span> . Cuando se hace clic en los vínculos de anclaje generados, se muestra la página de resultados, pero con la página desplazada hasta la etiqueta de anclaje más cercana que precede al resultado. En el caso de los vínculos PDF, el visor de Acrobat muestra la página que contiene el resultado. Un atributo de destinatario opcional especifica la ventana con nombre en la que los navegadores compatibles con marcos deben mostrar la página de resultados. </p> <p>Establezca el atributo hbx-enable en "yes" para aprovechar los análisis disponibles a través de HBX. Establezca hbx-linkid-name en el nombre de un campo de metadatos que desee rastrear. Por ejemplo, para rastrear los resultados de búsqueda por número de SKU, establezca hbx-linkid-name en el nombre del campo Meta-data que contiene información de SKU. </p> <p>Los campos de tipo de fecha no son compatibles actualmente. El valor de hbx-linkid-name se anexa al ID del vínculo en el anclaje generado. El valor del atributo hbx-linkid-none se anexa al ID del vínculo siempre que el campo Meta-data con nombre esté vacío. El valor de hbx-linkid-length limita el número de caracteres recuperados y mostrados desde la etiqueta Meta. El número predeterminado de caracteres es 12. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-link-extension&gt; ... &lt;/search-if-link-extension&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-link-extension&gt; ... &lt;/search-if-not-link-extension&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el HTML entre ellas si un atributo de valor especifica una extensión que coincide con el final de la URL del resultado. Esta etiqueta es útil para incluir un gráfico en los resultados de búsqueda según la extensión del vínculo. El atributo value es una lista de una o varias extensiones (separadas por espacios) de la siguiente manera: VALUE=".pdf" o VALUE=".html .htm". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Etiquetas condicionales de posición de bucle {#section_E0C29DDA09E043C9A396F36334F05EBB}

Las etiquetas siguientes incluyen condicionalmente el texto entre ellas. Solo pueden aparecer dentro de las etiquetas de &quot;bucle&quot;: &lt; `search-results>` y `<search-field-values>`. Se utilizan para probar la posición del resultado actual dentro del conjunto de resultados.

Consulte [Acerca de las etiquetas](../c-appendices/c-templates.md#section_D4DC7B4560144663972E8DBC3369C629)de bucle Results.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-first&gt; ... &lt;/search-if-first&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-first&gt; ... &lt;/search-if-not-first&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el texto entre ellas si el resultado actual es (o no) el primer resultado de la página (cuando se utiliza dentro de <span class="codeph"> &lt;search-results&gt; </span>) o el primer valor de campo (cuando se utiliza dentro de <span class="codeph"> &lt;search-field-values&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-last&gt; ... &lt;/search-if-last&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-last&gt; ... &lt;/search-if-not-last&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el texto entre ellas si el resultado actual es (o no) el último resultado de la página (cuando se utiliza dentro de <span class="codeph"> &lt;search-results&gt; </span>) o el último valor del campo (cuando se utiliza dentro de <span class="codeph"> &lt;search-field-values&gt; </span>). Esta etiqueta se puede utilizar para insertar un separador entre los resultados. Por ejemplo, inserta una etiqueta <span class="codeph"> &lt;hr&gt; </span> entre los resultados: </p> <p> <code class="syntax html"> &lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-inner&gt; ... &lt;/search-if-inner&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-inner&gt; ... &lt;/search-if-not-inner&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el texto entre ellas si el resultado actual no es el primero ni el último de la página (cuando se utiliza dentro de <span class="codeph"> &lt;search-results&gt; </span>) o no es el primer ni el último valor del campo (cuando se utiliza dentro de <span class="codeph"> &lt;search-field-values&gt; </span>). La versión no de la etiqueta comprueba si el resultado es el primero o el último. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-alt&gt; ... &lt;/search-if-alt&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-alt&gt; ... &lt;/search-if-not-alt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el texto entre ellas si el resultado actual es (o no) un resultado alternativo en la página (cuando se utiliza dentro de <span class="codeph"> &lt;search-results&gt; </span>) o un valor de campo alternativo (cuando se utiliza dentro de <span class="codeph"> &lt;search-field-values&gt; </span>). Los resultados "alternativos" son el segundo, cuarto, sexto, etc., de la página. En este ejemplo se aplica una clase diferente a filas de tabla alternativas. Tenga en cuenta el uso de <span class="codeph"> &lt;search-lt&gt; </span> y <span class="codeph"> &lt;search-gt&gt; </span> para permitir que la etiqueta <span class="codeph"> &lt;search-if-alt&gt; </span> se coloque "dentro" de la <span class="codeph"> &lt;tr&gt; </span> . </p> <p> <code class="syntax html"> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-lt&gt;tr&lt;search-if-alt&gt;&nbsp;class="alt"&lt;/search-if-alt&gt;&lt;search-gt&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;td&gt;&lt;search-url&gt;&lt;/td&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/tr&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-even&gt;... &lt;/search-if-even&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-even&gt; ... &lt;/search-if-not-even&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen el texto entre ellas si el resultado actual es (o no) un resultado par (cuando se utiliza dentro de <span class="codeph"> &lt;search-results&gt; </span>) o un valor de campo par (cuando se utiliza dentro de <span class="codeph"> &lt;search-field-values&gt; </span>). Un resultado de búsqueda es par si su valor <span class="codeph"> &lt;search-index&gt; </span> es par. En otras palabras, si su posición dentro de todo el conjunto de resultados es uniforme. Esto puede diferir de <span class="codeph"> &lt;search-if-alt&gt; </span> que prueba la posición de un resultado en la página, no en todo el conjunto de resultados. Las dos tablas siguientes ilustran la diferencia: </p> </td> 
  </tr> 
 </tbody> 
</table>

### Primera página, sp_n=1

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Índice </p> </th> 
   <th colname="col2" class="entry"> <p>Resultado </p> </th> 
   <th colname="col3" class="entry"> <p>¿Incluso? </p> </th> 
   <th colname="col4" class="entry"> <p>¿Alt? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Primer resultado </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Segundo resultado </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Tercer resultado </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Cuarto resultado </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>Quinto resultado </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
 </tbody> 
</table>

### Página posterior, sp_n=10

<table>  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Índice </p> </th> 
   <th colname="col2" class="entry"> <p>Resultado </p> </th> 
   <th colname="col3" class="entry"> <p>¿Incluso? </p> </th> 
   <th colname="col4" class="entry"> <p>¿Alt? </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>Décimo resultado </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p>Undécimo resultado </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>Duodécimo resultado </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>Decimotercer resultado </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>Decimocuarto resultado </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
  </tr> 
 </tbody> 
</table>

Por último, tenga en cuenta que siempre `<search-if-even>` es lo mismo que `<search-if-alt>` para los valores de los campos de búsqueda, ya que los valores de los campos no se paginan.

## Etiquetas de lista de valor de campo {#section_D3298B5F976447DBA0032B883DCC91B1}

Las etiquetas avanzadas siguientes generan valores de campo y datos relacionados de todo el conjunto de resultados de búsqueda. Estas etiquetas solo producen resultados para los campos especificados por los parámetros `sp-sfvl-field` CGI en la consulta de búsqueda.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-lista name="field-name" quote="yes/no" comas="yes/no" data="values/counts/results" separator="X" sortby="none/values/counts/results" max-items="XX" date-format="date-format-string" gmt="yes/no" language="0/language-id" encoding="html/html javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta muestra una lista de valores de campo únicos, recuentos de valores o recuentos de resultados en todo el conjunto de resultados. </p> <p>Esta etiqueta solo produce resultados para los campos especificados por los parámetros CGI <span class="codeph"> sp_sfvl_field </span> en la consulta de búsqueda. El atributo opcional "comillas" controla si la salida de elementos individuales está rodeada por comillas dobles (o comillas simples, si encoding=perl). El valor predeterminado de "comillas" es "sí". El atributo opcional "comas" controla si la salida de elementos individuales está separada por comas. El valor predeterminado de "comas" es "yes". El atributo opcional "data" controla si se genera cada valor de campo único (data="values"), el recuento total de cada valor de campo único (data="counts") o el número de resultados que contienen cada valor único (data="results"). El valor predeterminado de "data" es "values". Para los campos que no son de tipo lista, data="counts" y data="results" son equivalentes. El atributo separator define el carácter único, o delimitador, que se insertará entre los valores de la salida. El atributo opcional "sortby" controla el orden de la salida; sortby="none" significa que no hay un orden concreto, sortby="values" significa ordenar por valores de campo (en orden ascendente o descendente según la propiedad Sorting del campo), sortby="counts" significa ordenar en orden descendente los recuentos de valores de campo y ordenar por "resultados" significa ordenar en orden descendente el número de resultados que contiene cada valor. </p> <p>Tenga en cuenta que sortby="counts" y sortby="results" son equivalentes para los campos que no son de tipo lista. El atributo opcional "max-items" limita el número de elementos que se van a generar. El valor predeterminado de "max-items" es -1, lo que significa "salida de todos los elementos". </p> <p>Hay un límite absoluto de 100 para los artículos máximos. Los atributos "date-format", "gmt" y "language" solo son relevantes si el tipo de contenido del campo especificado es "date". El atributo "date-format" toma una cadena de formato de fecha de estilo UNIX como "%A, %B %d, %Y" (para "lunes, 25 de julio de 2016"). "gmt" tiene el valor predeterminado "sí" y controla si la parte de tiempo de la cadena de fecha debe aparecer en GMT ("sí") o en la zona horaria de la cuenta ("no"). </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Cadenas</a>de formato de fecha. </p> <p>El atributo "language" controla las convenciones de idioma y configuración regional de la cadena de fecha de salida. "0" (valor predeterminado) significa "Usar idioma de la cuenta". Cualquier otro valor de "idioma" se interpreta como un identificador de idioma específico; por ejemplo, "en_US" significa "inglés (Estados Unidos)". El atributo opcional "encoding" controla si los caracteres de cadena de salida son HTML codificados, JavaScript codificados, Perl codificados, URL codificados o no, para que se muestren en la página de resultados. El valor predeterminado de "encoding" es "html". </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identificadores</a>de idioma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-lista-count name="field-name" value="field-value" results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta muestra la información de recuento de una determinada lista search-field-value. Esta etiqueta tiene tres usos distintos. Si solo se proporciona el atributo "name", esta etiqueta genera el número de valores únicos para el campo con nombre dentro de todo el conjunto de resultados. Si se proporcionan los atributos "name" y "value", esta etiqueta genera el recuento total del valor dado en todo el conjunto de resultados (para results="no") o el recuento total de resultados que contiene el valor dado en todo el conjunto de resultados (para results="yes"). El valor predeterminado de "results" es "no". Nota: Para los campos que no son de tipo lista, los resultados="sí" y los resultados="no" son equivalentes. El valor de "results" se omite si no se proporciona el atributo "value". Esta etiqueta solo produce resultados para los campos especificados por los parámetros CGI de campo <span class="codeph"> </span> sp-sfvl en la consulta de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-field-value-lista-count name="field-name" value="field-value"&gt;&gt;... &lt;/search-if-field-value-lista-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-field-value-lista-count name="field-name" value="field-value"&gt;&gt;... &lt;/search-if-not-field-value-lista-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas muestran el HTML entre ellas si la llamada equivalente a <span class="codeph"> &lt;search-field-value-lista-count name="field-name" value="field-value"&gt; </span> con los atributos dados devolverá (o no) un valor bueno que no sea cero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-single-field-value-lista-count name="field-name"&gt;&gt; ... &lt;/search-if-single-field-value-lista-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas muestran el contenido entre ellas si la llamada equivalente a <span class="codeph"> &lt;search-field-value-lista-count name="field-name" value="field-value"&gt; </span> con los atributos dados devolverá (o no devolverá) un solo valor. Esto generalmente se utiliza cuando una cuenta utiliza ranuras de facetas. Con las ranuras de facetas, normalmente solo desea mostrar la ranura de valores cuando la ranura de nombres asociada tiene un solo elemento. Realizar esta comprobación en la plantilla de transporte es más eficaz que hacerlo en la capa de presentación. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Etiquetas de bucle de lista de valor de campo {#section_0717FA09F0FC449CB916883B0500A60E}

Las siguientes etiquetas avanzadas enumeran y muestran los valores de campo de salida y los datos relacionados de todo el conjunto de resultados de búsqueda mediante una construcción de bucle. Estas etiquetas solo producen resultados para los campos especificados por los parámetros `sp-sfvl-field` CGI en la consulta de búsqueda.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-values name="field-name" sortby="none/values/counts/results" max-items="XX"&gt;... &lt;/search-field-values&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta crea un bucle para enumerar valores de campo y datos relacionados para un campo concreto dentro de todo el conjunto de resultados. No anide esta etiqueta dentro de otra etiqueta <span class="codeph"> &lt;search-field-values&gt; </span> . El atributo "name" especifica el nombre del campo que contiene los valores que se van a enumerar. El atributo opcional "sortby" controla el orden de lista desglosada: "ninguno" significa que no hay un orden concreto, "valores" significa ordenar por valores de campo (en orden ascendente o descendente según la propiedad Ordenación del campo), ordenar por="recuentos" significa ordenar en orden descendente los recuentos de valor del campo y ordenar por "resultados" significa ordenar en orden descendente el número de resultados que contienen cada valor. </p> <p>Tenga en cuenta que sortby="counts" y sortby="results" son equivalentes para los campos que no son de tipo lista. . El atributo opcional "max-items" limita el número de iteraciones al valor dado. El valor predeterminado de "max-items" es -1, lo que significa "enumerar todos los valores". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value date-format="date-format-string" encoding="html/javascript/json/perl/url/none" gmt="yes/no" language="0/language-id"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta genera el valor de campo para la iteración de bucle actual &lt;search-field-values&gt;. Esta etiqueta solo es válida dentro de un bucle <span class="codeph"> &lt;search-field-values&gt; </span> . Los atributos "date-format", "gmt" y "language" solo son relevantes si el tipo de contenido del nombre del campo especificado en la etiqueta &lt;search-field-values&gt; que lo rodea es "date". El atributo "date-format" toma una cadena de formato de fecha de estilo UNIX como "%A, %B %d, %Y" (para "lunes, 25 de julio de 2020"). </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_4BBDBBEF2B96414497617CD4B52D96E4" type="section" format="dita" scope="local"> Cadenas</a>de formato de fecha. </p> <p>El atributo opcional "encoding" controla si los caracteres de cadena de salida son HTML codificados, JavaScript codificados, Perl codificados, URL codificados o no, para que se muestren en la página de resultados. El valor predeterminado de "encoding" es "none". Normalmente, no es necesario especificar el atributo de codificación. "gmt" tiene el valor predeterminado "sí" y controla si la parte de tiempo de la cadena de fecha debe aparecer en GMT ("sí") o en la zona horaria de la cuenta ("no"). El atributo "language" controla las convenciones de idioma y configuración regional de la cadena de fecha de salida. "0" (valor predeterminado) significa "Usar idioma de la cuenta". Cualquier otro valor de "idioma" se interpreta como un identificador de idioma específico; por ejemplo, "en_US" significa "inglés (Estados Unidos)". </p> <p>Consulte <a href="../c-appendices/c-templates.md#section_0490DECC00E34691ADE5A9ED90A6D911" type="section" format="dita" scope="local"> Identificadores</a>de idioma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-count results="yes/no"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta genera el recuento asociado con la iteración de bucle <span class="codeph"> &lt;search-field-values&gt; </span> actual. El recuento de resultados es el número de resultados en todo el conjunto de resultados que contiene el valor de campo (results="yes") o el recuento total del valor de campo en todo el conjunto de resultados. El valor predeterminado de "results" es "no". </p> <p>Para los campos que no son de tipo lista, los resultados="sí" y los resultados="no" son equivalentes. Esta etiqueta solo es válida dentro de un bucle <span class="codeph"> &lt;search-field-values&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-field-value-counter&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta genera el contador ordinal de la iteración del bucle <span class="codeph"> &lt;search-field-values&gt; </span> actual. Esta etiqueta solo es válida dentro de un bucle <span class="codeph"> &lt;search-field-values&gt; </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sugerir etiquetas {#section_C28EB8B4F7DC4E278A0F143BCFEEB1AC}

Sugiero proporciona un sencillo mensaje de usuario &quot;¿Quiso decir?&quot; para sugerir términos de búsqueda alternativos. Si un usuario ha escrito mal un término de búsqueda, por ejemplo, Sugerir puede ayudar al usuario a encontrar los resultados sugiriendo una ortografía correcta. El sistema también puede sugerir palabras clave relacionadas que pueden ayudar al usuario a descubrir los resultados. Al generar sugerencias, el servicio Sugerir utiliza dos diccionarios: uno basado en el idioma de la cuenta (establecido en **[!UICONTROL Indexing]** > **[!UICONTROL Words and Languages]** > **[!UICONTROL Language]**) y el otro creado exclusivamente a partir de las palabras clave en el índice de la cuenta.

>[!NOTE]
>
>El servicio Sugerir no funciona para chino, japonés o coreano.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-recommendations&gt;... &lt;/search-if-recommendations&gt; </span> </p> </td> 
   <td colname="col2"> <p>Rodee estas etiquetas con cualquier etiqueta de plantilla "Sugerir", tales como <span class="codeph"> &lt;search-sugerencia&gt; </span>, <span class="codeph"> &lt;search-sugerencia-vínculo&gt; </span>, etc. Si la búsqueda genera sugerencias, el motor de búsqueda genera y procesa todo lo que haya entre las etiquetas open y close. Si la búsqueda no genera sugerencias, no se muestra ningún contenido anidado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-recommendations&gt;... &lt;/search-recommendations&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta genera el bucle "Sugerir", que contiene una lista de términos de búsqueda sugeridos (por ejemplo, "intención", "intención" y "intención", para una consulta ingresada originalmente como "intenciones"). Al generar la lista de términos, el motor de búsqueda repite cualquier etiqueta HTML o de plantilla anidada hasta cinco veces, que es el número máximo de sugerencias. Utilice el atributo count para especificar el número de sugerencias generadas (entre 0 y 5). </p> <p>La etiqueta <span class="codeph"> &lt;search-recommendations&gt; </span> puede aparecer varias veces en la página para repetir la lista de sugerencias. Las sugerencias múltiples se ordenan según el número de resultados que cada uno arroje. </p> <p>Anide la etiqueta <span class="codeph"> &lt;search-recommendations&gt; </span> entre las etiquetas open y close <span class="codeph"> &lt;search-if-recommendations&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sugerencia-link&gt;... &lt;/search-sugerencia-link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta genera un vínculo a la consulta de búsqueda original utilizando el término de búsqueda sugerido seleccionado en lugar del término original. La etiqueta acepta y simplemente imprime cualquier atributo HTML como clase, destinatario y estilo. La etiqueta también puede aceptar un atributo de URL, cuyo valor se utiliza como dirección URL base para el vínculo generado. Las etiquetas solo pueden aparecer dentro del bucle <span class="codeph"> &lt;search-recommendations&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sugerencia-text/&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta imprime el término de consulta sugerido actualmente (por ejemplo, "intención" de una consulta introducida originalmente como "intenciones"). La etiqueta no tiene atributos y solo puede aparecer dentro del bucle <span class="codeph"> &lt;search-recommendations&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-not-recommendations&gt; ... &lt;/search-if-not-recommendations&gt; </span> </p> </td> 
   <td colname="col2"> <p>Si la búsqueda no genera sugerencias, el motor de búsqueda genera y procesa todo lo que haya entre la etiqueta open y close. Si la búsqueda genera sugerencias, no se muestra ningún contenido anidado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-first-recommendations&gt; ... &lt;/search-if[-not]-first-recommendations&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas condicionales incluyen el HTML entre ellas en función de si el término sugerido es el primer término del bucle Sugerir. Las etiquetas deben aparecer entre las etiquetas open y close <span class="codeph"> &lt;search-recommendations&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if[-not]-last-recommendations&gt; ... &lt;/search-if[-not]-last-recommendations&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas condicionales incluyen el HTML entre ellas en función de si el término sugerido es el último término del bucle Sugerir. Las etiquetas deben aparecer entre las etiquetas open y close <span class="codeph"> &lt;search-recommendations&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sugerencia-index&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta devuelve el índice numérico del término de búsqueda sugerido actual. La etiqueta debe aparecer entre las etiquetas open y close <span class="codeph"> &lt;search-recommendations&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-recommendations-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta devuelve el número total de términos de búsqueda sugeridos generados. La etiqueta debe aparecer entre las etiquetas open y close <span class="codeph"> &lt;search-recommendations&gt; </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sugerencia-result-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta devuelve el número total de resultados para el término de búsqueda sugerido. La etiqueta debe aparecer entre las etiquetas open y close <span class="codeph"> &lt;search-recommendations&gt; </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Etiquetas de cadena de plantilla {#section_67E3D529661F4F03A1FF469D9D658CAF}

Las etiquetas siguientes envían una cadena al HTML en ese punto de la plantilla.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-body&gt; </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta de cuerpo HTML con cualquier configuración de color de vínculo de búsqueda que la sección de aspecto básico establezca en el vínculo Plantilla. Añada un atributo de fondo a esta etiqueta para mostrar imágenes de fondo en la página de resultados. Cualquier atributo de color agregado a esta etiqueta anula la configuración de Color del vínculo de búsqueda que establece la sección Aspecto básico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-header&gt; </span> </p> </td> 
   <td colname="col2"> <p>El HTML para el encabezado de resultados de búsqueda como se define en la sección Aspecto básico en el vínculo Plantilla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-data&gt;... &lt;/search-data&gt; </span> </p> </td> 
   <td colname="col2"> <p>Las etiquetas search-data se reemplazan con sus equivalentes XML: <span class="codeph"> &lt;search-data&gt; </span> se reemplaza por <span class="codeph"> &lt;![CDATA[" y la etiqueta &lt;/search-data&gt; </span> se reemplazan por " <span class="codeph"> ]]&gt; </span>". Un analizador de XML no analiza ninguna información entre las etiquetas open y close. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-consulta número-consulta="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>La consulta en la que entró el visitante. El atributo avanzado y opcional "número-consulta" controla qué cadena de consulta numerada se genera con esta etiqueta. Por ejemplo, <span class="codeph"> &lt;search-consulta consulta-número=1&gt; </span> genera el contenido del parámetro <span class="codeph"> sp_q_1 </span> cgi. Si no se especifica "número-consulta" o si el número-consulta es "0", se mostrará la consulta principal ( <span class="codeph"> sp_q </span>). El atributo opcional "encoding" controla si el resultado es HTML codificado, JavaScript codificado, Perl codificado, URL codificado o no, para que se muestre en la página de resultados. El valor predeterminado de "encoding" es "html". Normalmente, no es necesario especificar el atributo de codificación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-total&gt; </span> </p> </td> 
   <td colname="col2"> <p>Recuento total de resultados para esta búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Recuento de resultados informados para esta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lower&gt; </span> </p> </td> 
   <td colname="col2"> <p>El número del primer resultado registrado para esta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-top&gt; </span> </p> </td> 
   <td colname="col2"> <p>El número del último resultado registrado para esta página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-prev-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Número de resultados informados para la página anterior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>10 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Número de resultados informados para la página siguiente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>11 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-time&gt; </span> </p> </td> 
   <td colname="col2"> <p>Tiempo en segundos para esta búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>12 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-logo&gt; </span> </p> </td> 
   <td colname="col2"> <p>El HTML del logotipo de búsqueda configurado para su cuenta, si existe. Este logotipo es la imagen que da crédito a la búsqueda o comercialización del sitio </p> <p>La mayoría de las cuentas no tienen un logotipo de búsqueda asociado en este momento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>13 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-collection all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Recopilación de resultados para esta búsqueda. El atributo opcional "all" se utiliza para dar el nombre de la colección que representa el sitio web completo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>14 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-form&gt;...&lt;/search-form&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserta las etiquetas de inicio y fin del formulario. Inserta el método y los atributos de acción en la etiqueta del formulario de inicio. Acepta atributos adicionales, incluido el atributo dir="RTL" para el lenguaje, así como los atributos "name" y "onSubmit" relacionados con JavaScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>15 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-account&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserta una etiqueta de entrada de formulario que especifica el número de cuenta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>16 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-Gallery&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserta una etiqueta de entrada de formulario que especifica el número de galería. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>17 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-consulta número-consulta="XX"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserta una etiqueta de entrada de formulario que especifica la cadena de consulta. El atributo avanzado y opcional "número de consulta" controla qué consulta numerada se utiliza para la etiqueta de entrada del formulario. Por ejemplo, <span class="codeph"> &lt;search-input-consulta número-consulta=1&gt; </span> genera una etiqueta de entrada de formulario para la <span class="codeph"> consulta sp_q_1 </span> . Si no se especifica "número-consulta" o si "número-consulta" es "0", se inserta una etiqueta de entrada para la consulta principal <span class="codeph"> sp_q </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>18 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input-collection all="name"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserta una etiqueta de selección de formulario y el código HTML asociado que muestran el menú de selección de colecciones. El atributo opcional "all" se utiliza para dar el nombre de la colección que representa el sitio web completo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>19 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-lt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserta el resultado de una de las etiquetas de plantilla de búsqueda dentro de otras etiquetas HTML o de plantilla en la página de resultados. <span class="codeph"> &lt;search-lt&gt; </span> inserta un carácter menor que. El uso de <span class="codeph"> &lt;search-lt&gt; </span> y <span class="codeph"> &lt;search-gt&gt; </span> proporciona una manera de escapar la definición de una etiqueta para que pueda utilizar las etiquetas de plantilla de búsqueda como valores de atributos. Cuando la plantilla se procesa como respuesta a una búsqueda, un signo menor que (&lt;) reemplaza la etiqueta <span class="codeph"> &lt;search-lt&gt; </span> . Por ejemplo: <span class="codeph"> &lt;search-link&gt; </span> es equivalente a <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>20 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-gt&gt; </span> </p> </td> 
   <td colname="col2"> <p>Inserta el resultado de una de las etiquetas de plantilla de búsqueda dentro de otras etiquetas HTML o de plantilla en la página de resultados. <span class="codeph"> &lt;search-gt&gt; </span> inserta un bueno carácter. El uso de <span class="codeph"> &lt;search-lt&gt; </span> y <span class="codeph"> &lt;search-gt&gt; </span> proporciona una forma de escapar la definición de una etiqueta para que pueda utilizar otras etiquetas de plantilla como valores de atributo. Cuando la plantilla se procesa como respuesta a una búsqueda, un signo bueno (&gt;) reemplaza la etiqueta <span class="codeph"> &lt;search-gt&gt; </span> . Por ejemplo: <span class="codeph"> &lt;search-link&gt; </span> es equivalente a <span class="codeph"> &lt;search-lt&gt;a href="&lt;search-url&gt;"&lt;search-gt&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>21 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-param name="param-name" length="XX" encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Devuelve el valor del parámetro cgi denominado "param-name" de la solicitud de búsqueda actual. El atributo opcional "encoding" controla si el resultado es HTML codificado, JavaScript codificado, Perl codificado, URL codificado o no, para que se muestre en la página de resultados. El valor predeterminado de "encoding" es "html". Normalmente, no es necesario especificar el atributo de codificación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>22 </p> </td> 
   <td colname="col1"> <p> 
     <!--NEW for S&P 8.17.0 release on October 30 2014--> <span class="codeph"> &lt;search-trace encoding="html/javascript/json/perl/url/none"&gt; </span> </p> </td> 
   <td colname="col2"> 
    <!--<p>This global core search template tag outputs a representation of the submitted core search query, including any "fuzzy-search" query term expansions that happen by way of synonyms, sound-alikes, and so forth. </p>--> <p>El <span class="codeph"> atributo de codificación </span> es opcional; el valor predeterminado es <span class="codeph"> json </span>. </p> <p> <p>Nota:  Esta etiqueta solo tiene resultados si <span class="codeph"> sp_trace=1 </span> se especifica con los parámetros de consulta de búsqueda principales. </p> </p> <p>Consulte la fila 48 de la tabla que se encuentra en los parámetros <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"></a>CGI de búsqueda back-end. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Etiquetas de vínculos de anclaje de plantilla {#section_3A51D27616C541E2B818CC52B2B856BA}

Las etiquetas siguientes provocan que un vínculo de anclaje rodee el HTML entre ellas. Cuando se hace clic en él, el vínculo de anclaje solicita que se muestre otra página de resultados. El atributo opcional &quot;count&quot; solicita que se muestren muchos resultados en la página. Si no se especifica, se utiliza el recuento solicitado en la página actual. El atributo &quot;URL&quot; avanzado y opcional controla el dominio al que se dirige el vínculo asociado. De forma predeterminada, el dominio es `https://search.atomz.com/search/`, pero puede cambiarlo mediante el atributo URL.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-next URL="https://search.yourdomain.com/search/"&gt;... &lt;/search-next&gt; </span> </p> <p> <span class="codeph"> &lt;search-prev URL="https://search.yourdomain.com/search/"&gt;... &lt;/search-prev&gt; </span> </p> </td> 
   <td colname="col2"> <p>Muestra la página siguiente o anterior de los resultados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-date URL="https://search.yourdomain.com/search/"&gt; ... &lt;/search-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-sort-by-score URL="https://search.yourdomain.com/search/"&gt;... &lt;/search-sort-by-score&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ordena los resultados por fecha o por relevancia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-show-summaries URL="https://search.yourdomain.com/search/"&gt;... &lt;/search-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-hide-summaries URL="https://search.yourdomain.com/search/"&gt;... &lt;/search-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>Muestra u oculta los resúmenes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Etiquetas condicionales de plantilla {#section_18D9BC66DE484881932FD2F7EA9D170D}

Etiquetas que permiten incluir HTML condicionalmente entre ellas.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-results&gt;... &lt;/search-if-results&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-results&gt; ...&lt;/search-if-not-results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen HTML si la página actual contiene algún resultado de búsqueda (o no). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-prev-count&gt;... &lt;/search-if-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-prev-count&gt; ... &lt;/search-if-not-prev-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-next-count&gt; ... &lt;/search-if-next-count&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-next-count&gt; ... &lt;/search-if-not-next-count&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen HTML si la página anterior o la página siguiente tienen algún resultado (o ninguno) asociado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-score&gt; ... &lt;/search-if-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-score&gt; ... &lt;/search-if-not-sort-by-score&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-sort-by-date&gt; ... &lt;/search-if-sort-by-date&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-date&gt; ... &lt;/search-if-not-sort-by-date&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen HTML si la página actual está, o no, ordenada por relevancia o por fecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-show-summaries&gt; ... &lt;/search-if-show-summaries&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-hide-summaries&gt; ... &lt;/search-if-hide-summaries&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen HTML si la página actual muestra u oculta resúmenes. Puede utilizar estas etiquetas para incluir o excluir cualquier parte del resultado de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-input-collection&gt;... &lt;/search-if-input-collection&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-input-collection&gt;... &lt;/search-if-not-input-collection&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen HTML si se especificó una colección en la generación de resultados de búsqueda para la página actual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>6 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-advanced&gt;... &lt;/search-if-advanced&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-advanced&gt; ... &lt;/search-if-not-advanced&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen HTML si se especificó el parámetro <span class="codeph"> sp_advanced=1 </span> CGI para la consulta de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>7 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-bad-param name="parameter-name"&gt; ... &lt;/search-if-bad-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-bad-param name="parameter-name"&gt; ... &lt;/search-if-not-bad-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas incluyen o excluyen el HTML entre ellas si el parámetro dado no es válido o no lo es. </p> <p>Actualmente solo se admite el parámetro <span class="codeph"> sp_q_location[_#] </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>8 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-param name="param-name" value="param-value"&gt;&gt; ... &lt;/search-if-param&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-param name="param-name" value="param-value"&gt;&gt; ... &lt;/search-if-not-param&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas avanzadas incluyen el HTML entre ellas en función de si el parámetro CGI especificado en el atributo "name" tiene el valor especificado en el atributo "value". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>9 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-if-sort-by-field name="field-name"&gt; ... &lt;/search-if-sort-by-field&gt; </span> </p> <p> <span class="codeph"> &lt;search-if-not-sort-by-field name="field-name"&gt; ... &lt;/search-if-not-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas avanzadas incluyen el HTML entre ellas si la página actual está ordenada o no por el nombre de campo determinado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Etiquetas de control de formulario de plantilla {#section_45AFC414ACA74825B72FEAA8456F8DD2}

Etiquetas que permiten controlar el estado de selección predeterminado para casillas de verificación, botones de radio y cuadros de lista dentro de una `<form>` plantilla de búsqueda.

<table> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Etiqueta </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-input&gt; </span> </p> </td> 
   <td colname="col2"> <p>Se utiliza en una plantilla en lugar de una etiqueta <span class="codeph"> &lt;input&gt; </span> . Cuando se escribe la etiqueta en el explorador, la palabra <span class="codeph"> input </span> reemplaza la entrada de <span class="codeph"> búsqueda </span> y toda la demás información de la etiqueta se muestra tal cual. Además, si el <span class="codeph"> nombre </span> especificado en la etiqueta aparece como un parámetro CGI y si el <span class="codeph"> valor </span> especificado en la etiqueta es el valor para ese parámetro CGI, la palabra <span class="codeph"> check </span> se agrega al final de la etiqueta . De este modo, puede hacer que el estado predeterminado del botón de radio o la casilla de verificación en el resultado de búsqueda sea el mismo que la consulta actual. </p> <p>Por ejemplo, el código HTML de una casilla de verificación puede tener el siguiente aspecto: </p> <p> <span class="codeph"> &lt;input type=checkname="sp_w" value="exacto"&gt;No hay coincidencia de sonido </span> </p> <p>El código de plantilla correspondiente para esa casilla de verificación es el siguiente: </p> <p> <span class="codeph"> &lt;search-input type=checkname="sp_w" value="exacto"&gt;No hay coincidencia de sonido </span> </p> <p>Si la cadena del parámetro CGI para la consulta contiene <span class="codeph"> sp_w=exacto </span>, la etiqueta escrita en el navegador con los resultados de búsqueda tendrá el siguiente aspecto (la palabra <span class="codeph"> check </span> se inserta al final de la etiqueta): </p> <p> <span class="codeph"> &lt;input type=checkname="sp_w" value="exacto" marcado&gt;No hay coincidencia de sonido </span> </p> <p>Si la cadena del parámetro CGI para la consulta no contiene <span class="codeph"> sp_w=exacto </span>, la etiqueta escrita en el navegador con los resultados de búsqueda tendrá el siguiente aspecto (la palabra <span class="codeph"> check </span> no aparece en la etiqueta): </p> <p> <span class="codeph"> &lt;input type=checkname="sp_w" value="exacto"&gt;No hay coincidencia de sonido </span> </p> <p>La etiqueta <span class="codeph"> &lt;search-input&gt; </span> resulta útil para colocar casillas de verificación y botones de radio en la plantilla de búsqueda. Si tiene casillas de verificación o botones de opción que desea agregar al <span class="codeph"> &lt;formulario&gt; </span> en la plantilla de búsqueda, utilice <span class="codeph"> &lt;search-input...&gt; </span> en lugar de <span class="codeph"> &lt;input...&gt; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-select&gt; ... &lt;/search-select&gt; </span> </p> <p> <span class="codeph"> &lt;search-option&gt;... &lt;/search-option&gt; </span> </p> </td> 
   <td colname="col2"> <p>Los cuadros de lista desplegable de una etiqueta <span class="codeph"> &lt;form&gt; </span> se inician con una etiqueta <span class="codeph"> &lt;select&gt; </span> y finalizan con una etiqueta <span class="codeph"> &lt;/select&gt; </span> . El <span class="codeph"> nombre </span> del parámetro CGI asociado se muestra dentro de la etiqueta <span class="codeph"> &lt;select&gt; </span> . Después de la etiqueta <span class="codeph"> &lt;select&gt; </span> hay una lista de etiquetas <span class="codeph"> &lt;option&gt; </span> que especifica los valores que se mostrarán dentro del cuadro lista. </p> <p>Las etiquetas <span class="codeph"> &lt;search-select&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span>, <span class="codeph"> &lt;search-option&gt; </span>y <span class="codeph"> &lt;/search-option&gt; </span> proporcionan una funcionalidad similar a la etiqueta <span class="codeph"> &lt;search-input&gt; </span> . Es decir, la palabra <span class="codeph"> seleccionada </span> se agrega automáticamente al final de la etiqueta <span class="codeph"> &lt;option&gt; </span> enviada al explorador si el <span class="codeph"> nombre </span> en la etiqueta <span class="codeph"> &lt;search-select&gt; </span> se enumera como parámetro CGI y si el <span class="codeph"> valor </span> <span class="codeph"> </span> <span class="codeph"> </span> del parámetro CGI se enumera como valor en una etiqueta concreta &lt;search-option&gt; . De este modo, puede hacer que la opción predeterminada del cuadro de lista en el resultado de búsqueda sea la misma que la consulta actual. </p> <p>Por ejemplo, un cuadro de lista típico tiene el siguiente aspecto: </p> <p> <code class="syntax html"> &lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;/select&gt; </code> </p> <p>El código de plantilla correspondiente para ese cuadro de lista es el siguiente: </p> <p> <code class="syntax html"> &lt;search-select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;search-option&nbsp;value="any"&gt;Anywhere&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="title"&gt;Title&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="desc"&gt;Description&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="keys"&gt;Keywords&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="body"&gt;Body&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="url"&gt;URL&lt;/search-option&gt; 
      &lt;search-option&nbsp;value="target"&gt;Target&lt;/search-option&gt; 
      &lt;/search-select&gt; </code> </p> <p>Si tiene cuadros de lista que desea agregar al <span class="codeph"> &lt;formulario&gt; </span> en la plantilla de búsqueda, utilice <span class="codeph"> &lt;search-select...&gt; </span> en lugar de <span class="codeph"> &lt;select...&gt; </span>, <span class="codeph"> &lt;/search-select&gt; </span> en lugar de <span class="codeph"> &lt;/select&gt; </span><span class="codeph"> </span> <span class="codeph"> </span><span class="codeph"> </span> <span class="codeph"> </span>, &lt;search-option....&gt; en lugar de la &lt;opción.&gt; , y la &lt;/opción de búsqueda &lt;/lugar de los vínculos de búsqueda &lt;.&gt;./option&gt;. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-sort-by-field name="field-name" count="XX"&gt; ... &lt;/search-sort-by-field&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas etiquetas avanzadas crean un vínculo de anclaje alrededor del HTML entre ellas. Cuando se hace clic en este anclaje, se muestra una página de resultados ordenados en un campo determinado. El atributo opcional <span class="codeph"> count </span> especifica el número de resultados que se mostrarán en la página de resultados. Si <span class="codeph"> se omite </span> count, se utiliza el recuento utilizado en la página actual. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cadenas de formato de fecha {#section_4BBDBBEF2B96414497617CD4B52D96E4}

Puede utilizar las siguientes especificaciones de conversión en cadenas de formato de fecha:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Cadena de formato de fecha </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%Una </p> </td> 
   <td colname="col2"> <p> Coincide con la representación nacional del nombre completo del día de la semana, por ejemplo, "lunes". La configuración en <span class="uicontrol"> Lingüística </span> &gt; <span class="uicontrol"> Palabras e idiomas </span> &gt; <span class="uicontrol"> Idioma </span> determina la representación nacional. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Acerca de palabras e idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> Coincide con la representación nacional del nombre abreviado del día de la semana, donde la abreviatura es de los tres primeros caracteres, por ejemplo "Mon". La configuración en <span class="uicontrol"> Lingüística </span> &gt; <span class="uicontrol"> Palabras e idiomas </span> &gt; <span class="uicontrol"> Idioma </span> determina la representación nacional. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Acerca de palabras e idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> Coincide con la representación nacional del nombre completo del mes, por ejemplo "Junio". La configuración en <span class="uicontrol"> Lingüística </span> &gt; <span class="uicontrol"> Palabras e idiomas </span> &gt; <span class="uicontrol"> Idioma </span> determina la representación nacional. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Acerca de palabras e idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> Coincide con la representación nacional del nombre abreviado del mes, donde la abreviatura es de los tres primeros caracteres, por ejemplo "Jun". La configuración en <span class="uicontrol"> Lingüística </span> &gt; <span class="uicontrol"> Palabras e idiomas </span> &gt; <span class="uicontrol"> Idioma </span> determina la representación nacional. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Acerca de palabras e idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p>Equivalente a "%m/%d/%y", por ejemplo "25/07/13". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> Coincide con el día del mes como un número decimal (01-31). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> Coincide con el día del mes como un número decimal (1-31). Un espacio en blanco precede a un solo dígito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> Coincide con el reloj de 24 horas como número decimal (00-23). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> Coincide con la representación nacional del nombre abreviado del mes, donde la abreviatura es de los tres primeros caracteres, por ejemplo "Jun" (el mismo que %b). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> Coincide con el reloj de 12 horas como número decimal (01-12). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> Coincide con el día del año como número decimal (001-366). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> Coincide con el (reloj de 24 horas como número decimal (0-23). Un espacio en blanco precede a un solo dígito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> Coincide con el reloj de 12 horas como número decimal (1-12). Un espacio en blanco precede a un solo dígito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> Coincide con el minuto como un número decimal (00-59). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> Coincide con el mes como número decimal (01-12). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> Coincide con la representación nacional de "ante meridiem" o "post meridiem", según proceda, por ejemplo, "PM". La configuración en <span class="uicontrol"> Lingüística </span> &gt; <span class="uicontrol"> Palabras e idiomas </span> &gt; <span class="uicontrol"> Idioma </span> determina la representación nacional. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Acerca de palabras e idioma</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p>Equivalente a "%H:%M", por ejemplo, "13:23". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p>Equivalente a "%I:%M:%S %p", por ejemplo, "01:23:45 PM". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> Coincide con el segundo como número decimal (00-60). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p>Equivalente a "%H:%M:%S", por ejemplo, "13:26:47". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> Coincide con el número de semana del año (domingo como primer día de la semana) como número decimal (00-53). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p>Equivalente a "%e-%b-%Y", por ejemplo, "25-Jul-2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y </p> </td> 
   <td colname="col2"> <p> Coincide con el año con el siglo como número decimal, por ejemplo, "2013". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> Coincide con el año sin siglo como número decimal (00-99). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> Coincide con el nombre del huso horario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> coincide "%". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Identificadores de idioma {#section_0490DECC00E34691ADE5A9ED90A6D911}

La siguiente tabla contiene los identificadores de idioma de cada idioma admitido. Puede utilizar estos identificadores como valores para el atributo opcional &quot;language&quot; en las siguientes etiquetas de plantilla:

* `search-date` y `search-display-field`.

   Consulte Etiquetas [de cadena de bucle](../c-appendices/c-templates.md#section_80D68334E8D04A33937A6E58ABAAA320)Results.

* `search-field-value-list` Consulte Etiquetas [de lista de valores de campo](../c-appendices/c-templates.md#section_D3298B5F976447DBA0032B883DCC91B1).

* `search-field-value` Consulte Etiquetas [de bucle de lista de valor de campo](../c-appendices/c-templates.md#section_0717FA09F0FC449CB916883B0500A60E).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Idioma  </p> </th> 
   <th colname="col2" class="entry"> <p>Identificador de idioma </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Búlgaro (Bulgaria) </p> </td> 
   <td colname="col2"> <p> bg_BG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chino (China) </p> </td> 
   <td colname="col2"> <p> zh_CN </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chino (Hong Kong) </p> </td> 
   <td colname="col2"> <p> zh_HK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chino (Singapur) </p> </td> 
   <td colname="col2"> <p>zh_SG </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chino (Taiwán) </p> </td> 
   <td colname="col2"> <p> zh_TW </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Checo (República Checa) </p> </td> 
   <td colname="col2"> <p> cs_CZ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Danés (Dinamarca) </p> </td> 
   <td colname="col2"> <p> da_DK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Holandés (Bélgica) </p> </td> 
   <td colname="col2"> <p> nl_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Holandés (Países Bajos) </p> </td> 
   <td colname="col2"> <p> nl_NL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglés (Australia) </p> </td> 
   <td colname="col2"> <p> en_AU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglés (Canadá) </p> </td> 
   <td colname="col2"> <p> en_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglés (Buena Gran Bretaña) </p> </td> 
   <td colname="col2"> <p> en_GB </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Inglés (Estados Unidos) </p> </td> 
   <td colname="col2"> <p> en_US </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francés (Bélgica) </p> </td> 
   <td colname="col2"> <p> fr_BE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francés (Canadá) </p> </td> 
   <td colname="col2"> <p>fr_CA </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Finés (Finlandia) </p> </td> 
   <td colname="col2"> <p> fi_FI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francés (Francia) </p> </td> 
   <td colname="col2"> <p> fr_FR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Francés (Suiza) </p> </td> 
   <td colname="col2"> <p> fr_CH </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Alemán (Austria) </p> </td> 
   <td colname="col2"> <p> de_AT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Alemán (Alemania) </p> </td> 
   <td colname="col2"> <p> de_DE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Alemán (Suiza) </p> </td> 
   <td colname="col2"> <p> (de_CH) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Griego (Grecia) </p> </td> 
   <td colname="col2"> <p> Alemán </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gaélico irlandés (Irlanda) </p> </td> 
   <td colname="col2"> <p> ・_IE </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Italiano (Italia) </p> </td> 
   <td colname="col2"> <p> it_IT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>es japonés (Japón) </p> </td> 
   <td colname="col2"> <p> ja_JP </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Coreano (Corea) </p> </td> 
   <td colname="col2"> <p> ko_KR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Noruego (Noruega) </p> </td> 
   <td colname="col2"> <p> coreano </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Polaco (Polonia) </p> </td> 
   <td colname="col2"> <p> pl_PL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Portugués (Brasil) </p> </td> 
   <td colname="col2"> <p> pt_BR </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Portugués (Portugal) </p> </td> 
   <td colname="col2"> <p> Norteamérica_PT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ruso (antigua Unión Soviética) </p> </td> 
   <td colname="col2"> <p> ru_SU </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Eslovaco (Eslovaquia) </p> </td> 
   <td colname="col2"> <p> sk_SK </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Eslovaco (Eslovenia) </p> </td> 
   <td colname="col2"> <p>sl_SI </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Español (México) </p> </td> 
   <td colname="col2"> <p> es_MX </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Español (España) </p> </td> 
   <td colname="col2"> <p> es_ES </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sueco (Suecia) </p> </td> 
   <td colname="col2"> <p> sv_SE </p> </td> 
  </tr> 
 </tbody> 
</table>

## Especificación del encabezado HTTP de tipo de contenido {#section_AEED823E9938448A9EDB2F286D9CFD90}

Puede especificar el encabezado de respuesta HTTP Content-Type mediante la siguiente etiqueta:

`<search-content-type-header [content="MIME-type"] [charset="charset-name"]>`

Los atributos `content` y `charset` son opcionales. Esta etiqueta debe aparecer lo antes posible en la plantilla. También se recomienda que aparezca antes `<search-html-meta-charset>` o `<search-xml-decl>`, ya que afecta al comportamiento de dichas etiquetas.

Si no especifica el `content` atributo, el valor de `MIME-type` predeterminado es el valor que se establece en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**. Si especifica un `content` atributo, se utiliza como `content` atributo predeterminado para la `<search-html-meta-charset>` etiqueta.

Si no especifica el `charset` atributo, no se escribe ningún `charset` valor en el `content-type` encabezado.

Si especifica `charset="1"` entonces el valor real para `charset-name` es el valor del parámetro `sp_f` CGI. Si no se envía ningún parámetro `sp_f` CGI con la búsqueda, el valor real de `charset-name` se lee en la configuración de la cuenta. Puede vista o cambiar el conjunto de caracteres asociado a su cuenta en **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Consulte [Configuración de la información](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)personal del usuario.

Puede elegir un nombre de conjunto de caracteres específico enumerándolo como el `charset` valor, como `charset="iso-8859-1"` o `charset="Shift-JIS"`.

Si especifica un `charset` atributo, se utilizará como `charset` atributo predeterminado para las etiquetas `<search-html-meta-charset>` y `<search-xml-decl>` , así como como como como resultado en el `content-type` encabezado.

## Especificación de un conjunto de caracteres en una plantilla HTML {#section_E0D1816ABB5846BEBE9C26D5980CCBE6}

Las plantillas de resultados de búsqueda HTML predeterminadas especifican el conjunto de caracteres asociado a la cuenta actual mediante la etiqueta siguiente:

`<search-html-meta-charset [content="MIME-type"] [charset="charset-name"]>`

Los atributos de contenido y de conjunto de caracteres son opcionales. Esta etiqueta debe aparecer en la sección HTML `<head>` de la plantilla. Esta etiqueta da como resultado la siguiente etiqueta en la página HTML generada a partir de la plantilla:

`<meta http-equiv="content-type" content="MIME-type; charset=charset-name">`

Si no especifica el atributo content, el valor real de `MIME-type` se establece de forma predeterminada en uno de los dos valores. Si la `<search-content-type-header>` etiqueta ha especificado un `content` atributo, se utiliza ese valor. De lo contrario, el valor utilizado es el que se define en la **[!UICONTROL Templates]** ficha > **[!UICONTROL Settings]** > **[!UICONTROL Content Type]** .

Si no especifica el `charset` atributo, el valor real de `charset-name` se establece de forma predeterminada en uno de los dos valores. Si la `<search-content-type-header>` etiqueta ha especificado un `charset` atributo, se utiliza ese valor. De lo contrario, el valor real de `charset-name` se lee en la configuración de la cuenta. Puede vista o cambiar el conjunto de caracteres asociado a su cuenta en **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Consulte [Configuración de la información](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)personal del usuario.

Si especifica `charset="1"` entonces el valor real para `charset-name` es el valor del parámetro `sp_f` CGI. Si no se envía ningún parámetro `sp_f` CGI con la búsqueda, el valor real de `charset-name` es el valor establecido en la `<search-content-type-header>` etiqueta si se especificó o el valor establecido en la configuración de la cuenta.

Puede especificar un nombre de conjunto de caracteres específico, como en `charset="charset-name"`. For example, `charset="iso-8859-1"` or `charset="Shift-JIS"`.

La `<search-html-meta-charset>` etiqueta es opcional. Si lo elimina, el explorador asume los valores predeterminados para `content-type`, que son los siguientes: `content="text/html; charset=ISO-8859-1"`. También puede elegir reemplazar la `<search-html-meta-charset>` etiqueta con su propia `http-equiv` etiqueta.

## Especificación de un conjunto de caracteres en una plantilla XML {#section_17DC31CDCC104F5F8081466B41A96E9D}

La plantilla de resultados de búsqueda XML predeterminada especifica el conjunto de caracteres asociado a la cuenta actual mediante la etiqueta siguiente:

`<search-xml-decl [charset="charset-name"]>`

El `charset` atributo es opcional. Esta etiqueta debe aparecer en la parte superior de la plantilla, pero después de cualquier `<search-content-type-header>` etiqueta. Esta etiqueta tiene como resultado la siguiente etiqueta en el documento XML que se genera a partir de la plantilla:

`<?xml version="1.0" encoding="charset-name" standalone="yes" ?>`

Si no especifica el `charset`, el valor real de `charset-name` se establece de forma predeterminada en uno de los dos valores. Si `<search-content-type-header>` se especifica un `charset` atributo, se utiliza ese valor. De lo contrario, el valor real de `charset-name` se lee en la configuración de la cuenta. Puede vista o cambiar el conjunto de caracteres asociado a su cuenta en **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]** > **[!UICONTROL Character Encoding]**.

Consulte [Configuración de la información](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)personal del usuario.

Si especifica `charset="1"` entonces el valor real para `charset-name` es el valor del parámetro `sp_f` CGI. Si no se envía ningún parámetro `sp_f` CGI con la búsqueda, el valor real de `charset-name` es el valor que se establece en la `<search-content-type-header>` etiqueta si se especificó o el valor que se establece en la configuración de la cuenta.

Puede especificar un nombre de conjunto de caracteres específico, como en `charset="charset-name"`caso de que lo desee. Por ejemplo, `charset="iso-8859-1" or charset="Shift-JIS"`.

Puede elegir reemplazar la `<search-xml-decl>` etiqueta con su propia `?xml` etiqueta.

## Inclusión de una plantilla de búsqueda dentro de otra {#section_7D1FCD3D9E2340C291E354C9720E8BC0}

Para incluir una plantilla de búsqueda en otra, utilice la `<search-include>` etiqueta , estableciendo el atributo de archivo en el nombre del archivo de plantilla que desea incluir como en el siguiente ejemplo:

`<search-include file="seo/seo_search_title.tpl" />`

Los segmentos de plantilla de búsqueda SEO están en la `seo/` subcarpeta y las plantillas de búsqueda normales están en la `templates/` subcarpeta. Solo los archivos .tpl tienen sentido para incluirlos en este contexto.

## Administración de varias plantillas de transporte para el sitio web {#reference_12AAB3B9F4C74C11956F1DBA95714C2F}

Puede controlar la apariencia de los resultados de búsqueda en el sitio web mediante distintas plantillas de transporte de búsqueda para cada área.

<!-- 

r_managing_multiple_templates.xml

 -->

Para lograr este tipo de funcionalidad de búsqueda, puede administrar las plantillas de transporte en la búsqueda y comercialización del sitio. O bien, puede administrar las plantillas de transporte en Publicar. Al igual que la búsqueda y comercialización del sitio, Publicar permite editar, previsualización y publicación de varias plantillas de transporte de búsqueda.

Para configurar los formularios de búsqueda para que utilicen una plantilla de transporte específica (distinta de la predeterminada), utilice el parámetro de `sp_t` consulta. Por ejemplo, supongamos que tiene una plantilla de búsqueda denominada &quot;liquidación&quot; para el área de ventas marcada como &quot;baja&quot; de su sitio web. El formulario de búsqueda HTML estándar se utiliza con el siguiente código de formulario adicional:

`<input type=hidden name="sp_t" value="clearance">`

Cuando un cliente hace clic en un formulario estándar que contiene esta línea de código, se muestra la plantilla de transporte de búsqueda de &quot;liquidación&quot; junto con los resultados de búsqueda.

Consulte [Uso de colecciones en formularios](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)de búsqueda.

Consulte [Uso de marcos con formularios](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consulte [Ejemplo de formulario](../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)de búsqueda avanzada.
