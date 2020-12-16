---
description: Utilice el menú de Adobe Analytics para configurar la autenticación de métricas de Adobe Analytics, administrar las métricas de Adobe Analytics de un grupo de informes o usar SAINT para mejorar los informes de Adobe Analytics mediante la aceptación de datos tabulares de fuentes externas.
seo-description: Utilice el menú de Adobe Analytics para configurar la autenticación de métricas de Adobe Analytics, administrar las métricas de Adobe Analytics de un grupo de informes o usar SAINT para mejorar los informes de Adobe Analytics mediante la aceptación de datos tabulares de fuentes externas.
seo-title: Acerca del menú Adobe Analytics
solution: Target
subtopic: Adobe Analytics
title: Acerca del menú Adobe Analytics
topic: Settings,Site search and merchandising
uuid: 5536edf1-d3a4-47af-a307-6e46f385f738
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a
workflow-type: tm+mt
source-wordcount: '3448'
ht-degree: 1%

---


# Acerca del menú de Adobe Analytics{#about-the-adobe-analytics-menu}

Utilice el menú de Adobe Analytics para configurar la autenticación de métricas de Adobe Analytics, administrar las métricas de Adobe Analytics de un grupo de informes o usar SAINT para mejorar los informes de Adobe Analytics mediante la aceptación de datos tabulares de fuentes externas.

## Configuración de la autenticación de métricas de Adobe Analytics {#task_8AA93F6273B747F9B4DE9E8DFBCBDC42}

Para incorporar métricas de Adobe Analytics en las clasificaciones de búsqueda y comercialización del sitio, primero debe obtener un inicio de sesión en Adobe Analytics Web Services. Después de obtener la información de inicio de sesión, puede utilizarla para configurar la autenticación de Adobe Analytics en la búsqueda o comercialización del sitio.

**Para configurar la autenticación de métricas de Adobe Analytics**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Authentication]**.
1. En la página [!DNL Setup Adobe Analytics Metrics Authentication], especifique la información solicitada en cada campo.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Campo de texto </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nombre de Compañía de Adobe Analytics </p> </td> 
      <td colname="col2"> <p>La misma configuración de Nombre de Compañía que se utiliza para iniciar sesión en la cuenta de Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de usuario de los servicios web </p> </td> 
      <td colname="col2"> <p>Nombre de usuario de servicios Web asociado a su cuenta de Adobe Analytics. </p> <p>Puede obtener esta información en Adobe Analytics. En la barra de menús de Adobe Analytics, haga clic en <span class="uicontrol"> <b>Administración</b> </span> &gt; <span class="uicontrol"> <b>Admin Console</b> </span> &gt; <span class="uicontrol"> <b>Compañía</b> </span> &gt; <span class="uicontrol"> <b>Servicios Web a14/&gt; </span>. </b> La información se encuentra en la tabla Información de acceso a API. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Shared Secret de servicios Web </p> </td> 
      <td colname="col2"> <p>Shared Secret de servicios Web asociado a su cuenta de Adobe Analytics. </p> <p>Puede obtener esta información en Adobe Analytics. En la barra de menús de Adobe Analytics, haga clic en <span class="uicontrol"> <b>Administración</b> </span> &gt; <span class="uicontrol"> <b>Admin Console</b> </span> &gt; <span class="uicontrol"> <b>Compañía</b> </span> &gt; <span class="uicontrol"> <b>Servicios Web a14/&gt; </span>. </b> La información se encuentra en la tabla Información de acceso a API. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de los grupos de informes de Adobe Analytics {#concept_1A51AEC5D40E459B813E7891D64B1BAE}

Para utilizar los datos del grupo de informes de Adobe Analytics dentro de la búsqueda o comercialización del sitio, primero debe crear copias de los datos de Adobe Analytics en la cuenta de comercialización o búsqueda del sitio.

Puede crear nuevas definiciones de grupos de informes de Adobe Analytics o puede realizar vistas o modificar los grupos de informes de Adobe Analytics existentes y las métricas asociadas.

La primera vez que accede a Adobe Analytics desde la búsqueda o comercialización del sitio, se descarga y almacena en caché una lista de los grupos de informes disponibles de la compañía. Si se han agregado nuevos grupos de informes recientemente o se han eliminado los existentes, puede actualizar la lista del grupo de informes para volver a descargar la lista de los grupos de informes.

## Añadir un grupo de informes de Adobe Analytics {#task_6DE17305EA7146DA8C30FF8FDF68A3C0}

Puede seleccionar un grupo de informes de Adobe Analytics en el cual basar las reglas de clasificación de comercialización y búsqueda del sitio.

La lista que puede seleccionar debe corresponderse con los grupos de informes disponibles en su cuenta de Adobe Analytics. El grupo de informes seleccionado determina las métricas que están disponibles para su uso en las reglas de clasificación de comercialización y búsqueda del sitio.

Consulte [Acerca de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

Después de agregar un grupo de informes de Adobe Analytics, puede editar sus métricas.

Consulte [Edición de las métricas de Adobe Analytics de un grupo de informes](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

**Para agregar un grupo de informes de Adobe Analytics**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. En la página Grupos de informes de Adobe Analytics, haga clic en **[!UICONTROL Add Report Suite]**.
1. En la lista desplegable de la fila de tabla recientemente agregada, seleccione el grupo de informes que desee.
1. Edite las métricas de Adobe Analytics de un grupo de informes.

## Edición de las métricas de Adobe Analytics de un grupo de informes {#task_360904CCBBB140238ADA036C3CC07664}

Para incorporar las métricas de Adobe Analytics en las reglas de clasificación en la búsqueda o comercialización del sitio, seleccione una o más de las métricas asociadas con el grupo de informes seleccionado. A continuación, configure las opciones que se utilizan para recuperar datos de métricas a través del servicio Web de Adobe Analytics.

Consulte [Añadir un grupo de informes de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0).

Consulte [Configuración de opciones avanzadas de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_C0FF2D69F59D44D8943A7831ED7FEC19).

**Para editar las métricas de Adobe Analytics de un grupo de informes**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. En la página [!DNL Adobe Analytics Report Suites], en la columna **[!UICONTROL Actions]**, haga clic en **[!UICONTROL Edit]** para el grupo de informes cuyas métricas desee configurar.
1. En la página [!DNL Edit Adobe Analytics Metrics], configure las métricas que son necesarias. Las métricas que no tienen un asterisco (*) junto al nombre de la métrica son opcionales.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Grupo de informes </p> </td> 
      <td colname="col2"> <p>Muestra el nombre del grupo de informes que agregó actualmente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de Vista del grupo de informes </p> </td> 
      <td colname="col2"> <p>Proporciona un nombre de "alias" para el nombre del grupo de informes de Adobe Analytics. Este nombre alternativo es útil si se utiliza el mismo grupo de informes en más de una definición. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Seleccione el tipo de informe </p> </td> 
      <td colname="col2"> <p>Especifica el valor del tipo de informe que se usará con el grupo de informes seleccionado. El valor identifica la clave para cada fila de resultados devuelta. </p> <p>El tipo de informe también se conoce como el elemento Adobe Analytics. </p> <p>Esta métrica es obligatoria. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de campo de referencia cruzada </p> </td> 
      <td colname="col2"> <p>Especifica un campo de metadatos cuyos valores se utilizan como "claves" de búsqueda en los datos del grupo de informes. </p> <p>Si no se selecciona ningún valor ("— Ninguno —"), los datos de este grupo de informes no están disponibles para utilizarse en cálculos de clasificación ( <span class="uicontrol"> <b>Reglas</b> </span> &gt; <span class="uicontrol"> <b>Reglas de clasificación</b> </span> &gt; <span class="uicontrol"> <b>Editar reglas</b> &lt;a110&gt; 1/&gt;).</span> </p> <p>Al seleccionar un valor, los valores de este campo se utilizan para hacer referencia cruzada a los documentos de comercialización y búsqueda del sitio con los datos de Adobe Analytics de este grupo de informes, utilizando el valor de Tipo de informe seleccionado que configuró anteriormente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Informe Términos de búsqueda </p> </td> 
      <td colname="col2"> <p>Permite crear reglas comerciales y simular términos de búsqueda desde la página <b>Previsualización de datos de Adobe Analytics de la etapa</b>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0" type="task" format="dita" scope="local">Vista previa de datos de Adobe Analytics</a>. </p> <p>Aparece un menú desplegable en cada fila que incluye dos opciones: <b>Simular término de búsqueda</b> y <b>Crear nueva regla comercial</b>. </p> <p>Ambas opciones utilizan los datos del tipo de informe como términos de búsqueda. Por lo tanto, esta función solo tiene sentido si el tipo de informe representa los términos de búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Métricas </p> </td> 
      <td colname="col2"> <p>Identifica los valores de las métricas que desea descargar y utilizar dentro de las reglas de clasificación de comercialización y búsqueda del sitio. </p> <p>Las métricas que configure aquí aparecen como opciones en las <span class="uicontrol"> <b>Reglas</b> </span> &gt; <span class="uicontrol"> <b>Reglas de clasificación</b> </span> &gt; <span class="uicontrol"> <b>Reglas de edición</b> </span> páginas centrales de miembros, cuando el Tipo de datos de la regla está establecido en &lt;a8&lt;a9/&gt; a12/&gt; Métrica de Adobe Analytics (número) </span>. <span class="uicontrol"> Las opciones muestran una combinación de los nombres de los grupos de informes o de los nombres de las Vistas de los grupos de informes, si se especifican, y los nombres de las métricas individuales. </span></p> <p>Esta métrica es obligatoria. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor mínimo de la métrica </p> </td> 
      <td colname="col2"> <p>Permite introducir un valor distinto de cero para especificar un valor mínimo para la métrica. </p> <p>Si está en blanco o es cero, se descargan todos los valores de la métrica; de lo contrario, la descarga de esta métrica se detiene cuando se pasa el valor mínimo de la métrica. </p> <p>Las métricas de Adobe Analytics se recuperan en orden descendente. </p> <p>Haga clic en <span class="uicontrol"> <b>+</b> </span> para agregar definiciones de métricas adicionales; haga clic en <span class="uicontrol"> <b>-</b> </span> para eliminar las definiciones de métricas que ya no necesite ni desee. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Período de agregación de métricas de Adobe Analytics (días) </p> </td> 
      <td colname="col2"> <p> Controla el número de días de las métricas de Adobe Analytics que se van a recuperar, contando desde la fecha de ayer. No se intenta recuperar datos del día actual. </p> <p>El valor predeterminado es 7. </p> <p>Esta métrica es obligatoria. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Frecuencia de actualización de descarga de Adobe Analytics (días) </p> </td> 
      <td colname="col2"> <p> Establece el intervalo mínimo entre descargas de datos de Adobe Analytics que se utiliza en los cálculos de clasificación. </p> <p>Las descargas desencadenadas por índices que se producen dentro del intervalo de frecuencia de actualización de la descarga se omiten. Sin embargo, las descargas manuales omiten este valor. </p> <p>Cuando se establece este valor en el valor predeterminado de 1, los datos de Adobe Analytics no se descargan más de una vez en un período de 24 horas. Todos los índices de búsqueda que se producen dentro del intervalo de frecuencia de actualización de la descarga utilizan el último conjunto de datos que se descargó. </p> <p>Esta métrica es obligatoria. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Consulte también [Acerca de las reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).
1. Haga clic **[!UICONTROL Save Changes]**.

   Volverá a la página Ensayo [!DNL Adobe Analytics Report Suites].
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de un grupo de informes de Adobe Analytics {#task_0ACA172214D14654ABDB139F417B9F7D}

Puede utilizar Eliminar para eliminar un grupo de informes de la página [!DNL Adobe Analytics Report Suites]. Al eliminar un grupo de informes solo se elimina la copia de los datos de los servidores de comercialización y búsqueda del sitio; no afecta a los datos de los sistemas Adobe Analytics.

**Para eliminar un grupo de informes de Adobe Analytics**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. En la página [!DNL Adobe Analytics Report Suites], en la columna **[!UICONTROL Actions]**, haga clic en **[!UICONTROL Delete]** para el grupo de informes que desee eliminar.
1. En la página [!DNL Adobe Analytics Delete Report Suite], haga clic en **[!UICONTROL Delete]**.

## Vista preliminar de datos de Adobe Analytics {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

Puede utilizar la Previsualización para vista de las métricas de Adobe Analytics cargadas más recientemente.

La columna Fila de la tabla muestra el número de cada fila de datos de métricas, indicando el orden original en que se cargaron las métricas de Adobe Analytics.

La columna Producto muestra el elemento Adobe Analytics que está asociado con cada fila de datos de métricas. Los valores de esta columna se utilizan para asociar las páginas de búsqueda y comercialización del sitio con los valores de métrica correspondientes, según se haya configurado en las definiciones de clasificación.

Consulte [Acerca de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

Consulte [Configuración de la clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

Las columnas restantes muestran los valores de métrica asociados con cada entrada.

Si la tabla está vacía, significa que aún no ha cargado ningún dato de Adobe Analytics. Puede cerrar la página [!DNL Adobe Analytics Data Preview] y luego cargar datos de Adobe Analytics.

Consulte [Carga de datos de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).
Si la tabla fue designada como un informe de términos de búsqueda, aparece un pequeño triángulo en cada fila. Puede hacer clic en la lista desplegable y seleccionar **Simular término de búsqueda** o **Crear nueva regla comercial**. La acción seleccionada se aplica al término de búsqueda de esa fila, los datos que residen en la segunda columna

**Para previsualización de datos de Adobe Analytics**

1. En el menú del producto, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**. En la página [!DNL Adobe Analytics Report Suites], en la columna [!DNL Actions], haga clic en **[!UICONTROL Preview]** para el grupo de informes cuyos datos descargados desee vista.

   * Haga clic **[!UICONTROL Reports]** > **[!UICONTROL Adobe Analytics Terms Reports]**. En la página [!DNL Adobe Analytics Terms Report], en la columna [!DNL Actions], haga clic en **[!UICONTROL Preview]** para el grupo de informes cuyos datos descargados desee vista.

1. En la página [!DNL Adobe Analytics Data Preview], utilice las opciones de navegación y visualización en la parte superior e inferior de la página para realizar una vista de los datos.

   Haga clic en cualquier encabezado de columna de la tabla para ordenar los datos en orden ascendente o descendente.
1. Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Download to Desktop]** para descargar y guardar la tabla como archivo `.xlt`.

   * Cierre la página cuando haya terminado de obtener una vista previa de los datos de Adobe Analytics y vuelva a la página vista anteriormente.

## Visualización del registro desde la carga de datos más reciente de Adobe Analytics {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

Puede utilizar el registro de Vista para examinar el archivo de registro de datos de Adobe Analytics del proceso de descarga más reciente. También puede utilizar la vista de registro para supervisar una descarga en ejecución.

Consulte [Carga de datos de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Para vista del registro desde la carga de datos más reciente de Adobe Analytics**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. En la página [!DNL Adobe Analytics Report Suites], haga clic en **[!UICONTROL View Log]**. Página de registro,
1. En la página [!DNL Adobe Analytics Data Log], utilice las opciones de navegación y visualización en la parte superior e inferior de la página para vista de la información del registro.
1. Cuando haya terminado, cierre la página para volver a la página [!DNL Adobe Analytics Report Suites].

## Cargando datos de Adobe Analytics {#task_2F3C55189B0A4049AB2113F2291CC181}

Puede descargar los datos configurados del grupo de informes de Adobe Analytics en la búsqueda o comercialización del sitio.

La página Carga de datos muestra el estado de la última operación de carga de datos de Adobe Analytics con la siguiente información:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Campo Estado </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Estado </p> </td> 
   <td colname="col2"> <p>Indica el éxito o error del último intento de carga de datos. O bien, muestra el estado de una operación de carga de datos que ya está en curso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Resultados </p> </td> 
   <td colname="col2"> <p>Muestra el número de filas de datos de métricas que se descargaron durante el último intento de carga de datos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hora de inicio </p> </td> 
   <td colname="col2"> <p>Muestra la fecha y la hora en que se inició la última operación de carga de datos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hora de detención </p> </td> 
   <td colname="col2"> <p>Muestra la fecha y hora de finalización de la última operación de carga de datos. O bien, indica que la operación de carga de datos actual aún está en curso. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Para cargar datos de Adobe Analytics**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. En la página [!DNL Stage Adobe Analytics Report Suites], haga clic en **[!UICONTROL Load Adobe Analytics Data]**.
1. En la página **[!UICONTROL Adobe Analytics Data Load]**, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Start Load]** para inicio de la operación de carga.

      Durante una operación de carga de datos, la fila **Progress** proporciona información sobre su progreso.

   * Haga clic en **[!UICONTROL Stop Load]** para detener la operación de carga.

1. Haga clic en **[!UICONTROL Close]** para volver a la página [!DNL Stage Adobe Analytics Reports Suite].

## Actualización de la lista del grupo de informes {#task_EA6215D438CA4185B106657D9712ED34}

La primera vez que accede a Adobe Analytics desde la interfaz de usuario de búsqueda y comercialización del sitio, se descarga y almacena en caché una lista de los grupos de informes de Adobe Analytics disponibles para su compañía. Si se han agregado nuevos grupos de informes recientemente o se han eliminado los existentes, puede utilizar la Lista Actualizar grupo de informes para actualizar la lista mostrada actualmente en la búsqueda o comercialización del sitio.

Consulte [Añadir un grupo de informes de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0).

Consulte [Eliminación de un grupo de informes de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_0ACA172214D14654ABDB139F417B9F7D).

**Para actualizar la lista de grupos de informes**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. En la página [!DNL Adobe Analytics Report Suites], haga clic en **[!UICONTROL Refresh Report Suite List]**.

## Configuración de opciones avanzadas de Adobe Analytics {#task_C0FF2D69F59D44D8943A7831ED7FEC19}

Puede utilizar [!DNL Advanced Adobe Analytics Options] para controlar las configuraciones que están destinadas a ayudarle a ajustar el comportamiento del proceso de descarga del grupo de informes de Adobe Analytics.

Consulte [Edición de las métricas de Adobe Analytics de un grupo de informes](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

**Para configurar opciones avanzadas de Adobe Analytics**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Advanced Options]**.
1. En la página [!DNL Advanced Adobe Analytics Options], establezca las siguientes opciones:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Número máximo de filas, cualquier métrica </p> </td> 
      <td colname="col2"> <p>Una configuración de optimización que evita la descarga de demasiados datos de Adobe Analytics. </p> <p>Si establece esta opción en un valor distinto de cero, la captura de datos de Adobe Analytics se detiene cuando el número total de filas buscadas para cada métrica supera el valor especificado. </p> <p>El valor predeterminado es 0; no se ha aplicado ningún valor máximo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tamaño de captura de repetición de métrica (filas) </p> </td> 
      <td colname="col2"> <p> Controla el número de valores de métricas de Adobe Analytics que se van a recuperar a la vez. Las filas de datos de métricas se recuperan repetidamente hasta que se recuperan todos los datos o hasta que se alcanza el límite máximo de filas. </p> <p>Normalmente no es necesario cambiar esta configuración. Sin embargo, puede resultar útil optimizar la fase de descarga de métricas de un reíndice completo del sitio. </p> <p>El valor predeterminado es 5000. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las fuentes de clasificación de SAINT {#concept_C55609DA24914BBC92CD90ED0259199D}

Puede utilizar Adobe Analytics SAINT para mejorar los informes de análisis mediante la aceptación de datos tabulares de fuentes externas. Por ejemplo: puede utilizar la búsqueda o comercialización del sitio para recuperar los datos de sus propios índices y exportarlos a Adobe Analytics.

Para utilizar correctamente la función de SAINT de Adobe Analytics en la búsqueda o comercialización del sitio, tenga en cuenta los siguientes requisitos:

* Debe tener una compañía de Adobe Analytics y un grupo de informes.

   Consulte [Acerca del menú de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#concept_5FD2D13C9D0D40988E6E51480D690411).
* La cuenta de usuario de Adobe Analytics debe tener privilegios para modificar el grupo de informes.

   Consulte [Configuración de la autenticación de métricas de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42).
* El usuario de Adobe Analytics debe pertenecer al grupo de API web para poder usar la API web de Adobe Analytics.
* El índice de búsqueda debe tener datos que Adobe Analytics pueda utilizar, como tener datos en el formato correcto.

Antes de crear una fuente, revise las siguientes preguntas e información para poder completar correctamente el asistente de fuentes de SAINT:

* ¿Con qué grupo de informes va a trabajar?
* ¿Para qué conjunto de clasificaciones, como product, e-var, etc., va a proporcionar datos?
* ¿Qué clasificaciones existen en los informes? La respuesta a esta pregunta está determinada por el tipo de datos que se puede obtener fácilmente en la búsqueda o comercialización del sitio y el tipo de informes que Adobe Analytics considera convenientes.
* SAINT acepta los datos de la búsqueda o comercialización del sitio como un tipo de texto. El formato de esos datos afecta a la presentación de los informes de Adobe Analytics.

## Creación de una fuente de Adobe Analytics SAINT {#task_914B5AB821E84627953D8EF9339A7DD0}

Puede utilizar Adobe Analytics SAINT para mejorar los informes de Adobe Analytics mediante la aceptación de datos tabulares de fuentes externas.

Por ejemplo: puede utilizar la búsqueda/comercialización del sitio para recuperar datos de sus propios índices y exportar esos datos a Adobe Analytics.

**Para crear una fuente de Adobe Analytics SAINT**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. En la página [!DNL SAINT Classification Feeds], haga clic en **[!UICONTROL Create SAINT Feed]**.
1. En el cuadro de diálogo [!DNL Create Feed], en el campo de texto **Nombre de la fuente**, introduzca el nuevo nombre de la fuente y haga clic en **[!UICONTROL Next]**.

   En este punto, la fuente se guarda y se agrega a la página [!DNL SAINT Classification Feed]. Si lo desea, puede salir y editar la fuente más adelante para completar el asistente.
1. En la página [!DNL Authentication], especifique el nombre de la compañía de Adobe Analytics, el nombre de usuario y el secreto web en los campos de texto correspondientes y, a continuación, haga clic en **[!UICONTROL Next]**.

   Asegúrese de que está autorizado a utilizar la API web con Adobe Analytics.
1. En la página **[!UICONTROL Report Suite]**, elija un grupo de informes y su conjunto de datos de clasificación y, a continuación, haga clic en **[!UICONTROL Next]**.
1. En la página [!DNL Field Maps], asigne las clasificaciones de Adobe Analytics con los campos de metadatos de búsqueda y comercialización del sitio y, a continuación, haga clic en **[!UICONTROL Next]**.

   Para ajustar las clasificaciones de Adobe Analytics, haga clic en **[!UICONTROL Edit]** Clasificaciones de Adobe Analytics para iniciar sesión en Adobe Analytics. Cuando haya terminado de realizar los cambios, haga clic en **[!UICONTROL Refresh Classifications]** para actualizar las opciones de las clasificaciones.
1. En la página [!DNL Search Criteria], los datos de la búsqueda o comercialización del sitio se pueden filtrar antes de enviarse al SAINT de Adobe Analytics. Cree las reglas de filtro aquí mediante la interfaz del generador de reglas y haga clic en **[!UICONTROL Next]**.
1. En la página [!DNL Configure FTP], seleccione el servidor FTP. Especifique la frecuencia con la que desee cargar los datos y, a continuación, haga clic en **[!UICONTROL Next]**.

   Como práctica recomendada, cada fuente tiene su propia cuenta de FTP para evitar la pérdida accidental de datos. Puede crear una nueva cuenta de FTP de Adobe Analytics aquí.
1. En la página [!DNL Verification], haga clic en **[!UICONTROL Show Data View]** para revisar la representación de la vista de datos del resultado. Si existen archivos de fuente reales, se enumeran aquí y están disponibles para que los descargue.
1. Haga clic **[!UICONTROL Close]**.

## Edición de una fuente de Adobe Analytics SAINT {#task_5BF34D02D0D14359B1CF4B3C1B0ACC84}

Puede editar todos los aspectos de una fuente de SAINT existente que haya creado.

**Para editar una fuente de Adobe Analytics SAINT**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. En la página [!DNL Saint Classification Feeds], en la columna **[!UICONTROL Name]**, en la lista desplegable al lado de una fuente, haga clic en **[!UICONTROL Edit feed]**.
1. En el cuadro de diálogo Fuente de SAINT, en el campo de texto **Nombre de fuente**, introduzca el nuevo nombre de fuente y haga clic en **[!UICONTROL Next]**.

   En este punto, la fuente se guarda y se agrega a la página [!DNL SAINT Classification Feed]. Si lo desea, puede salir y editar la fuente más adelante para completar el asistente.
1. En la página [!DNL Authentication], especifique el nombre de la compañía de Adobe Analytics, el nombre de usuario y el secreto web en los campos de texto correspondientes y, a continuación, haga clic en **[!UICONTROL Next]**.

   Asegúrese de que está autorizado a utilizar la API web con Adobe Analytics.
1. En la página **[!UICONTROL Report Suite]**, elija un grupo de informes y su conjunto de datos de clasificación y, a continuación, haga clic en **[!UICONTROL Next]**.
1. En la página [!DNL Field Maps], asigne las clasificaciones de Adobe Analytics con los campos de metadatos de búsqueda y comercialización del sitio y, a continuación, haga clic en **[!UICONTROL Next]**.

   Para ajustar las clasificaciones de Adobe Analytics, haga clic en **[!UICONTROL Edit]** Clasificaciones de Adobe Analytics para iniciar sesión en Adobe Analytics. Cuando haya terminado de realizar los cambios, haga clic en **[!UICONTROL Refresh Classifications]** para actualizar las opciones de las clasificaciones.
1. En la página [!DNL Search Criteria], los datos de la búsqueda o comercialización del sitio se pueden filtrar antes de enviarse al SAINT de Adobe Analytics. Cree las reglas de filtro aquí mediante la interfaz del generador de reglas y haga clic en **[!UICONTROL Next]**.
1. En la página [!DNL Configure FTP], seleccione el servidor FTP. Especifique la frecuencia con la que desee cargar los datos y, a continuación, haga clic en **[!UICONTROL Next]**.

   Como práctica recomendada, cada fuente tiene su propia cuenta de FTP para evitar la pérdida accidental de datos. Puede crear una nueva cuenta de FTP de Adobe Analytics aquí.
1. En la página [!DNL Verification], haga clic en **[!UICONTROL Show Data View]** para revisar la representación de la vista de datos del resultado. Si existen archivos de fuente reales, se enumeran aquí y están disponibles para que los descargue.
1. Haga clic **[!UICONTROL Close]**.

## Eliminación de una fuente de SAINT de Adobe Analytics {#task_5319B1F4CA1A406393CFD7AE97258CEB}

Puede eliminar una fuente SAINT de Adobe Analytics existente que ya no necesite ni use.

**Para eliminar una fuente de Adobe Analytics SAINT**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. En la página [!DNL Saint Classification Feeds], en la columna **[!UICONTROL Name]**, en la lista desplegable al lado de una fuente que desee eliminar, haga clic en **[!UICONTROL Delete feed]**.
1. En el cuadro de diálogo Eliminar, haga clic en **Sí** para verificar la eliminación de la fuente.

## Visualización de un archivo de fuente de Adobe Analytics SAINT {#task_F0C8BADD25E14E5DB30BF31D1F879FDB}

Puede abrir la página [!DNL Verification] de una fuente de SAINT existente para revisar la representación de la vista de datos de la salida.

Si existen archivos de fuente reales, se enumeran aquí y están disponibles para que los descargue como archivo de texto.

**Vista de un archivo de fuente de Adobe Analytics SAINT**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. En la página [!DNL Saint Classification Feeds], en la columna **[!UICONTROL Name]**, en la lista desplegable al lado de una fuente, haga clic en **[!UICONTROL View Feed Files]**.
1. (Opcional) Haga clic en **[!UICONTROL Download File]** para guardar el archivo de fuente como archivo de texto.
1. Haga clic en **[!UICONTROL Close]** para volver a la página [!DNL SAINT Classification Feeds].

## Prueba de una fuente de SAINT de Adobe Analytics {#task_9864D69BE3824FC29C10B36EE4855D25}

Puede probar una fuente de Adobe Analytics SAINT existente sin carga de archivos.

Consulte [Generación y carga de una fuente de SAINT de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_47AED946AA964334A877FDC8D4F6F00A).

Consulte [Visualización de un archivo de fuente SAINT de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB).

**Prueba de un archivo de fuente de Adobe Analytics SAINT**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. En la página [!DNL Saint Classification Feeds], en la columna **[!UICONTROL Name]**, en la lista desplegable al lado de una fuente, haga clic en **[!UICONTROL Test Feed (No file upload)]**.
1. Cuando la fuente termine de procesarse, en la lista desplegable del nombre de la fuente, haga clic en **[!UICONTROL View Feed Files]**.
1. En la página [!DNL Verification], haga clic en **[!UICONTROL Download File]** para descargar el archivo de fuente.
1. Haga clic en **[!UICONTROL Close]** para volver a la página [!DNL SAINT Classification Feeds].

## Generación y carga de una fuente SAINT de Adobe Analytics {#task_47AED946AA964334A877FDC8D4F6F00A}

Puede generar y cargar archivos de fuente para una fuente de Adobe Analytics existente que haya creado.

Consulte [Prueba de una fuente de SAINT de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_9864D69BE3824FC29C10B36EE4855D25).

Consulte [Visualización de un archivo de fuente SAINT de Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB).

**Para generar y cargar un archivo de fuente de Adobe Analytics SAINT**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. En la página [!DNL Saint Classification Feeds], en la columna **[!UICONTROL Name]**, en la lista desplegable al lado de una fuente, haga clic en **[!UICONTROL Generate and Upload Feed]**.
1. Cuando la fuente termine de procesarse, en la lista desplegable del nombre de la fuente, haga clic en **[!UICONTROL View Feed Files]**.
1. En la página [!DNL Verification], haga clic en **[!UICONTROL Download File]** para descargar el archivo de fuente.
1. Haga clic en **[!UICONTROL Close]** para volver a la página [!DNL SAINT Classification Feeds].
