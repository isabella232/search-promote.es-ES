---
description: Puede utilizar Plantillas para administrar las plantillas de presentación y las plantillas de transporte.
solution: Target
title: Acerca de las plantillas
topic-legacy: Design,Site search and merchandising
uuid: f5805d3e-43bf-4e13-95df-b6bd6b762d11
exl-id: 846f34b3-9857-494e-9010-3db0b48412d3
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '2647'
ht-degree: 1%

---

# Acerca de las plantillas{#about-templates}

Puede utilizar **[!UICONTROL Templates]** para administrar las plantillas de presentación y las plantillas de transporte.

## Acerca de las plantillas {#concept_06EB481B14864E18A8AE2BCD1D6EF0B5}

<!-- 

c_about_templates.xml

 -->

Puede agregar, editar, copiar, cambiar el nombre o eliminar plantillas de presentación y plantillas de transporte. Al hacer clic en un nombre de plantilla existente en la tabla Plantillas, este se abre en una ventana del editor (o visor) en la que puede realizar los cambios.

Puede revertir cualquier cambio que realice en las plantillas mediante la función Historial desde la lista desplegable del nombre de la plantilla en la tabla Plantillas.

Puede reducir el peso de la página de una plantilla de presentación marcando la casilla **[!UICONTROL Minimize]** correspondiente de la plantilla en la tabla de plantillas. Al reducir el peso de la página de la plantilla, se minimiza dinámicamente JavaScript y CSS en línea. También puede eliminar espacios en blanco redundantes en el HTML. Minimizar el peso de la página de la plantilla de presentación puede ayudar a ofrecer los resultados de búsqueda más rápido.

Para obtener una vista previa del aspecto de la plantilla minimizada, haga clic en la lista desplegable junto al nombre del archivo y, a continuación, haga clic en **[!UICONTROL Preview minimized]**. Si minimiza la plantilla de presentación principal, asegúrese de habilitar la minimización de plantillas incluidas (con etiqueta `guided-include`) porque esta opción no es heredable.

Aunque minimice una plantilla de presentación, puede editar la versión &quot;sin minimizar&quot; de la misma plantilla.

Puede utilizar las reglas de búsqueda previa, las reglas posteriores a la búsqueda y las reglas empresariales para determinar cuándo utilizar una de las otras plantillas de presentación. Es común tener una regla como &quot;Para cada búsqueda, establezca la plantilla de destino en xxxx&quot;. Con una regla así en su lugar, cuando cambia la plantilla &quot;Predeterminada&quot; en la tabla Plantillas, parece que no tiene ningún efecto.

Consulte [Acerca de las reglas de búsqueda previa](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

Consulte [Acerca de las reglas posteriores a la búsqueda](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

Consulte [Acerca de las reglas comerciales](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Acerca de las plantillas de presentación {#section_ACDDEA5C499E481C828A517C230D4596}

Las plantillas de presentación son plantillas HTML que un cliente ve cuando ve los resultados de su búsqueda en su sitio web.

En la capa de presentación, puede tener una sola plantilla de presentación que presente los resultados de varias búsquedas de varias fuentes. Puede definir tantas plantillas de presentación como desee e incluso definir las plantillas de presentación que comparten otras plantillas mediante comandos `include`. La plantilla de presentación es el lugar donde se unen todos los componentes de diseño, como facetas, menús y rutas de exploración. Para mostrar los distintos componentes de diseño, debe utilizar las etiquetas de plantilla de presentación.

Consulte [Etiquetas de plantillas de presentación](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Cuando tiene más de una plantilla de presentación, define en qué condiciones se utilizan las distintas plantillas de presentación. Puede seleccionar qué plantilla de presentación utilizar en función de los parámetros y cookies CGI entrantes. O puede cambiar la plantilla de presentación que utiliza en función del resultado de una búsqueda anterior.

Cuando utilice varias plantillas de presentación, asegúrese de indicar qué plantilla desea que aparezcan inicialmente los resultados de búsqueda. Puede hacerlo utilizando la columna **[!UICONTROL Default]** de la tabla Plantillas.

## Acerca de las plantillas de transporte {#section_35FD3E8AAA4E4695A737DB7E00C3258B}

Las plantillas de transporte pueden ser plantillas XML o JSON que pasan datos de la búsqueda back-end a la capa de presentación Búsqueda guiada .

De forma predeterminada, la cuenta está configurada para utilizar plantillas de transporte XML. Sin embargo, si prefiere utilizar JSON para pasar sus datos a la Búsqueda guiada, póngase en contacto con el Adobe de consultoría, que le ayudará.

En la capa de presentación, puede tener una sola plantilla de presentación que presente los resultados de varias búsquedas. Cada búsqueda puede utilizar la misma plantilla de transporte o una plantilla de transporte personalizada para pasar los datos a la capa de presentación. Como la plantilla de transporte solo se utiliza para pasar datos a la capa de presentación, no debe tener ningún HTML que se utilice para mostrar los resultados de búsqueda. La plantilla utiliza etiquetas de plantilla de transporte para pasar los resultados de la búsqueda y los resultados para rellenar las facetas. Dentro de estas etiquetas, las etiquetas de plantilla de búsqueda estándar se utilizan para mostrar los valores reales.

Consulte [Buscar etiquetas de plantilla](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

**Etiquetas específicas de la plantilla de transporte XML**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Etiqueta de plantilla de transporte XML </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>Estas son las etiquetas XML raíz que utiliza la capa de presentación para detectar qué debe analizar a partir de la plantilla de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas rodea las etiquetas de plantilla de búsqueda que proporcionan datos de resumen basados en el conjunto de resultados. Normalmente, estas etiquetas contienen etiquetas de búsqueda para el número total de resultados, el resultado más bajo y el resultado más alto. Puede definir cualquier número de campos globales adicionales que desee con la etiqueta <span class="codeph"> general-field </span> . </p> <p> <b>Ejemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;general&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas se envuelve en torno a los resultados de búsqueda, de modo que la Búsqueda guiada sepa dónde buscarlos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas se envuelve alrededor de cada resultado de búsqueda, de modo que la Búsqueda guiada reconoce dónde comienza y finaliza el contenido de un solo resultado de búsqueda. </p> <p> <b>Ejemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="tablename"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Esta etiqueta permite recorrer en bucle cada elemento de una lista de varios valores para obtener un solo resultado. Utilice la etiqueta solo dentro de un resultado. Su principal función es permitirle iterar los atributos que pertenecen a un campo de resultado. </p> <p> <b>Ejemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facets&gt;&lt;/facets&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas pasa los resultados que rellenan las facetas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cada faceta debe tener sus propias etiquetas de faceta donde el parámetro name coincida con el nombre de la faceta. Las etiquetas de búsqueda se utilizan en las etiquetas de facetas para los valores de facetas. </p> <p>Consulte <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" type="concept" format="dita" scope="local"> Acerca de las facetas </a>. </p> <p> <b>Ejemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;facets&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/facets&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestions&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas ajusta las sugerencias Quiso decir para que la Búsqueda guiada reconozca qué nodos XML contienen sugerencias. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestion&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas ajusta cada sugerencia de ¿Quiso decir? </p> <p> <b>Ejemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-if-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;value&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/value&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;count&gt;&lt;search-suggestion-result-count&nbsp;/&gt;&lt;/count&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-if-suggestions&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Etiquetas específicas de plantillas de transporte JSON**

Se sabe que el paso de JSON frente a XML desde el motor de búsqueda es más rápido porque es una carga útil más pequeña y un analizador más rápido. Tenga cuidado, sin embargo, cuando utilice JSON para asegurarse de que lo que resulta sea un JSON estricto porque el analizador no es indulgente.

Si es nuevo en JSON, puede utilizar los siguientes vínculos y ejemplos para ayudarle a empezar:

* Introducción a JSON. Consulte [https://www.json.org/](https://www.json.org/).
* Pruebe el JSON para asegurarse de que sea válido. Consulte [https://jsonlint.com/](https://jsonlint.com/).

**Ejemplo de plantilla JSON**

```
{ 
 "general": 
 { 
  "total" : "<search-total />", 
  "lower" : "<search-lower />", 
  "upper" : "<search-upper />", 
  "rbt-trigger-list" : "<search-rbta-trigger-id-list>", 
  "fields" :  
  [ 
   { 
    "name" : "seo_search_title", 
    "value" : "<search-include file="seo/seo_search_title.tpl" />" 
   }, 
   { 
    "name" : "seo_search_keywords", 
    "value" : "<search-include file="seo/seo_search_keywords.tpl" />" 
   } 
  ] 
 }, 
 
 <search-if-suggestions> 
 "suggestions": 
  [ 
  <search-suggestions> 
  { 
   "suggestion":"<search-suggestion-text />", 
   "count": "<search-suggestion-result-count>" 
  }<search-if-not-last-suggestion>,</search-if-not-last-suggestion> 
  </search-suggestions> 
 ], 
 </search-if-suggestions> 
 
 "facets" : 
 [ 
  { 
   "name" : "leveli", 
   "values" : [ <search-field-value-list name="leveli" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="leveli" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" :"levelii", 
   "values" : [<search-field-value-list name="levelii" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="levelii" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" : "brand", 
   "values" : [<search-field-value-list name="brand" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="brand" quotes="no" sortby="values" data="results" />] 
  }, 
 ], 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    }, 
    { 
     "name" : "title", 
     "value" : "<search-display-field name="title" encoding="json"/>" 
    }, 
    { 
     "name" : "img_url_thumbnail", 
     "value" : "<search-display-field name="img_url_thumbnail" encoding="json"/>" 
    }, 
    { 
     "name" : "description", 
     "value" : "<search-display-field name="description" encoding="json"/>" 
    }, 
    { 
     "name" : "mdi", 
     "value" : "<SEARCH-RBTA-DISPLAY-MDI-FIELD>" 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**Ejemplo de sección de resultados JSON con una tabla de atributos de resultados**

```
{ 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    } 
   ], 
   "tables" : 
   [ 
    { 
     "name" : "downloads", 
     "fields" : 
     [ 
      { 
       "name" : "download_title", 
       "value" : <search-display-field name="download_title" encoding="json"/> 
      }, 
      { 
       "name" : "download_link", 
       "value" : <search-display-field name="download_link" encoding="json"/> 
      } 
     ] 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**Ejemplo de sección de faceta JSON para una faceta con campos asociados**

```
{ 
 facets" : 
 [ 
  { 
   "name" : "t1", 
   "values" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
   "counts" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="results" sortby="values" />], 
   "custom-fields" : 
   [ 
    { 
     "name" : "taxonmyId", 
     "value" : [<search-field-value-list name="tax1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />] 
    } 
   ] 
  } 
 ] 
}
```

**Ejemplo de sección de facetas JSON para facetas asignadas**

```
{ 
  "facets" : 
  [  
   { 
    "name" : "fvalue0", 
                  "dynamic" : 1, 
                  "display-names" : [<search-field-value-list name="fname0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "values" : [<search-field-value-list name="fvalue0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "counts" : [<search-field-value-list name="fvalue0" quotes="no" commas="yes" data="results" sortby="values" />] 
   } 
  ] 
} 
```

## Adición de un nuevo archivo de plantilla de presentación o transporte {#task_73199757B6E748CAA604902FF913F012}

Puede utilizar **[!UICONTROL Add Template]** para agregar plantillas de presentación (.tmpl) o plantillas de transporte (.tpl) a la página [!DNL Templates].

<!-- 

t_adding_a_new_presentation_or_transport_template_file.xml

 -->

**Para agregar una nueva presentación o un archivo de plantilla de transporte**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la página [!DNL Templates], haga clic en **[!UICONTROL Add New Template]**.
1. En el cuadro de diálogo [!DNL Add Template], defina las opciones que desee.

   <!-- 
   
   r_add_template_options.xml
   
   -->

   | Opción | Descripción |
   |--- |--- |
   | Nuevo nombre de archivo | Especifica el nombre de la plantilla que desea agregar. La extensión de archivo adecuada se añade automáticamente al nombre del archivo, según el tipo de plantilla que seleccione.  Las plantillas de presentación tienen una extensión de archivo .tmpl; Las plantillas de transporte tienen una extensión de archivo .tpl. |
   | Nuevo tipo de plantilla | Permite elegir una presentación o una plantilla de transporte que desee añadir.  Consulte [Acerca de las plantillas](../c-about-design-menu/c-about-templates.md). |

   Consulte también [Edición de una presentación o de una plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).
1. Haga clic **[!UICONTROL Add]**.
1. (Opcional) En la página [!DNL Templates], realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una presentación o de una plantilla de transporte {#task_800E0E2265C34C028C92FEB5A1243EC3}

Puede utilizar el Editor de plantillas para ver y editar el contenido de los archivos de plantilla de presentación y transporte.

<!-- 

t_editing_a_template.xml

 -->

Puede editar y probar las plantillas de transporte y presentación organizadas, mientras que los visitantes del sitio web siguen utilizando las versiones activas de las plantillas. La plantilla de ensayo se prueba con la versión de ensayo de la dirección URL del dominio de búsqueda. Por ejemplo, puede probar la plantilla de transporte por etapas ejecutando una consulta por etapas ( `sp_staged=1`) con `sp_t` que esté configurada con el nombre de la plantilla de transporte. Cuando esté satisfecho con el aspecto del diseño, puede utilizar **[!UICONTROL Push Live]** desde el editor de plantillas para activar la plantilla. Una vez publicada la plantilla, los visitantes del sitio empiezan a utilizarla.

Utilice la referencia de la etiqueta de la plantilla de presentación para aprender a conectar la plantilla de presentación a los componentes de Búsqueda guiada, como facetas, rutas de exploración y menús.

Consulte [Etiquetas de plantillas de presentación](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Utilice la referencia de la etiqueta de la plantilla de transporte para obtener más información sobre las etiquetas que se deben utilizar en las plantillas de transporte.

Consulte [Etiquetas de plantillas de transporte](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**[!UICONTROL To edit a presentation or a transport template]**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la página [!DNL Templates], haga clic en una presentación o en un nombre de archivo de plantilla de transporte.
1. En la página [!DNL Template Editor], realice los cambios que desee en las etiquetas y la codificación.

   Tenga cuidado con los cambios que realiza en [!DNL Template Editor]; no existe la función Deshacer. Si realiza un cambio no deseado y desea volver a la versión anterior del archivo, puede hacer clic en **[!UICONTROL Cancel]** para volver a la tabla de plantillas (suponiendo que no guardó ninguno de los cambios hasta ese momento). Si ya ha guardado los cambios, puede utilizar **[!UICONTROL History]** en el editor para revertirlos.
1. (Opcional) Haga clic en **[!UICONTROL Insert Symbol]** para introducir caracteres especiales y símbolos que no tengan claves correspondientes en los teclados en inglés de EE. UU.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Cierre la página Editor de plantillas cuando haya terminado; volverá a la página Plantillas .

## Copia de una presentación o un archivo de plantilla de transporte {#task_B744AB3384C84DD59C33CD25E18C2C90}

Puede utilizar **[!UICONTROL Copy Template]** para ahorrar tiempo duplicando una plantilla de Presentación existente (.tmpl) o una plantilla de Transporte (.tpl) y agregarla a la página Plantillas.

<!-- 

t_copying_a_presentation_or_a_transport_template.xml

 -->

Debe cambiar el nombre de la plantilla, el tipo de plantilla o ambos. Si no realiza ningún cambio, la plantilla no se copia.

Debe tener una plantilla ya agregada para poder copiar una plantilla.

Consulte [Adición de una nueva presentación o archivo de plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012).

**Para copiar una presentación o un archivo de plantilla de transporte**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la página [!DNL Templates], en la lista desplegable junto al nombre de la plantilla que desea copiar, haga clic en **[!UICONTROL Copy]**.
1. En el cuadro de diálogo [!DNL Copy Template], defina una o más de las opciones que desee.
1. Haga clic **[!UICONTROL Copy]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cambio del nombre de una presentación o de un archivo de plantilla de transporte {#task_CC30050FC2DE4898BF44379D8378EB31}

Puede utilizar [!DNL Rename Template] para cambiar el nombre de una plantilla de presentación existente (.tmpl) o una plantilla de transporte (.tpl).

<!-- 

t_renaming_a_presentation_or_a_transport_template_file.xml

 -->

Si lo desea, también puede cambiar el tipo de plantilla.

Debe tener una plantilla ya agregada para cambiar el nombre de una plantilla.

Consulte [Adición de una nueva presentación o archivo de plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012).

**Cambio del nombre de una presentación o de un archivo de plantilla de transporte**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la página [!DNL Templates], en la lista desplegable junto al nombre de la plantilla cuyo nombre desea cambiar, haga clic en **[!UICONTROL Rename]**.
1. En el cuadro de diálogo [!DNL Rename Template], defina una o más de las opciones que desee.
1. Haga clic **[!UICONTROL Rename]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una presentación o un archivo de plantilla de transporte {#task_67E532C2B83A449687737E3B06C5AA58}

Puede utilizar **[!UICONTROL Delete Template]** para eliminar una plantilla de presentación existente (.tmpl) o una plantilla de transporte (.tpl).

<!-- 

t_deleting_a_presentation_or_a_transport_template_file.xml

 -->

Puede que ya tenga una versión correspondiente de la plantilla de ensayo que se inserta en vivo. Si es así, asegúrese de insertar la plantilla eliminada en vivo utilizando **[!UICONTROL Staging]** para que también se elimine del entorno en directo. O bien, puede utilizar **[!UICONTROL Push Live]** en la página Plantillas.

Consulte [Acerca del ensayo](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)

Consulte [Configuración de los escenarios de inserción en vivo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

Debe tener una plantilla ya agregada para poder eliminar una plantilla.

Consulte [Adición de una nueva presentación o archivo de plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

**Eliminar una presentación o un archivo de plantilla de transporte**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la página [!DNL Templates], en la lista desplegable junto al nombre de la plantilla que desea eliminar, haga clic en **[!UICONTROL Delete]**.
1. En el cuadro de diálogo [!DNL Delete Template], haga clic en **[!UICONTROL Delete.]**
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Vista previa de la plantilla de presentación minimizada {#task_1757B6207CC74221AE4BFFE5674D320B}

Puede utilizar **[!UICONTROL Preview minimized]** para ver el aspecto que tendría el peso de página reducido de una plantilla de presentación si decide minimizarlo.

<!-- 

t_previewing_the_presentation_template_minimized.xml

 -->

Si minimiza la plantilla de presentación principal, asegúrese de habilitar la minimización de las plantillas incluidas (con etiqueta de inclusión guiada) porque esta opción no es heredable.

Consulte [Reducción del peso de página de una plantilla de presentación en su...](../c-about-design-menu/c-about-templates.md#task_B09BB3CE89714DEAAE8D9A899CF3009E)

Debe tener una plantilla ya agregada para obtener una vista previa de la plantilla minimizada.

Consulte [Adición de una nueva presentación o archivo de plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

Puede obtener una vista previa del código XML de un archivo de plantilla de transporte.

Consulte [Vista previa del XML de un archivo de plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_58C6C52078E14AD88D2B2F0B3C439AE8)

**Para previsualizar la plantilla de presentación minimizada**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la página [!DNL Templates], en la lista desplegable junto al nombre de una plantilla de presentación, haga clic en **[!UICONTROL Preview minimized]**.

   Utilice la columna **[!UICONTROL Type]** de la tabla Plantillas para ordenar las plantillas por Presentación y Transporte.
1. (Opcional) En la página [!DNL Preview Minimized Template], marque **[!UICONTROL Wrap lines]** para leer las etiquetas dentro de la ventana definida.
1. Haga clic **[!UICONTROL Close]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Reducción del peso de página de una plantilla de presentación en el sitio web {#task_B09BB3CE89714DEAAE8D9A899CF3009E}

Puede reducir el peso de la página de una plantilla de presentación utilizando la opción **[!UICONTROL Minimize]** de la tabla de plantillas.

<!-- 

t_reducing_the_page_weight_of_a_presentation_template.xml

 -->

Al reducir el peso de la página de la plantilla, se minimiza dinámicamente JavaScript y CSS en línea. También puede eliminar espacios en blanco redundantes en el HTML. Minimizar el peso de la página de la plantilla de presentación puede ayudar a ofrecer los resultados de búsqueda más rápido.

También puede obtener una vista previa del aspecto de la plantilla de presentación minimizada utilizando **[!UICONTROL Preview minimized]**.

Consulte [Vista previa de la plantilla de presentación minimizada](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B).

**[!UICONTROL To reduce the page weight of a presentation template on your website]**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la página [!DNL Templates], en la columna [!DNL Minimize], marque la casilla de uno o más archivos de plantilla de presentación que desee insertar como mínimo en el sitio web.

   Utilice la columna **[!UICONTROL Type]** de la tabla [!DNL Templates] para ordenar las plantillas por Presentación y Transporte.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuración del archivo de plantilla de presentación predeterminado para usar en el sitio web {#task_C1E8CE817E4D43E096167A347C54DD53}

Cuando tiene varias plantillas de presentación, puede indicar qué plantilla se utilizará inicialmente para mostrar los resultados de la búsqueda.

<!-- 

t_setting_the_default_presentation_template_file_to_use.xml

 -->

Puede utilizar las reglas de prebúsqueda, las reglas posteriores a la búsqueda y las reglas empresariales para determinar cuándo se debe utilizar una de las otras plantillas de presentación.

Consulte [Acerca de las reglas de búsqueda previa](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

Consulte [Acerca de las reglas posteriores a la búsqueda](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

Consulte [Acerca de las reglas comerciales](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

Es común tener una regla como &quot;Para cada búsqueda, establezca la plantilla de presentación de destino en xxxx&quot;. Con una regla de este tipo en su lugar, el cambio de la plantilla &quot;predeterminada&quot; en la página Plantillas parecerá no tener ningún efecto.

**[!UICONTROL To set the default presentation template file to use on your website]**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la página [!DNL Templates], en la columna [!DNL Default], haga clic en el botón de opción del archivo de plantilla de presentación correspondiente que desea que sea el predeterminado.

   Utilice la columna **[!UICONTROL Type]** de la tabla [!DNL Templates] para ordenar las plantillas por Presentación y Transporte.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Vista previa del XML de un archivo de plantilla de transporte {#task_58C6C52078E14AD88D2B2F0B3C439AE8}

Puede utilizar [!DNL Preview] para revisar el XML de una plantilla de transporte que haya agregado.

<!-- 

t_previewing_the_xml_of_a_transport_template_file.xml

 -->

Debe tener una plantilla de transporte ya agregada para obtener una vista previa del XML de la plantilla.

Consulte [Adición de una nueva presentación o archivo de plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012).

Puede obtener una vista previa de los archivos de plantilla de presentación minimizados para ver su peso de página reducido.

Consulte [Vista previa de la plantilla de presentación minimizada](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B).

**Para obtener una vista previa del XML de un archivo de plantilla de transporte**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la página [!DNL Templates], en la lista desplegable junto al nombre de una plantilla de transporte, haga clic en **[!UICONTROL Preview]**.

   Utilice la columna **[!UICONTROL Type]** de la tabla [!DNL Templates] para ordenar las plantillas por Presentación y Transporte.
1. Cierre la ventana de visualización y vuelva a [!DNL site search/merchandising].
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
