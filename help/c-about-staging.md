---
description: El ensayo le permite probar y previsualizar los cambios en la configuración sin afectar al índice activo.
seo-description: El ensayo le permite probar y previsualizar los cambios en la configuración sin afectar al índice activo.
seo-title: Acerca del ensayo
solution: Target
title: Acerca del ensayo
topic: Staging,Site search and merchandising
uuid: 2e5889a6-2e9c-4ac7-9d6e-d35e7cafda5b
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Acerca del ensayo{#about-staging}

El ensayo le permite probar y previsualizar los cambios en la configuración sin afectar al índice activo.

## Acerca del ensayo {#concept_08B8F3CA1F4241108F14BA7FC7806CA7}

El ensayo le permite probar y previsualizar los cambios en la configuración sin afectar al índice activo.

Consulte también ID [de elemento:context_A5783D07C72042EC8886F300FFF62C50](c-about-simulator.md#context_A5783D07C72042EC8886F300FFF62C50).

Cualquier página que tenga las opciones de ensayo **[!UICONTROL Push All Live]** o **[!UICONTROL View Live Settings]** significa que se puede escalonar toda la configuración de esa página. Las excepciones son las páginas web en el índice. Las páginas de esta área son explícitamente para el índice escalonado o el índice activo para permitirle controlar directamente los dos índices de forma independiente.

Puede escenificar casi cualquier cosa, incluyendo su índice. Algunas excepciones incluyen la configuración específica de la cuenta que afecta tanto al entorno de ensayo como activo de forma simultánea y la programación de operaciones de indexación. De forma predeterminada, cuando guarda los cambios realizados en una configuración que se puede escalonar, se escala automáticamente.

Cuando las opciones **[!UICONTROL Push All Live]** o **[!UICONTROL View Lives Settings]** o no están activadas (atenuadas), significa que la configuración de ensayo de esa página es la misma que la configuración de lanzamiento.

En el caso de un elemento que se está escalonando, tenga en cuenta que la versión activa de la configuración es de solo lectura; solo se puede manipular activando la configuración de ensayo.

## Acerca del historial en las páginas de ensayo {#section_5BE780AFF26A450A9EFF4000DE53531B}

La mayoría de los ajustes de ensayo tiene una [!DNL History] opción en el área superior derecha de la página. Al hacer clic en **[!UICONTROL History]**, le permite revertir cualquier cambio que haya realizado recientemente en la página de ensayo concreta que haya abierto.

También puede ver el Registro de cambios para ver una vista alternativa del Historial. Cada vez que se aplica un cambio, se crea una versión de copia de seguridad del archivo de datos subyacente. El registro de cambios muestra cada una de estas revisiones, mostrando el número de versión, la dirección de correo electrónico del usuario que realizó los cambios y la fecha en que se realizó la copia de seguridad. La entrada con un valor de versión en negrita representa la versión actual.

See [Viewing the Change Log](c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

## La página Administrar configuración de escenario en directo {#section_E72B8CAF516345A5B6B6783CF6E512EE}

Además de ofrecer las **[!UICONTROL Push All Live]** opciones y **[!UICONTROL View Live Settings]** directamente desde una página determinada, también puede utilizar la **[!UICONTROL Manage Stage-Live Settings]** página para hacer lo mismo. La **[!UICONTROL Manage Stage-Live Settings]** página, disponible en el menú principal del producto, es una ubicación central que muestra todas las configuraciones de la cuenta que están actualmente en etapa. Puede insertar todas las opciones de configuración en directo, insertar solo las opciones seleccionadas en directo o eliminar las opciones de configuración. Sin embargo, como práctica recomendada, siempre se debe insertar todos los elementos escalonados en directo para evitar cualquier problema de interdependencia.

La configuración de la página se agrupa en categorías. Puede expandir cada categoría para mostrar la configuración de la página que se está escalonando. Actualmente, las dependencias no se rastrean dentro del administrador de etapas. Por lo tanto, se recomienda insertar todo en directo a la vez excepto el índice.

Puede insertar un índice escalonado en vivo. Asegúrese de comprobar primero que el índice de ensayo no está antiguo ni dañado. Si comete un error y envía el índice escalonado en directo, puede revertir un índice activo antiguo. La inserción activa de un índice escalonado suele tardar menos de 30 segundos.

## Prueba de una configuración o índice de ensayo {#section_6800E52D20854A779946EAB600801F12}

En las páginas que admiten un control de prueba, puede realizar pruebas con la configuración de ensayo o de lanzamiento. Al ver la configuración de ensayo, se utiliza la configuración de ensayo para la prueba. Del mismo modo, cuando se visualiza la configuración en vivo, la prueba utiliza la configuración en directo. En la sección de plantillas, todas las pruebas se realizan con la versión escalonada del índice. Para buscar un índice escalonado, establezca el parámetro `sp_staged` CGI en 1. A su vez, esto indica que desea utilizar el índice escalonado. Si no existe un índice escalonado, se busca en el índice activo y se aplica cualquier configuración de tiempo de búsqueda escalonada según corresponda.

Consulte también Parámetros [CGI de búsqueda back-end](c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

## Visualización de la configuración de lanzamiento {#task_401A0EBDB5DB4D4CA933CBA7BECDC10F}

Puede revisar la versión activa de la configuración desde cualquier página de ensayo.

<!-- 

t_viewing_live_settings.xml

 -->

Si la **[!UICONTROL View Live Settings]** opción no está activada (atenuada), significa que la configuración del escenario para esa página y la configuración de lanzamiento ya están sincronizadas.

**Para ver la configuración en directo**

1. En cualquier página que tenga una configuración de ensayo, haga clic en **[!UICONTROL View Live Settings]** para ver la versión activa de la configuración.
1. Opcionalmente, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL View]** para ver las opciones actuales seleccionadas para la configuración de ensayo.
   * Haga clic en **[!UICONTROL View Stage Settings]** para volver a la configuración de ensayo, donde puede editar o eliminar la configuración.

## Activación de la configuración del escenario {#task_44306783B4C0408AAA58B471DAF2D9A4}

Puede insertar la configuración en directo desde cualquier vista de página de ensayo o desde la **[!UICONTROL Manage Stage-Live Settings]** página central.

<!-- 

t_pushing_live_settings_live.xml

 -->

Cuando la **[!UICONTROL Push Live]** opción está habilitada (sin atenuar) en una página, significa que hay una configuración que se ha escalonado. O bien, significa que un ajuste tiene ediciones y, al guardarlo, se coloca en un escenario. Al hacer clic en esta opción, las ediciones no guardadas se guardan en el área de ensayo. Si no hay ediciones pendientes, la configuración de la página se activa inmediatamente.

**Para insertar la configuración de ensayo en directo**

1. Realice uno de los siguientes pasos:

   * En cualquier página que tenga seleccionada la opción &quot;En etapas&quot; como la vista, haga clic en **[!UICONTROL Push Live]**.
   * En el menú del producto, haga clic en **[!UICONTROL Staging]**. En la **[!UICONTROL Manage Stage-Live Settings]** página, realice una de las acciones siguientes:

   * Utilice el árbol de configuración para comprobar solo la configuración que desea activar y, a continuación, haga clic en **[!UICONTROL Push Selected Live]**.
   * Haga clic **[!UICONTROL Push All Live]**.

## Eliminación de la configuración de la fase de lanzamiento desde una ubicación central {#task_B72BEA9269704B1399600A9CA273369B}

Si tiene muchas opciones de configuración que eliminar, puede utilizar la página para eliminar las opciones de configuración de una ubicación central. **[!UICONTROL Manage Stage-Live Settings]**

<!-- 

t_deleting_staged_settings_from_a_central_location.xml

 -->

**Advertencia**: Al hacer clic en **[!UICONTROL Delete Selected]**, se eliminan inmediatamente todos los ajustes marcados; no hay ningún cuadro de diálogo de confirmación para comprobar que realmente desea eliminar la configuración seleccionada. Además, no hay ninguna función de historial asociada con la página. Por lo tanto, no puede deshacer la eliminación.

**Eliminación de la configuración de puesta en marcha desde una ubicación central**

1. En el menú del producto, haga clic en **[!UICONTROL Staging]**.
1. En la **[!UICONTROL Manage Stage-Live Settings]** página, utilice el árbol de configuración para comprobar solo la configuración que desea eliminar.
1. Haga clic **[!UICONTROL Delete Selected]**.
