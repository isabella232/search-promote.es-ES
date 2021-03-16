---
description: Puede utilizar Índice completo para indexar todas las páginas del sitio web en escena o activo. La indexación ayuda a los clientes a encontrar más fácilmente qué buscan o qué necesitan cuando realizan una búsqueda.
solution: Target
subtopic: Full Index
title: Acerca del índice completo
topic: Índice,Búsqueda de sitios y comercialización
uuid: dce1eafd-5aea-4945-8305-8f9e7dc392df
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---


# Acerca del índice completo{#about-full-index}

Puede utilizar Índice completo para indexar todas las páginas del sitio web en escena o activo. La indexación ayuda a los clientes a encontrar más fácilmente qué buscan o qué necesitan cuando realizan una búsqueda.

## Uso del índice completo {#concept_C69BD21863FD4856B49326F35DB570D3}

Cuando se genera un índice completo, se muestra la información de estado, como la hora de inicio, el tiempo transcurrido y los errores durante el proceso de indexación. También se muestra información sobre el estado del último índice.

Si ha cambiado una configuración de cuenta que requiere una regeneración de índice, el estado puede ser &quot;Regeneración&quot;. Durante la regeneración, la configuración de la cuenta se aplica para crear un índice de sitio actualizado.

Puede detener o reiniciar el proceso de indexación en cualquier momento.

Aunque el nuevo índice está creado para un sitio web activo, los clientes pueden seguir buscando en el sitio con el último índice. También se muestra información sobre el estado del último índice.

## Configuración de la programación de índice completa para un sitio web activo {#task_6760F3256D004A228B38968DF15421F0}

Puede especificar la hora y los días en los que desea rastrear el sitio web y actualizar el índice.

La hora seleccionada es local según la zona horaria configurada en Configuración de la cuenta.

Consulte [Configuración de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Los servidores web suelen estar programados para su mantenimiento a mitad de la noche. Si el servidor está inactivo durante una hora de índice programada, el proceso de indexación fallará. Asegúrese de seleccionar una hora del día en la que el servidor web esté disponible.

La programación de índices solo se aplica a su índice activo; no puede programar índices por etapas.

**Para establecer la programación de índice completa de un sitio web activo**

1. En el menú del producto, haga clic en **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Schedule]**.
1. En la lista desplegable **[!UICONTROL Time]**, seleccione la hora en la que desea que comience la indexación completa.
1. Seleccione uno o más días en los que desea ejecutar la indexación completa.
1. Haga clic **[!UICONTROL Save Changes]**.

## Ejecución de un índice completo de un sitio web activo o provisional {#task_F7FE04D8A1654A7787FCCA31B45EB42D}

Puede utilizar Índice completo para indexar todas las páginas del sitio web en escena o activo. La indexación ayuda a los clientes a encontrar más fácilmente qué buscan o qué necesitan cuando realizan una búsqueda.

**Ejecutar un índice completo de un sitio web activo o provisional**

1. En el menú del producto, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**.

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Staged Index]**.

1. Defina las opciones de indexación que desee.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>Opción </p> </th> 
    <th colname="col2" class="entry"> <p>Descripción </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Borrar caché de índice </p> </td> 
    <td colname="col2"> <p>Quita todos los documentos de la caché de índice. </p> <p>Cuando se selecciona, todas las páginas del sitio web se descargan del servidor. Si esta configuración está marcada y deshabilitada, la cuenta se configura para borrar la caché cada vez que se realiza un índice completo. O bien, algunos ajustes de cuenta modificados anteriormente ahora requieren un índice completo. </p> <p>Cuando se anula la selección, todas las páginas indexadas permanecen en el índice hasta que el servidor web indica que la página ya no existe. Esta situación es verdadera incluso si se eliminan los vínculos a esa página. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Regenerar pendiente </p> </td> 
    <td colname="col2"> <p>Seleccione Si ha realizado cambios en la configuración de la cuenta que hayan cambiado sustancialmente el contenido del índice. Los cambios sustanciales incluyen la realización de cambios en cualquiera de los siguientes: 
    <ul id="ul_4EB8FF692FEB47BBB9A64D61299380D1"> 
    <li id="li_7CF8D286512F4210BEA3DB9F0EFA097A">Sinónimos </li> 
    <li id="li_8178ABC342BB4365B3927E20433756E3">Colecciones </li> 
    <li id="li_57C8BD06BFA64AFAA2C9EF2CC59520EF">Metadatos </li> 
    <li id="li_C4B6A7DA023B4A43991D03EC592170C9">Palabras excluidas </li> 
    <li id="li_9E0AD4B6DDC24A5A8FB5C2C1CCD5348A">Idioma de la cuenta </li> 
    <li id="li_338F107547DF48AAA0EF90F4AD8664A5">Clasificación </li> 
    <li id="li_7F49B86D94974E79AAD381A64A1400F2">Alternar la búsqueda que distingue entre mayúsculas y minúsculas </li> 
    <li id="li_E8FE6EE240A840AC826ADF4294AAC6F6">Alternar el soporte diacrítico </li> 
    <li id="li_51763D482DCB4ED0972966F492B8C0F2">Alternar la indexación de números </li> 
    </ul> </p> <p>Antes de que se produzca otro rastreo, se realiza un paso rápido a través de todos los datos de índice para ajustarlos a la nueva configuración de cuenta. </p> <p>Esta opción solo está disponible si está haciendo un índice completo de un sitio web escalonado. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Recuento de todas las páginas </p> </td> 
    <td colname="col2"> <p>Permite que continúe el rastreo de páginas de sitios web incluso después de haber alcanzado el límite de páginas de su cuenta. </p> <p>Las páginas adicionales no se agregan al índice, pero puede determinar el número total de documentos en el sitio web. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Full Index Now]**.
1. (Opcional) Si se produjeron errores de indexación, haga clic en **[!UICONTROL View Errors]** para ver el registro asociado.

## Visualización del registro de índice completo de un sitio web activo o por etapas {#task_02E5E944C56B4EB19CC1FF321F3221B8}

Cuando se completa un índice completo activo o un índice completo escalonado, puede ver su registro asociado para solucionar cualquier error que se haya producido.

No puede exportar registros ni guardarlos. El registro permanece disponible para su visualización hasta que se produzca el nuevo índice.

**Para ver el registro de índice completo de un sitio web activo o provisional**

1. En el menú del producto, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Log]**.

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Staged Log]**.

1. En la página de registro, en la parte superior o inferior, realice una de las acciones siguientes:

   * Utilice las opciones de navegación **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** o **[!UICONTROL Go to line]** para desplazarse por el registro.

   * Utilice las opciones de visualización **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** o **[!UICONTROL Show]** para restringir lo que ve.

