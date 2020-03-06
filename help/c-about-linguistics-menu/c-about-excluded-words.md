---
description: Puede utilizar Palabras excluidas para especificar frases y palabras comunes utilizadas con frecuencia, como "a" y "the", que desee excluir de los resultados de búsqueda.
seo-description: Puede utilizar Palabras excluidas para especificar frases y palabras comunes utilizadas con frecuencia, como "a" y "the", que desee excluir de los resultados de búsqueda.
seo-title: Acerca de las palabras excluidas
solution: Target
title: Acerca de las palabras excluidas
topic: Linguistics,Site search and merchandising
uuid: 1c879462-1b19-44f6-a3b2-20aa786b3221
translation-type: tm+mt
source-git-commit: 46cdbdf94ba8f92dba7d03ce80b25a2ae73b228a

---


# Acerca de las palabras excluidas{#about-excluded-words}

Puede utilizar Palabras excluidas para especificar frases y palabras comunes utilizadas con frecuencia, como &quot;a&quot; y &quot;the&quot;, que desee excluir de los resultados de búsqueda.

## Uso de palabras excluidas {#concept_9DB67BD2F0DC43AC88741003D9F39812}

See also [About Searches](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

Sin palabras excluidas, las búsquedas que contengan estas palabras pueden identificar numerosos resultados irrelevantes. Al excluir palabras y frases, se omiten los resultados de búsqueda que coinciden únicamente con los términos excluidos que ha especificado. Si una consulta de búsqueda contiene una palabra excluida, solo se utilizan las palabras no excluidas para buscar documentos.

Las palabras de búsqueda excluidas no se resaltan en los resultados de búsqueda. Sin embargo, la puntuación de relevancia de cada resultado se ve influida por las palabras excluidas. En otras palabras, las palabras excluidas se omiten al buscar documentos, pero se siguen utilizando al clasificar los documentos en la página de resultados de búsqueda. Antes de que los efectos de la configuración Palabras excluidas (o cambios en esta configuración) estén disponibles para los clientes, asegúrese de volver a generar el índice del sitio.

Cuando se escriben palabras para excluir de los resultados de la búsqueda, las palabras o frases se separan entre sí con comas. Puede introducir una o varias palabras de exclusión por línea. A continuación se muestra un ejemplo de palabras excluidas en líneas separadas y divididas por comas.

![](assets/excluded_words_1.jpg)

Utilizando la lista de palabras excluidas de arriba, si el cliente busca &quot;los estados unidos de América&quot;, la palabra &quot;el&quot; y la palabra &quot;de&quot; se excluyen de la búsqueda. En su lugar, la búsqueda encuentra todas las páginas que contienen las palabras &quot;unidos&quot;, &quot;estados&quot; y &quot;americanos&quot;. No se muestran las páginas que contienen solamente la palabra &quot;de&quot; o &quot;de&quot;.

Algunos sitios contienen frases específicas en la mayoría o en todas las páginas. Por ejemplo, un sitio web sobre turismo en Nueva York podría contener las palabras Nueva York en el título de cada página. Considere agregar esta frase, y otras similares, a la lista de exclusión:

![](assets/excluded_words_2.jpg)

Cuando se excluye una frase, las palabras individuales que la componen se seguirán utilizando como términos de búsqueda. Sólo cuando un visitante busca las palabras exactas, en el orden exacto de una frase excluida, se excluye la frase de los resultados de búsqueda. Utilizando el ejemplo anterior, si un cliente buscó el &quot;ballet de nueva york&quot;, se excluyen la palabra &quot;el&quot; y la frase &quot;nueva york&quot;; sólo se devuelven como resultado de búsqueda las páginas que contienen la palabra &quot;ballet&quot;. Por otra parte, una búsqueda de &quot;nuevos edificios&quot; o &quot;duque de york&quot; todavía encuentra páginas que contienen la palabra &quot;nuevo&quot; o &quot;york&quot;, respectivamente.

## Configuración de palabras excluidas {#task_60BF6BB7A66C48479D2BBB32C0F38CDE}

Puede excluir las frases y palabras comunes utilizadas con frecuencia de los resultados de búsqueda.

Puede introducir una o más palabras por línea. Separe cada palabra con comas como en el ejemplo siguiente:

![](assets/excluded_words_1.jpg)

Puede elegir mostrar los resultados de búsqueda cuando todas las palabras de la búsqueda del cliente sean palabras excluidas. Por ejemplo: si ha excluido la palabra &quot;el&quot; y un cliente decide buscar sólo &quot;el&quot;, los resultados de la búsqueda muestran cualquier página que contenga la palabra &quot;el&quot;. Este resultado es cierto aunque se excluya la palabra &quot;el&quot;. Si no marca esta opción, el cliente no obtiene ningún resultado de búsqueda. Esta configuración no tiene efecto si la búsqueda contiene al menos una palabra no excluida.

**Para configurar palabras excluidas**

1. En el menú de producto, haga clic en **[!UICONTROL Linguistics]** > **[!UICONTROL Excluded Words]**.
1. En la [!DNL Excluded Words] página, en el campo de **[!UICONTROL Words and Phrases]** texto, escriba las palabras que desee excluir de los resultados de búsqueda.
1. (Opcional) Haga clic en **[!UICONTROL Show results when all words in the query are excluded words]**.

   Cuando se excluyen todas las palabras de la búsqueda del cliente, todas las palabras se utilizan juntas para realizar la búsqueda.
1. Haga clic **[!UICONTROL Save Changes]**.
1. Para obtener una vista previa de los resultados de los cambios, haga clic en **[!UICONTROL regenerate your staged site index]** para volver a generar el índice del sitio web escalonado.

   Consulte [Ejecución de un índice completo de un sitio web activo o en un sitio web escalonado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Ejecución de un índice incremental de un sitio Web activo o en un sitio Web en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) En el menú de producto, haga clic en **[!UICONTROL Linguistics]** > **[!UICONTROL Excluded Words]** y, a continuación, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

