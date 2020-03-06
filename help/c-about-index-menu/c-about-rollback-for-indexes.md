---
description: Puede utilizar la opción de revertir para realizar copias de seguridad y archivar los índices de sitios web que haya generado. También puede restaurar la copia de seguridad de un índice en cualquier momento.
seo-description: Puede utilizar la opción de revertir para realizar copias de seguridad y archivar los índices de sitios web que haya generado. También puede restaurar la copia de seguridad de un índice en cualquier momento.
seo-title: Acerca de la anulación de índices
solution: Target
subtopic: Rollback
title: Acerca de la anulación de índices
topic: Index,Site search and merchandising
uuid: abed878a-71b3-4122-9822-7410f4427a9a
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Acerca de la anulación de índices{#about-rollback-for-indexes}

Puede usar [!DNL Rollback] para realizar copias de seguridad y archivar los índices de sitios web que haya generado. También puede restaurar la copia de seguridad de un índice en cualquier momento.

## Uso de Rollback para índices {#concept_0BC4BC975DB045A986C3607CF32705D8}

El archivo contiene cuatro índices: el índice del sitio actual y tres índices de sitio anteriores, que el robot de búsqueda archiva automáticamente en función de la configuración de rollback. Cada vez que se indexa el sitio web, se actualiza el archivo. Los índices más recientes reemplazan a los ya archivados para que el archivo siempre se mantenga actualizado.

Cada índice archivado se enumera en el archivo con la siguiente información:

* Fecha y hora en que se finalizó el índice.
* Índice de edad.
* Número de documentos indexados.
* Tipo de operación de indexación (completa, incremental, etc.).
* Estado del índice, tal como si el índice está activo actualmente y si se conservará o eliminará después del siguiente índice.

Cada vez que se indexa el sitio web, se agrega el nuevo índice al archivo y se elimina un índice archivado existente. Sin embargo, tenga en cuenta que el índice más antiguo no es necesariamente el que se elimina. Cuando se agrega un nuevo índice al archivo, se realiza una comparación de edad de cada índice archivado con las páginas especificadas en los ajustes de configuración de rollback. Se elimina el índice más alejado de la programación deseada. Por ejemplo, supongamos que la configuración es 24,48,72 y que las edades de los índices guardados son 5, 23, 47 y 71. El índice más reciente (cinco horas de edad) se elimina cuando se agrega un nuevo índice al archivo porque su edad está más alejada de la configuración. Para mayor comodidad, el archivo indica qué índice se elimina cuando se vuelve a indexar el sitio.

Puede desplazarse a otras áreas de la interfaz de usuario mientras se activa un índice. Un indicador de estado realiza un seguimiento del progreso de la activación y está disponible cuando ve la [!DNL Rollback] página. Si se restaura un índice archivado, se notifica a los usuarios en la parte superior de las páginas Índice completo, Índice incremental, Índice de secuencias de comandos y Regenerar. No se puede realizar ninguna operación de indexación mientras se restaura un índice. Si una operación de reversión entra en conflicto con un índice de sitio programado, la indexación programada se aplaza hasta que la reversión haya finalizado. Si un índice ya está en curso, se cancela siempre que el usuario confirme que la reversión recibe prioridad.

Para mantener la integridad del archivo, el robot de búsqueda no actualiza el archivo de rollback si se encuentran errores durante un rastreo. Tampoco hay actualizaciones si un usuario cancela una operación de indexación. Si una operación de indexación supera el tiempo máximo, los bytes, las páginas o los documentos, el buscador finaliza el índice y lo agrega al archivo. Además, si no se cumple el número mínimo de páginas durante una operación de indexación, el buscador cancela el índice y el índice anterior permanece activo.

## Configuración del programa de archivado de versiones anteriores de índices {#task_CD403B9AE2244B13A6B3861B5F9B055C}

Puede utilizar [!DNL Configure] para determinar qué archivos de índice desea almacenar en el archivo de rollback. El archivo puede almacenar el índice actual y tres índices de copia de seguridad.

El **[!UICONTROL Schedule]** campo contiene tres valores separados por comas que representan horas del presente. Por ejemplo, los valores de programación de 24.48.72 especifican 24 horas desde el presente o ayer, 48 horas desde el presente o hace dos días y 72 horas desde el presente o hace tres días.

La búsqueda archiva continuamente los índices del sitio más cercanos a un día, dos días y tres días de antigüedad. Las fechas y horas reales de los índices archivados pueden variar según la programación de indexación del sitio web.

**Para configurar la programación de archivado de versiones anteriores de índices**

1. En el menú de producto, haga clic en **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Configure]**.
1. En la [!DNL Rollback Configuration] página, en el **[!UICONTROL Schedule]** campo, introduzca una lista separada por comandos de tres páginas de índice, en horas. Se guardarán los índices más cercanos a estas páginas.
1. Haga clic **[!UICONTROL Save Changes]**.

## Activación de un índice archivado {#task_5DCE3D660F6F4197993E92AA59227332}

Puede utilizar la opción de revertir para activar un índice archivado.

Al hacer clic **[!UICONTROL Activate]** para revertir un índice, el índice activo se mueve al archivo.

Después de activar el índice archivado, volverá a la [!DNL Activate Index] página. Se muestra información sobre la reversión del índice. Además, la [!DNL Activate] columna de la [!DNL Available Indexes] tabla identifica el índice revertido con el estado &quot;Índice activo&quot;.

1. En el menú de producto, haga clic en **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Rollback]**.
1. En la [!DNL Activate Index] página, en la [!DNL Available Indexes] tabla, haga clic en **[!UICONTROL Activate]** para el tipo de índice archivado asociado que desee activar.

   Utilice las columnas Fecha, Edad, Páginas y Operación para determinar qué índice activar.
1. En la [!DNL Verify Rollback] página, revise la información del índice para verificar que ha seleccionado el índice correcto y, a continuación, haga clic en **[!UICONTROL Activate Now]**.

## Visualización del registro de todas las devoluciones de índice {#task_D2D9AA7203F0465FB5AE0D49212AC41C}

Ver la fecha y la hora de todas las operaciones relacionadas con la reversión.

**Para ver el registro de todas las devoluciones de índice**

1. En el menú del producto, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Live Log]**.

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Staged Log]**.

1. En la página de registro, en la parte superior o inferior, realice una de las siguientes acciones:

   * Utilice las opciones de navegación **[!UICONTROL First]****[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** o **[!UICONTROL Go to line]** para desplazarse por el registro.

   * Utilice las opciones de visualización **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** o **[!UICONTROL Show]** para perfeccionar lo que ve.

