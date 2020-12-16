---
description: Puede configurar Quiso decir para que los clientes reciban sugerencias de términos de búsqueda válidos cuando hayan intentado realizar búsquedas con errores. Las sugerencias se forman buscando la ortografía y escribiendo las correcciones a los términos de búsqueda que resultan en una búsqueda válida.
seo-description: Puede configurar Quiso decir para que los clientes reciban sugerencias de términos de búsqueda válidos cuando hayan intentado realizar búsquedas con errores. Las sugerencias se forman buscando la ortografía y escribiendo las correcciones a los términos de búsqueda que resultan en una búsqueda válida.
seo-title: Acerca de ¿Quiso decir?
solution: Target
title: Acerca de ¿Quiso decir?
topic: Linguistics,Site search and merchandising
uuid: c5973541-3d6b-4fc9-bad4-66d4d3559fe8
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 2%

---


# Acerca de quiso decir{#about-did-you-mean}

Puede configurar Quiso decir para que los clientes reciban sugerencias de términos de búsqueda válidos cuando hayan intentado realizar búsquedas con errores. Las sugerencias se forman buscando la ortografía y escribiendo las correcciones a los términos de búsqueda que resultan en una búsqueda válida.

## Configurar ¿Quiso decir {#task_B539D6A0043547EFB1CA19B67E762371}

Puede personalizar la forma en que [!DNL site search/merchandising] realiza sugerencias de búsqueda cuando la consulta de un cliente devuelve resultados de búsqueda mínimos o nulos.

<!-- 

t_configuring_did_you_mean.xml

 -->

**Para configurar ¿Quiso decir?**

1. En el menú del producto, haga clic en **[!UICONTROL Linguistics]** > **[!UICONTROL Did You Mean]**.
1. En la página [!DNL Did You Mean], en el campo de texto **Eliminar estas palabras de sugerencias**, introduzca palabras separadas por espacios o líneas para filtrar las sugerencias no deseadas.

   Son palabras del índice de búsqueda que no se muestran como términos de búsqueda alternativos recomendados. Puede excluir cualquier palabra que coincida con un patrón mediante el uso de expresiones regulares. De lo contrario, solo se elimina la palabra exacta.

1. Configure las opciones **Quiso decir** que desee.

   <!-- 
   
   r_did_you_mean_options.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Algoritmo de sugerencia </p> </td> 
      <td colname="col2"> <p>Ajusta el alcance del software para encontrar sugerencias. Si un usuario comete un error de una sola letra, todos los algoritmos tienen las mismas sugerencias. La razón es que solo se necesita una edición para llegar a una sugerencia que funcione y todos los algoritmos encuentran palabras que están cerca del original. Pero cuando los términos de búsqueda originales no son similares a los términos existentes en el índice, los <b>Deep</b> y <b>Bad Spellers</b> Algoritmos de sugerencia continúan buscando posibles sugerencias. Este escenario es útil si un cliente prueba con un nombre adecuado que sea difícil de escribir y que suene los nombres. Sin embargo, si solo desea que aparezcan sugerencias similares, puede elegir el algoritmo <b>Quick</b>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Recuento predeterminado de sugerencias para mostrar </p> </td> 
      <td colname="col2"> <p>Especifica el número de sugerencias de términos de ¿Quiso decir? (0-20) que desea mostrar cuando la búsqueda de un cliente no arroja ningún resultado. El valor predeterminado es 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Longitud mínima de la palabra de sugerencia </p> </td> 
      <td colname="col2"> <p>Prunes Quiso decir términos especificando el número mínimo de letras de una palabra sugerida. </p> <p>Por ejemplo, si establece el valor en 4, el software no sugiere una palabra de 1, 2 o 3 caracteres de longitud. Si especifica un valor de 0, no se eliminará ninguna palabra corta de las sugerencias de término. Si se especifica un valor alto, normalmente no se producen sugerencias de términos. El valor predeterminado es 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Frecuencia mínima de índice </p> </td> 
      <td colname="col2"> <p> Especifica el número mínimo de veces que una palabra debe aparecer en el índice antes de incluirse en el diccionario Quiso decir. </p> <p>No se puede especificar un número negativo en el campo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Buscar término sugerido si no hay resultados </p> </td> 
      <td colname="col2"> <p>Vuelve a buscar automáticamente el primer término sugerido cuando la búsqueda de un cliente no arroja resultados y hay al menos una sugerencia de término ¿Quiso decir?. </p> <p>Puede utilizar las etiquetas siguientes en la plantilla de presentación para indicar que la búsqueda o comercialización del sitio está buscando automáticamente un término diferente: </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> <p>También puede mostrar otras sugerencias aquí. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;There&nbsp;was&nbsp;0&nbsp;matches&nbsp;for&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&nbsp;&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&lt;guided-param&nbsp;gsname="q"&gt;?&nbsp;Here&nbsp;are&nbsp;the&nbsp;results&nbsp;for&nbsp;that&nbsp;search.&nbsp;&nbsp;&nbsp;Or&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestions&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Hacer sugerencias debido a los bajos resultados </p> </td> 
      <td colname="col2"> <p>Si un cliente busca un término que arroje menos de diez resultados, el motor de búsqueda comprueba si tiene una sugerencia que pueda arrojar más de 100 resultados. Si es así, puede utilizar las etiquetas siguientes para indicar al usuario que, aunque tenga resultados, es posible que haya deseado buscar otra cosa: </p> <p> <code>&nbsp;&lt;guided-if-suggestion-low-results&gt; &nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;Search&nbsp;for&nbsp;guided-param&nbsp;gsname="q"&gt;.&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestion&gt;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-low-results&gt;</code> </p> <p> En el escenario anterior, el número de sugerencias está controlado por el valor especificado en <span class="uicontrol"> Recuento predeterminado de sugerencias para mostrar</span>. Los umbrales alto y bajo se pueden configurar mediante las opciones siguientes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Haga sugerencias cuando los resultados iniciales sean menores que </p> </td> 
      <td colname="col2"> <p>Controla el número de resultados cuando el sistema inicio las sugerencias de oferta. </p> <p>Esta opción solo aparece cuando marca <span class="uicontrol"> Hacer sugerencias debido a los bajos resultados</span>. </p> <p>El valor predeterminado es 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Una sugerencia debe generar al menos estos muchos resultados </p> </td> 
      <td colname="col2"> <p>Sugerencias de filtros que se realizan debido a los bajos resultados en la búsqueda principal según el recuento de resultados. </p> <p>Esta opción solo aparece cuando marca <span class="uicontrol"> Hacer sugerencias debido a los bajos resultados</span>. </p> <p>El valor predeterminado es 100. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic en **Guardar cambios**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

