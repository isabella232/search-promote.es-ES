---
description: El ensayo permite probar y previsualizar los cambios en la configuración sin afectar al índice activo.
solution: Target
title: Acerca del ensayo
topic: Ensayo, búsqueda de sitios y comercialización
uuid: 2e5889a6-2e9c-4ac7-9d6e-d35e7cafda5b
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---


# Acerca del ensayo{#about-staging}

El ensayo permite probar y previsualizar los cambios en la configuración sin afectar al índice activo.

## Acerca del ensayo {#concept_08B8F3CA1F4241108F14BA7FC7806CA7}

El ensayo permite probar y previsualizar los cambios en la configuración sin afectar al índice activo.

Consulte también [ID de elemento:context_A5783D07C72042EC886F300FFF62C50](c-about-simulator.md#context_A5783D07C72042EC8886F300FFF62C50).

Cualquier página que tenga las opciones de ensayo **[!UICONTROL Push All Live]** o **[!UICONTROL View Live Settings]** significa que se pueden configurar todas las opciones de esa página. Las excepciones son las páginas web en Index. Las páginas de esta área son explícitamente para el índice por etapas o el índice activo para permitirle controlar directamente los dos índices de forma independiente.

Se puede escenificar casi cualquier cosa incluyendo su índice. Algunas excepciones incluyen la configuración específica de la cuenta que afecta al entorno en tiempo real y en tiempo real simultáneamente, así como la programación de las operaciones de indexación. De forma predeterminada, cuando se guardan los cambios en una configuración que se puede escalonar, se monta automáticamente.

Cuando las opciones **[!UICONTROL Push All Live]** o **[!UICONTROL View Lives Settings]** no están habilitadas (atenuadas), significa que la configuración por etapas de esa página es la misma que la configuración en vivo.

Para un elemento que se haya montado, tenga en cuenta que la versión activa de la configuración es de solo lectura; solo puede manipularse activando la configuración por etapas.

## Acerca del historial en páginas por etapas {#section_5BE780AFF26A450A9EFF4000DE53531B}

La mayoría de las opciones de configuración organizadas tienen la opción [!DNL History] en el área superior derecha de la página. Al hacer clic en **[!UICONTROL History]**, le permite revertir cualquier cambio que haya realizado recientemente en la página provisional concreta que ha abierto.

También puede ver el registro de cambios para ver una vista alternativa del historial. Cada vez que se aplica un cambio, se crea una versión de copia de seguridad del archivo de datos subyacente. El registro de cambios muestra cada una de estas revisiones, mostrando el número de versión, la dirección de correo electrónico del usuario que realizó los cambios y la fecha en que se realizó la copia de seguridad. La entrada con un valor de versión en negrita representa la versión actual.

Consulte [Visualización del registro de cambios](c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

## La página Administrar configuración de etapa activa {#section_E72B8CAF516345A5B6B6783CF6E512EE}

Además de ofrecer las opciones **[!UICONTROL Push All Live]** y **[!UICONTROL View Live Settings]** directamente desde una página determinada, también puede utilizar la página **[!UICONTROL Manage Stage-Live Settings]** para hacer lo mismo. La página **[!UICONTROL Manage Stage-Live Settings]**, disponible en el menú principal del producto, es una ubicación central que muestra todas las configuraciones de la cuenta que están actualmente organizadas. Puede insertar todos los ajustes en directo, insertar solo los ajustes seleccionados en directo o eliminar los ajustes. Sin embargo, como práctica recomendada, siempre inserte todos los elementos clasificados en vivo para evitar problemas de interdependencia.

La configuración de la página se agrupa en categorías. Puede expandir cada categoría para mostrar la configuración de la página que está configurada. Actualmente, no se realiza un seguimiento de las dependencias dentro del administrador de escenarios. Por lo tanto, se recomienda que inserte todo en directo a la vez excepto para el índice.

Puede insertar un índice escalonado en vivo. Asegúrese de comprobar primero que el índice de ensayo no está obsoleto ni dañado. Si comete un error y activa el índice escalonado, puede revertir un antiguo índice activo. La inserción de un índice en vivo por etapas suele tardar menos de 30 segundos.

## Prueba de una configuración o índice por etapas {#section_6800E52D20854A779946EAB600801F12}

En las páginas que admiten un control de prueba, puede realizar pruebas con la configuración en vivo o en escena. Al ver la configuración de ensayo, se utiliza la configuración de ensayo para la prueba. Del mismo modo, cuando visualiza la configuración en directo, la prueba utiliza la configuración en directo. En la sección de plantillas, todas las pruebas se realizan con la versión por etapas del índice. Para buscar un índice escalonado, establezca el parámetro CGI `sp_staged` en 1. A su vez, esto indica que desea utilizar el índice escalonado. Si no existe un índice escalonado, se busca en el índice activo y se aplica cualquier configuración de tiempo de búsqueda escalonada según corresponda.

Consulte también [Parámetros CGI de búsqueda back-end](c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

## Visualización de la configuración de lanzamiento {#task_401A0EBDB5DB4D4CA933CBA7BECDC10F}

Puede revisar la versión activa de la configuración desde cualquier página configurada.

<!-- 

t_viewing_live_settings.xml

 -->

Si la opción **[!UICONTROL View Live Settings]** no está activada (atenuada), significa que la configuración de escenario de esa página y la configuración de lanzamiento ya están sincronizadas.

**Para ver la configuración de lanzamiento**

1. En cualquier página que tenga la configuración configurada, haga clic en **[!UICONTROL View Live Settings]** para ver la versión activa de la configuración.
1. Opcionalmente, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL View]** para ver las opciones actuales seleccionadas para la configuración por etapas.
   * Haga clic en **[!UICONTROL View Stage Settings]** para volver a la configuración por etapas, donde puede editar o eliminar la configuración.

## Inserción de la configuración del escenario en directo {#task_44306783B4C0408AAA58B471DAF2D9A4}

Puede insertar la configuración en directo desde cualquier vista de página por etapas o desde la página central **[!UICONTROL Manage Stage-Live Settings]** .

<!-- 

t_pushing_live_settings_live.xml

 -->

Cuando la opción **[!UICONTROL Push Live]** está activada (sin atenuar) en una página, significa que hay una configuración que está configurada. O bien, significa que una configuración tiene ediciones y cuando se guarda, se coloca en escena. Al hacer clic en esta opción, las ediciones sin guardar se guardan en el área de ensayo. Si no hay ediciones pendientes, la configuración de la página se inserta inmediatamente en vivo.

**Para insertar la configuración de ensayo en directo**

1. Realice uno de los siguientes pasos:

   * En cualquier página que tenga seleccionada la opción &quot;En escena&quot; como Vista, haga clic en **[!UICONTROL Push Live]**.
   * En el menú del producto, haga clic en **[!UICONTROL Staging]**. En la página **[!UICONTROL Manage Stage-Live Settings]**, realice una de las siguientes acciones:

   * Utilice el árbol de configuración para comprobar solo aquellos ajustes que desea insertar en directo y, a continuación, haga clic en **[!UICONTROL Push Selected Live]**.
   * Haga clic **[!UICONTROL Push All Live]**.

## Eliminación de la configuración de puesta en marcha desde una ubicación central {#task_B72BEA9269704B1399600A9CA273369B}

Si tiene muchas opciones de configuración que eliminar, puede usar la página **[!UICONTROL Manage Stage-Live Settings]** para eliminar las opciones de una ubicación central.

<!-- 

t_deleting_staged_settings_from_a_central_location.xml

 -->

**Advertencia**: Al hacer clic en  **[!UICONTROL Delete Selected]**, todos los ajustes marcados se eliminan inmediatamente; no hay ningún cuadro de diálogo de confirmación para verificar que realmente desea eliminar la configuración seleccionada. Además, no hay ninguna función Historial asociada a la página. Por lo tanto, no puede deshacer la eliminación.

**Eliminar la configuración de puesta en marcha desde una ubicación central**

1. En el menú del producto, haga clic en **[!UICONTROL Staging]**.
1. En la página **[!UICONTROL Manage Stage-Live Settings]**, utilice el árbol de configuración para comprobar solo aquellos ajustes que desee eliminar.
1. Haga clic **[!UICONTROL Delete Selected]**.
