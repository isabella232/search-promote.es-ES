---
description: Puede usar Regenerate Index (Regenerar índice) para actualizar el índice de su sitio web sin necesidad de volver a rastrear el sitio.
solution: Target
subtopic: Regenerate Index
title: Acerca de Regenerar índice
topic-legacy: Index,Site search and merchandising
uuid: 9d1f1d88-0453-4422-a625-a348febbf224
exl-id: 4155a52c-33f6-4f54-b69b-2a092530f7aa
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 1%

---

# Acerca de Regenerar índice{#about-regenerate-index}

Puede utilizar [!DNL Regenerate Index] para actualizar el índice del sitio web sin necesidad de rastrear de nuevo el sitio.

## Uso de Regenerar índice {#concept_6CBE6B8D18EF47D293091CBA542245FA}

Puede utilizar esta opción siempre que realice cambios en las siguientes opciones de cuenta:

* Palabras e idiomas
* Palabras excluidas
* Sinónimos
* La configuración de los metadatos, como cuando se elimina un campo de metadatos, se cambia el nombre de un campo, el tipo de datos, los formatos de fecha, el orden, el valor de clasificación mínimo o máximo, el valor de clasificación predeterminado, el tipo de lista o el separador de listas.

La información actualizada de la opción cuenta se utiliza para generar un nuevo índice de sitio. Regenerar permite realizar cambios rápida y eficazmente en el índice del sitio.

De forma predeterminada, cualquier contenido nuevo o modificado de un sitio web no se incluye en el índice. Para incluir dicho contenido, ejecute un índice completo o incremental.

Consulte también [Ejecución de un índice completo de un sitio web activo o organizado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Consulte también [Ejecución de un índice incremental de un sitio web activo o por etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Regeneración del índice de un sitio web activo o por etapas {#task_B28DE40C0E9A475ABCBCBC4FF993AACD}

Puede utilizar [!DNL Regenerate Index] para actualizar el índice del sitio web sin necesidad de rastrear el sitio.

**Para volver a generar el índice de un sitio web activo o provisional**

1. En el menú del producto, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Live Regenerate]**.

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Staged Regenerate]**.

1. En la página [!DNL Regenerate], haga clic en **[!UICONTROL Regenerate Index Now]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Si decide ejecutar **[!UICONTROL Live Regenerate]**, haga clic en **[!UICONTROL View Last Crawl]** para revisar las estadísticas de rendimiento de la última regeneración del índice activo realizada.

   * Mientras el índice se está regenerando, haga clic en **[!UICONTROL Stop Regenerate Now]** para detener el proceso de regeneración del índice.
   * Mientras el índice se está regenerando, haga clic en **[!UICONTROL Restart Regenerate Now]** para reiniciar el proceso de regeneración del índice desde el principio.
   * Si se produjeron errores de indexación después de una regeneración por etapas, haga clic en **[!UICONTROL View Errors]** para ver el registro asociado.

## Visualización del registro de índice regenerado de un sitio web activo o por etapas {#task_61CE8F9E7BF84BA89A8D482B2106BB15}

Cuando se completa la regeneración de un índice activo o una regeneración de índice por etapas, puede ver su registro asociado para solucionar cualquier error que se haya producido.

No puede exportar registros ni guardarlos. Sin embargo, el registro permanece disponible para su visualización hasta que se produzca el nuevo índice.

**Para ver el registro de índice regenerado de un sitio web activo o provisional**

1. En el menú del producto, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Live Log]**.

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Regenerate Index]** > **[!UICONTROL Staged Log]**.

1. En la página de registro, en la parte superior o inferior, realice una de las acciones siguientes:

   * Utilice las opciones de navegación **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** o **[!UICONTROL Go to line]** para desplazarse por el registro.

   * Utilice las opciones de visualización **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** o **[!UICONTROL Show]** para restringir lo que ve.
