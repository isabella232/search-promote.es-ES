---
description: Utilice Facetas dinámicas para crear nuevas selecciones de rango automáticamente en el momento de la búsqueda. Si lo desea, puede asociar cada campo de faceta dinámica con hasta un nombre de tabla en la cuenta Search&amp;Promote de Adobe. Las relaciones de tabla se aplican en el momento de la búsqueda para cualquier campo de faceta dinámica involucrado en la búsqueda.
solution: Target
subtopic: Navigation
title: Acerca de las facetas dinámicas
topic-legacy: Design,Site search and merchandising
uuid: 1ea91c22-dcc2-4173-aa50-ce618ad0a99c
exl-id: e668e683-3ed8-48fe-a82b-3c4dd484a1c8
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 0%

---

# Acerca de las facetas dinámicas{#about-dynamic-facets}

Utilice Facetas dinámicas para crear nuevas selecciones de rango automáticamente en el momento de la búsqueda. Si lo desea, puede asociar cada campo de faceta dinámica con hasta un nombre de tabla en la cuenta de Search&amp;Promote de Adobe. Las relaciones de tabla se aplican en el momento de la búsqueda para cualquier campo de faceta dinámica involucrado en la búsqueda.

## Uso de facetas dinámicas {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

>[!NOTE]
>
>Esta función no está habilitada en [!DNL Adobe Search&Promote] de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso.

Sin el uso de facetas dinámicas, tuvo que combinar atributos relacionados en &quot;ranuras&quot; y mostrar únicamente las ranuras homogéneas para una búsqueda determinada. Es decir, solo podrían contener valores de un atributo lógico, como &quot;tamaño de zapato&quot; o &quot;tamaño de anillo&quot;. Este método proporciona un rendimiento adecuado en el tiempo de búsqueda con un gran conjunto de atributos únicos.

Sin embargo, cuando se utiliza Facetas dinámicas, no se limita el número de facetas que la búsqueda principal puede rastrear de forma eficaz. Puede definir cientos de facetas dinámicas, desde las que la búsqueda principal puede devolver las &quot;facetas dinámicas principales `N`&quot; para una búsqueda determinada, donde `N` suele ser un valor más modesto de 10 a 20 o menos. Este método elimina la necesidad de asignar los atributos: ahora puede crear una faceta dinámica única para los atributos en el sitio web.

## ¿Qué facetas debe hacer dinámicas? {#section_254EE034BCAD4250A5D09FBF6158C4A5}

Las facetas que están escasamente pobladas en el sitio web y que solo aparecen en un subconjunto de búsquedas son buenas candidatas para ser dinámicas. Por ejemplo, una faceta denominada &quot;ancho de avance&quot; solo se puede rellenar cuando se buscan zapatos o botas. Mientras que otra faceta denominada &quot;Estilo numérico facial&quot;, con posibles valores &quot;romano&quot; y &quot;árabe&quot;, solo puede aparecer cuando se buscan relojes o relojes.

Si su cuenta tiene un gran número de estas facetas, mejora el rendimiento de la búsqueda para utilizar facetas dinámicas en lugar de seleccionar siempre todo el conjunto de facetas posibles para cada búsqueda. Las facetas genéricas como &quot;SKU&quot; o &quot;marca&quot;, que normalmente son apropiadas para mostrarse con los resultados de cada búsqueda, generalmente no son apropiadas como facetas dinámicas.

## Relación de facetas con campos de metaetiqueta {#section_2869E5FCDA8B431A87BC6E5573F2B0A0}

Las facetas se crean sobre los campos de metaetiqueta. Un campo de etiqueta meta es una función de capa de búsqueda principal de bajo nivel de [!DNL Adobe Search&Promote]. Las facetas, por otro lado, son parte de GS (Búsqueda guiada) - la capa de presentación de alto nivel de Search&amp;Promote de Adobe. Las facetas son campos de metaetiqueta, sin embargo, los campos de metaetiqueta no saben nada sobre las facetas. Al configurar facetas dinámicas, primero se agregan facetas y después se agregan campos de metaetiqueta con la opción Faceta dinámica seleccionada para establecer que la faceta identificada sea dinámica.

>[!NOTE]
>
>No hay ninguna configuración &quot;Faceta dinámica&quot; en **[!UICONTROL Design > Navigation > Facets]**. Lo que hace que una faceta sea &quot;dinámica&quot; es que su &quot;campo de metaetiqueta&quot; subyacente es dinámico, tal como se establece en **[!UICONTROL Settings > Metadata > Definitions]**.

## Ejemplos de facetas dinámicas en acción {#section_BC699A05E2E742EF94D41679163ACE84}

Ejemplo de facetas dinámicas que se muestran después de buscar &quot;botes&quot;:

![](assets/dynamicfacets_boots.png)

Otro ejemplo de facetas dinámicas que se muestran después de buscar &quot;relojes&quot;:

![](assets/dynamicfacets_watches.png)

Consulte también

* [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)
* [Etiquetas de plantillas de presentación](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)
* [Etiquetas de plantillas de transporte](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

## Configuración de facetas dinámicas {#task_D17F484130E448258100BAC1EEC53F39}

Configuración de facetas dinámicas en Search&amp;Promote.

<!-- 

t_configuring_dynamic_facets.xml

 -->

>[!NOTE]
>
>De forma predeterminada, esta función no está habilitada en el Search&amp;Promote de Adobe. Póngase en contacto con el soporte técnico para activar la función para su uso.

Antes de que los efectos de las facetas dinámicas sean visibles para los clientes, debe reconstruir el índice del sitio.

Consulte también

* [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)
* [Etiquetas de plantillas de presentación](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)
* [Etiquetas de plantillas de transporte](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**Para configurar facetas dinámicas**

1. Asegúrese de que ya ha agregado facetas.

   Consulte [Adición de una nueva faceta](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. Una vez añadidas las facetas, asegúrese de que ha añadido las facetas a los nuevos campos de metaetiqueta definidos por el usuario.

   Consulte [Adición de un nuevo campo de metaetiqueta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions.]**
1. En la página [!DNL Definitions], en la tabla [!DNL User-defined fields], en la columna [!DNL Actions], haga clic en el icono de lápiz (Editar) en la fila del nombre del campo de etiqueta meta asociado con la faceta que desea hacer dinámica.
1. En la página [!DNL Edit Field], marque **[!UICONTROL Dynamic Facet]**.

   Consulte la tabla de opciones en [Adición de un nuevo campo de metaetiqueta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Haga clic **[!UICONTROL Save Changes]**.
1. Haga clic en **regenerar el índice del sitio escalonado** en el cuadro azul para reconstruir rápidamente el índice del sitio web escalonado.

   Consulte también [Regeneración del índice de un sitio web activo o por etapas](../c-about-index-menu/c-about-regenerate-index.md#task_B28DE40C0E9A475ABCBCBC4FF993AACD).
1. Determine el número de facetas dinámicas que se seleccionarán para una búsqueda determinada. Para realizar esta tarea, realice una de las siguientes acciones:

   * Cree una regla de limpieza de consulta con las condiciones que desee, que realice la acción `set`, `backend parameter`, `sp_sfvl_df_count` para valorar `X`, donde `X` es el número deseado de facetas dinámicas que desea solicitar en el momento de la búsqueda y luego haga clic en **[!UICONTROL Add]**.

   ![](assets/querycleaningrule_dynamicfacets.png)

   Consulte [Adición de una regla de limpieza de consulta](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).

   Consulte también [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8), fila 40 en la tabla para obtener más información sobre `sp_sfvl_df_count`.

   * Agregue una búsqueda, establezca el parámetro &quot;custom&quot; `sp_sfvl_df_count` en el valor deseado y haga clic en **[!UICONTROL Add]**.

   ![](assets/gs_addsearch_dynamic_facets.png)

   Consulte [Adición de una nueva definición de búsqueda](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648).

   Consulte también [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8), fila 40 en la tabla para obtener más información sobre `sp_sfvl_df_count`.

1. Edite la plantilla de transporte adecuada para mostrar las facetas dinámicas que devuelve la búsqueda principal.

   Consulte [Edición de una presentación o de una plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

   Por ejemplo, supongamos que la plantilla de transporte tiene el nombre `guided.tpl`. En tal caso, en el menú del producto, haga clic en **[!UICONTROL Design > Templates]**. En la página [!DNL Templates], busque `guided.tpl` en la tabla. y, a continuación, haga clic en **[!UICONTROL Edit]** a la derecha del nombre. En la página Edición , agregue el siguiente bloque de código al final de `</facets>`: Salida JSON:

   ```
   ... 
   }<search-dynamic-facet-fields>, 
           { 
               "name" : "<search-dynamic-facet-field-name>", 
               "dynamic-facet" : 1, 
               "values" : [<search-field-value-list quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
               "counts" : [<search-field-value-list quotes="yes" commas="yes" data="results" sortby="values" />] 
   
           }</search-dynamic-facet-fields> 
   ...
   ```

1. Edite la plantilla de presentación o las plantillas adecuadas para obtener los resultados de las facetas dinámicas.

   Consulte [Edición de una presentación o de una plantilla de transporte](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

   Por ejemplo, supongamos que tiene una plantilla denominada `sim.tmpl` que se utiliza para generar contenido en el simulador. Para editar esa plantilla, en el menú del producto, haga clic en **[!UICONTROL Design > Templates]**. En la página [!DNL Templates], busque `sim.tmpl` en la tabla. y, a continuación, haga clic en **[!UICONTROL Edit]** a la derecha del nombre. En la página Edición , agregue lo siguiente dentro del área de visualización de facetas de la plantilla:

   ```
   <h6>DF RAIL</h6> 
   <guided-facet-rail gsname="__dynamic_facets"> 
               <guided-facet ><!-- behavior=Normal --> 
               <div class="facet-block" id="facet"> 
               <p><b><guided-facet-display-name /></b></p> 
               <ul> 
                   <guided-facet-values> 
                       <guided-if-facet-value-equals-length-threshold> 
               </ul> 
               <ul id="brand" style="display:none"> 
                       </guided-if-facet-value-equals-length-threshold> 
                       <guided-if-facet-value-selected> 
                           <li><guided-facet-value> [<guided-lt>a href="<guided-facet-value-undo-path />"<guided-gt>X</a>]</li> 
                       <guided-else-facet-value-selected> 
                           <li><guided-facet-link><guided-facet-value></guided-facet-link> (<guided-facet-count>) </li> 
                       </guided-if-facet-value-selected> 
                   </guided-facet-values> 
               </ul> 
               <guided-if-facet-long> 
                 <br /><guided-lt />a href="#" onclick="moreless(this,'brand');return false;" <guided-gt /><button style="font-size:10px;">VIEW MORE</button></a> 
               </guided-if-facet-long> 
               </div> 
               </guided-facet> 
   </guided-facet-rail> 
   <h6>/DF RAIL</h6>
   ```

   También realizaría una modificación similar a otras plantillas de Presentación, según fuera necesario, como `json.tmpl`.

   Asegúrese de especificar `__dynamic_facets` para `gsname` en la etiqueta `guided-facet-rail` . Esta etiqueta es un carril de faceta predefinido reservado para la salida de cualquier faceta dinámica que se devuelva para una búsqueda determinada.

   También puede editar este carril de faceta especial mediante **[!UICONTROL Rules > Business Rules]** y utilizando el **[!UICONTROL Advanced Rule Builder]** como se ve a continuación.

   ![](assets/dynamicfacetrail_businessrule.png)

   Consulte también [Adición de una nueva regla comercial](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)
