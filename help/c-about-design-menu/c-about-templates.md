---
description: Puede utilizar las plantillas para administrar las plantillas de presentación y las plantillas de transporte.
seo-description: Puede utilizar las plantillas para administrar las plantillas de presentación y las plantillas de transporte.
seo-title: Acerca de las plantillas
solution: Target
title: Acerca de las plantillas
topic: Design,Site search and merchandising
uuid: f5805d3e-43bf-4e13-95df-b6bd6b762d11
translation-type: tm+mt
source-git-commit: 60cedaac1846e384a37699a42bf7fda33828e1c0

---


# Acerca de las plantillas{#about-templates}

Puede utilizar **[!UICONTROL Templates]** para administrar las plantillas de presentación y las plantillas de transporte.

## Acerca de las plantillas {#concept_06EB481B14864E18A8AE2BCD1D6EF0B5}

<!-- 

c_about_templates.xml

 -->

Puede agregar, editar, copiar, cambiar el nombre o eliminar plantillas de presentación y plantillas de transporte. Al hacer clic en un nombre de plantilla existente en la tabla Plantillas, se abre en una ventana de editor (o visor) en la que puede realizar los cambios.

Puede revertir cualquier cambio que realice en las plantillas mediante la función Historial de la lista desplegable del nombre de la plantilla en la tabla Plantillas.

Puede reducir el grosor de página de una plantilla de presentación marcando la casilla de verificación correspondiente de la plantilla en la **[!UICONTROL Minimize]** tabla de la plantilla. Al reducir el grosor de página de la plantilla, se minimiza dinámicamente JavaScript y CSS en línea. También puede eliminar espacios en blanco redundantes en el HTML. Minimizar el grosor de página de la plantilla de presentación puede ayudar a ofrecer los resultados de búsqueda más rápido.

Para obtener una vista previa del aspecto de la plantilla minimizada, haga clic en la lista desplegable situada junto al nombre del archivo y, a continuación, haga clic en **[!UICONTROL Preview minimized]**. Si minimiza la plantilla de presentación principal, asegúrese de que no ha olvidado habilitar la minimización de plantillas incluidas (con `guided-include` etiquetas) porque esta opción no es heredable.

Incluso si minimiza una plantilla de presentación, puede editar la versión &quot;sin minimizar&quot; de la misma plantilla.

Puede utilizar las reglas de búsqueda previa, las reglas de búsqueda posterior y las reglas comerciales para determinar cuándo utilizar una de las otras plantillas de presentación. Es común tener una regla como &quot;Para cada búsqueda, establezca la plantilla de objetivo en xxxx&quot;. Con una regla de este tipo implementada, cuando se cambia la plantilla &quot;Predeterminada&quot; en la tabla Plantillas, parece que no tiene ningún efecto.

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

See [About Post-Search Rules](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Acerca de las plantillas de presentación {#section_ACDDEA5C499E481C828A517C230D4596}

Las plantillas de presentación son plantillas HTML que un cliente ve cuando ve los resultados de la búsqueda en su sitio web.

En la capa de presentación, puede tener una sola plantilla de presentación que presente los resultados de varias búsquedas de distintas fuentes. Puede definir tantas plantillas de presentación como desee e incluso definir plantillas de presentación que otras plantillas compartan mediante `include` comandos. En la plantilla de presentación se agrupan todos los componentes de diseño, como facetas, menús y rutas de exploración. Para mostrar los distintos componentes de diseño, debe utilizar etiquetas de plantilla de presentación.

Consulte Etiquetas de plantillas [de presentación](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Cuando tiene más de una plantilla de presentación, puede definir en qué condiciones se utilizan las distintas plantillas de presentación. Puede seleccionar qué plantilla de presentación utilizar en función de los parámetros y cookies CGI entrantes. O bien, puede cambiar la plantilla de presentación que utiliza en función del resultado de una búsqueda anterior.

Cuando utilice varias plantillas de presentación, asegúrese de indicar qué plantilla desea que aparezcan inicialmente los resultados de búsqueda. Puede hacerlo utilizando la **[!UICONTROL Default]** columna de la tabla Plantillas.

## Acerca de las plantillas de transporte {#section_35FD3E8AAA4E4695A737DB7E00C3258B}

Las plantillas de transporte pueden ser plantillas XML o JSON que pasan datos de la búsqueda back-end a la capa de presentación Búsqueda guiada.

De forma predeterminada, su cuenta está configurada para utilizar plantillas de transporte XML. Sin embargo, si prefiere utilizar JSON para pasar los datos a la búsqueda guiada, póngase en contacto con el consultor de Adobe, que le ayudará.

En la capa de presentación, puede tener una sola plantilla de presentación que presente los resultados de varias búsquedas. Cada búsqueda puede utilizar la misma plantilla de transporte o una plantilla de transporte personalizada para pasar los datos a la capa de presentación. Dado que la plantilla de transporte solo se utiliza para pasar datos a la capa de presentación, no debe tener ningún código HTML que se utilice para mostrar los resultados de la búsqueda. La plantilla utiliza etiquetas de plantilla de transporte para pasar los resultados de la búsqueda y los resultados para rellenar las facetas. Dentro de estas etiquetas, las etiquetas de plantilla de búsqueda estándar se utilizan para mostrar los valores reales.

Consulte [Buscar etiquetas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de plantilla.

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
   <td colname="col2"> <p>Son las etiquetas XML raíz que utiliza la capa de presentación para detectar lo que debe analizar a partir de la plantilla de transporte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas rodea las etiquetas de plantilla de búsqueda que proporcionan datos de resumen basados en el conjunto de resultados. Normalmente, estas etiquetas contienen etiquetas de búsqueda para el número total de resultados, el resultado más bajo y el resultado más alto. Puede definir cualquier número de campos globales adicionales que desee con la <span class="codeph"> etiqueta de campo general </span> . </p> <p> <b>Ejemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;general&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas se envuelve en torno a los resultados de búsqueda, de modo que la búsqueda guiada sepa dónde buscarlos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas se envuelve alrededor de cada resultado de búsqueda, de modo que la búsqueda guiada reconoce dónde comienza y termina el contenido de un único resultado de búsqueda. </p> <p> <b>Ejemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
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
   <td colname="col2"> <p>Esta etiqueta permite recorrer en bucle cada elemento de una lista de varios valores para obtener un único resultado. Utilice la etiqueta solo dentro de un resultado. Su principal función es permitir iterar los atributos que pertenecen a un campo de resultado. </p> <p> <b>Ejemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
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
   <td colname="col2"> <p>Cada faceta debe tener sus propias etiquetas de faceta donde el parámetro name coincida con el nombre de la faceta. Las etiquetas de búsqueda se utilizan dentro de las etiquetas de facetas para los valores de facetas. </p> <p>Consulte <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" type="concept" format="dita" scope="local"> Acerca de las facetas </a>. </p> <p> <b>Ejemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;facets&gt; 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;sugerencias&gt;&lt;/recommendations&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas ajusta las sugerencias de ¿Quiso decir? para que la búsqueda guiada reconozca qué nodos XML contienen sugerencias. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;sugerencia&gt;&lt;/sugerencia&gt; </span> </p> </td> 
   <td colname="col2"> <p>Este conjunto de etiquetas ajusta cada sugerencia ¿Quiso decir? </p> <p> <b>Ejemplo</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-if-suggestions&gt; 
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

Se sabe que el paso de JSON frente a XML desde el motor de búsqueda es más rápido porque es una carga útil más pequeña y un analizador más rápido. No obstante, tenga cuidado cuando utilice JSON para asegurarse de que lo que se obtiene es un JSON estricto porque el analizador no perdona.

Si es nuevo en JSON, puede utilizar los vínculos y ejemplos siguientes para ayudarle a empezar:

* Introducción a JSON. Consulte [https://www.json.org/](https://www.json.org/).
* Pruebe el JSON para asegurarse de que es válido. Consulte [https://jsonlint.com/](https://jsonlint.com/).

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

**Ejemplo de sección Faceta JSON para una faceta con campos asociados**

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

**Ejemplo de sección Faceta JSON para facetas con ranuras**

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

Puede utilizar **[!UICONTROL Add Template]** para agregar plantillas de presentación (.tmpl) o plantillas de transporte (.tpl) a la [!DNL Templates] página.

<!-- 

t_adding_a_new_presentation_or_transport_template_file.xml

 -->

**Para agregar una nueva presentación o archivo de plantilla de transporte**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la [!DNL Templates] página, haga clic en **[!UICONTROL Add New Template]**.
1. En el cuadro de diálogo [!DNL Add Template] , configure las opciones que desee.

   <!-- 
   
   r_add_template_options.xml
   
   -->

   | Opción | Descripción |
   |--- |--- |
   | Nuevo nombre de archivo | Especifica el nombre de la plantilla que desea agregar. La extensión de archivo adecuada se agrega automáticamente al nombre del archivo, según el tipo de plantilla que seleccione.  Las plantillas de presentación tienen una extensión de archivo .tmpl; Las plantillas de transporte tienen una extensión de archivo .tpl. |
   | Nuevo tipo de plantilla | Permite elegir una presentación o una plantilla de transporte que desee agregar.  Consulte [Acerca de las plantillas](../c-about-design-menu/c-about-templates.md). |

   Consulte también [Edición de una presentación o una plantilla](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transporte.
1. Haga clic **[!UICONTROL Add]**.
1. (Opcional) En la [!DNL Templates] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una presentación o una plantilla de transporte {#task_800E0E2265C34C028C92FEB5A1243EC3}

Puede utilizar el Editor de plantillas para ver y editar el contenido de los archivos de plantillas de presentación y transporte.

<!-- 

t_editing_a_template.xml

 -->

Puede editar y probar las plantillas de transporte y presentación en etapas, mientras que los visitantes del sitio web siguen utilizando las versiones activas de las plantillas. La plantilla de ensayo se prueba con la versión de ensayo de la dirección URL del dominio de búsqueda. Por ejemplo, puede probar la plantilla de transporte por etapas ejecutando una consulta por etapas ( `sp_staged=1`) con `sp_t` ese valor definido en el nombre de la plantilla de transporte. Cuando esté satisfecho con la apariencia del diseño, puede utilizar **[!UICONTROL Push Live]** desde el editor de plantillas para activar la plantilla. Una vez que la plantilla está activa, los visitantes del sitio empiezan a utilizarla.

Utilice la referencia de la etiqueta de la plantilla de presentación para aprender a enlazar la plantilla de presentación con los componentes de Búsqueda guiada, como facetas, rutas de exploración y menús.

Consulte Etiquetas de plantillas [de presentación](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Utilice la referencia de etiqueta de plantilla de transporte para obtener más información sobre las etiquetas que se utilizarán en las plantillas de transporte.

Consulte Etiquetas de plantilla [de transporte](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**[!UICONTROL To edit a presentation or a transport template]**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la [!DNL Templates] página, haga clic en un nombre de archivo de una presentación o de una plantilla de transporte.
1. En la [!DNL Template Editor] página, realice los cambios que desee en las etiquetas y la codificación.

   Tenga cuidado con los cambios que realice en la [!DNL Template Editor]; no existe la función Deshacer. Si realiza un cambio no deseado y desea volver a la versión anterior del archivo, puede hacer clic en **[!UICONTROL Cancel]** para volver a la tabla de plantillas (suponiendo que no guardó ninguno de los cambios hasta ese momento). Si ya ha guardado los cambios, puede utilizarlos **[!UICONTROL History]** en el editor para revertirlos.
1. (Opcional) Haga clic en **[!UICONTROL Insert Symbol]** para introducir caracteres especiales y símbolos que no tengan las claves correspondientes en los teclados en inglés de EE. UU.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Cierre la página Editor de plantillas cuando haya terminado; volverá a la página Plantillas.

## Copia de una presentación o un archivo de plantilla de transporte {#task_B744AB3384C84DD59C33CD25E18C2C90}

Puede utilizar **[!UICONTROL Copy Template]** para ahorrar tiempo duplicando una plantilla de presentación existente (.tmpl) o una plantilla de transporte (.tpl) y agregarla a la página Plantillas.

<!-- 

t_copying_a_presentation_or_a_transport_template.xml

 -->

Debe cambiar el nombre de la plantilla, el tipo de plantilla o ambos. Si no realiza ningún cambio, la plantilla no se copia.

Debe tener una plantilla ya agregada para poder copiar una plantilla.

Consulte [Adición de una nueva presentación o archivo](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)de plantilla de transporte.

**Para copiar una presentación o un archivo de plantilla de transporte**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la [!DNL Templates] página, en la lista desplegable situada junto al nombre de una plantilla que desea copiar, haga clic en **[!UICONTROL Copy]**.
1. En el cuadro de diálogo [!DNL Copy Template] , establezca una o varias de las opciones que desee.
1. Haga clic **[!UICONTROL Copy]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cambio del nombre de una presentación o un archivo de plantilla de transporte {#task_CC30050FC2DE4898BF44379D8378EB31}

Puede utilizar [!DNL Rename Template] para cambiar el nombre de una plantilla de presentación existente (.tmpl) o una plantilla de transporte (.tpl).

<!-- 

t_renaming_a_presentation_or_a_transport_template_file.xml

 -->

También puede cambiar el tipo de plantilla, si lo desea.

Debe tener una plantilla ya agregada para cambiar el nombre de una plantilla.

Consulte [Adición de una nueva presentación o archivo](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)de plantilla de transporte.

**Cambio del nombre de una presentación o un archivo de plantilla de transporte**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la [!DNL Templates] página, en la lista desplegable situada junto al nombre de una plantilla cuyo nombre desee cambiar, haga clic en **[!UICONTROL Rename]**.
1. En el cuadro de diálogo [!DNL Rename Template] , establezca una o varias de las opciones que desee.
1. Haga clic **[!UICONTROL Rename]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una presentación o un archivo de plantilla de transporte {#task_67E532C2B83A449687737E3B06C5AA58}

Puede utilizar **[!UICONTROL Delete Template]** para eliminar una plantilla de presentación existente (.tmpl) o una plantilla de transporte (.tpl).

<!-- 

t_deleting_a_presentation_or_a_transport_template_file.xml

 -->

Es posible que ya tenga una versión correspondiente de la plantilla de ensayo que se inserta en directo. Si es así, asegúrese de insertar la plantilla eliminada en directo **[!UICONTROL Staging]** para que también se elimine del entorno de lanzamiento. O bien, puede usar **[!UICONTROL Push Live]** en la página Plantillas.

Consulte [Acerca del ensayo](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)

Consulte [Activación de la configuración del escenario](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

Debe tener una plantilla ya agregada para poder eliminar una plantilla.

Consulte [Adición de una nueva presentación o archivo de plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

**Eliminar una presentación o un archivo de plantilla de transporte**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la [!DNL Templates] página, en la lista desplegable situada junto al nombre de una plantilla que desee eliminar, haga clic en **[!UICONTROL Delete]**.
1. En el cuadro de diálogo [!DNL Delete Template] , haga clic en **[!UICONTROL Delete.]**
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Vista previa de la plantilla de presentación minimizada {#task_1757B6207CC74221AE4BFFE5674D320B}

Puede usar **[!UICONTROL Preview minimized]** para ver el aspecto que tendría el peso de página reducido de una plantilla de presentación si decide minimizarla.

<!-- 

t_previewing_the_presentation_template_minimized.xml

 -->

Si minimiza la plantilla de presentación principal, asegúrese de que desea habilitar la minimización de plantillas incluidas (con etiquetas de inclusión guiada), ya que esta opción no es heredable.

Consulte [Reducción del grosor de página de una plantilla de presentación en su ...](../c-about-design-menu/c-about-templates.md#task_B09BB3CE89714DEAAE8D9A899CF3009E)

Debe tener una plantilla ya agregada para previsualizar la plantilla minimizada.

Consulte [Adición de una nueva presentación o archivo de plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

Puede obtener una vista previa del código XML de un archivo de plantilla de transporte.

Consulte [Vista previa del XML de un archivo de plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_58C6C52078E14AD88D2B2F0B3C439AE8)

**Para previsualizar la plantilla de presentación minimizada**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la [!DNL Templates] página, en la lista desplegable situada junto al nombre de una plantilla de presentación, haga clic en **[!UICONTROL Preview minimized]**.

   Utilice la **[!UICONTROL Type]** columna de la tabla Plantillas para ordenar las plantillas por presentación y transporte.
1. (Opcional) En la [!DNL Preview Minimized Template] página, marque **[!UICONTROL Wrap lines]** para leer las etiquetas dentro de la ventana definida.
1. Haga clic **[!UICONTROL Close]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Reducción del grosor de página de una plantilla de presentación en el sitio web {#task_B09BB3CE89714DEAAE8D9A899CF3009E}

Puede reducir el grosor de página de una plantilla de presentación utilizando la **[!UICONTROL Minimize]** opción de la tabla de plantillas.

<!-- 

t_reducing_the_page_weight_of_a_presentation_template.xml

 -->

Al reducir el grosor de página de la plantilla, se minimiza dinámicamente JavaScript y CSS en línea. También puede eliminar espacios en blanco redundantes en el HTML. Minimizar el grosor de página de la plantilla de presentación puede ayudar a ofrecer los resultados de búsqueda más rápido.

También puede obtener una vista previa del aspecto de la plantilla de presentación minimizada mediante **[!UICONTROL Preview minimized]**.

Consulte [Vista previa de la plantilla de presentación minimizada](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B).

**[!UICONTROL To reduce the page weight of a presentation template on your website]**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la [!DNL Templates] página, debajo de la [!DNL Minimize] columna, marque la casilla correspondiente a uno o varios archivos de plantilla de presentación que desee insertar como mínimo en el sitio web.

   Utilice la **[!UICONTROL Type]** columna de la [!DNL Templates] tabla para ordenar las plantillas por presentación y transporte.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuración del archivo de plantilla de presentación predeterminado para utilizarlo en el sitio web {#task_C1E8CE817E4D43E096167A347C54DD53}

Cuando tiene varias plantillas de presentación, puede indicar qué plantilla se utilizará inicialmente para mostrar los resultados de búsqueda.

<!-- 

t_setting_the_default_presentation_template_file_to_use.xml

 -->

Puede utilizar las reglas de búsqueda previa, las reglas de búsqueda posterior y las reglas comerciales para determinar cuándo debe utilizarse una de las otras plantillas de presentación.

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

See [About Post-Search Rules](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

Es común tener una regla como &quot;Para cada búsqueda, establezca la plantilla de presentación de destino en xxxx&quot;. Con una regla de este tipo implementada, el cambio de la plantilla &quot;predeterminada&quot; en la página Plantillas no tendrá ningún efecto.

**[!UICONTROL To set the default presentation template file to use on your website]**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la [!DNL Templates] página, debajo de la [!DNL Default] columna, haga clic en el botón de radio del archivo de plantilla de presentación correspondiente que desee que se muestre como predeterminado.

   Utilice la **[!UICONTROL Type]** columna de la [!DNL Templates] tabla para ordenar las plantillas por presentación y transporte.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Vista previa del XML de un archivo de plantilla de transporte {#task_58C6C52078E14AD88D2B2F0B3C439AE8}

Puede utilizar [!DNL Preview] para revisar el XML de una plantilla de transporte que haya agregado.

<!-- 

t_previewing_the_xml_of_a_transport_template_file.xml

 -->

Debe tener una plantilla de transporte ya agregada para obtener una vista previa del XML de la plantilla.

Consulte [Adición de una nueva presentación o archivo](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)de plantilla de transporte.

Puede obtener una vista previa de los archivos de plantilla de presentación minimizados para ver su peso de página reducido.

Consulte [Vista previa de la plantilla de presentación minimizada](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B).

**Vista previa del XML de un archivo de plantilla de transporte**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. En la [!DNL Templates] página, en la lista desplegable situada junto al nombre de una plantilla de transporte, haga clic en **[!UICONTROL Preview]**.

   Utilice la **[!UICONTROL Type]** columna de la [!DNL Templates] tabla para ordenar las plantillas por presentación y transporte.
1. Cierre la ventana de visualización y vuelva a [!DNL site search/merchandising].
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

