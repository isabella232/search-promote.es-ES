---
description: Vistas de datos muestra los resultados de la búsqueda con los campos meta. Cada columna es un campo meta y cada fila es el resultado de una consulta de búsqueda. Personalice las vistas de datos eligiendo y reorganizando columnas. Las vistas de datos también pueden tener títulos y descripciones personalizados.
seo-description: Vistas de datos muestra los resultados de la búsqueda con los campos meta. Cada columna es un campo meta y cada fila es el resultado de una consulta de búsqueda. Personalice las vistas de datos eligiendo y reorganizando columnas. Las vistas de datos también pueden tener títulos y descripciones personalizados.
seo-title: Acerca de las vistas de datos
solution: Target
title: Acerca de las vistas de datos
topic: Reports,Site search and merchandising
uuid: 18930551-960d-40c2-b5b7-0807a2e11134
translation-type: tm+mt
source-git-commit: 7af85dd37f06fe506e5f57e28a25385ca7ab3db5

---


# Acerca de las vistas de datos{#about-data-views}

Vistas de datos muestra los resultados de la búsqueda con los campos meta. Cada columna es un campo meta y cada fila es el resultado de una consulta de búsqueda. Personalice las vistas de datos eligiendo y reorganizando columnas. Las vistas de datos también pueden tener títulos y descripciones personalizados.

## Uso de vistas de datos {#concept_DCA897D074464BC1861AA47B40CC86C3}

Cada cuenta tiene la conveniencia de crear varias vistas de datos. Utilice la página Vistas de datos para crear y editar estas vistas de datos.

Después de agregar una vista de datos, debe editarla para configurar y personalizar la vista.

Consulte [Edición de una vista](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)de datos.

Puede copiar una vista de datos existente para utilizarla como base para crear una nueva vista de datos.

Consulte [Copia de una vista](../c-about-reports-menu/c-about-data-views.md#task_78D4C2799BC84677843ED4CA1CD205AF)de datos.

## Adición de una vista de datos {#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D}

Puede agregar una vista de datos a la [!DNL Data Views] página para mostrar los valores de cada meta campo con una consulta de búsqueda.

Después de agregar una vista de datos, debe editarla para configurar y personalizar la vista.

Consulte [Edición de una vista](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)de datos.

**Para agregar una vista de datos**

1. En el menú de producto, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. En la [!DNL Data Views] página, haga clic en **[!UICONTROL Add New Data View]**.
1. En el cuadro de diálogo [!DNL Add New Data View] , en el [!DNL Title] campo, escriba el nombre de la vista de datos que desea crear.
1. Haga clic **[!UICONTROL Add]**.

## Edición de una vista de datos {#task_258A367896C24DD498C755925EA8F516}

Al agregar una vista de datos a la [!DNL Data Views] página, utilice Editar para cambiar el nombre y la descripción de la vista de datos o para mover, mostrar u ocultar la visualización de cada meta campo.

También puede bloquear o desbloquear una vista de datos seleccionada.

Consulte [Adición de una vista](../c-about-reports-menu/c-about-data-views.md#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D)de datos.

**Para editar una vista de datos**

1. En el menú de producto, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. En la [!DNL Data Views] página, en la [!DNL Actions] columna de la tabla, haga clic **[!UICONTROL Edit]** en la fila con la vista de datos que desee cambiar.
1. En la [!DNL Data Views Editor] página, configure las opciones que desee.

   El Editor de vista de datos tiene todos los controles para ocultar, mostrar y mover columnas de campo en la página Vista de datos.

   Al ver una vista de datos, la tabla resultante también muestra los siguientes campos de columna adicionales que no son editables: Clasificación, Relevancia y Puntuación (general). Estos tres campos especiales representan las puntuaciones de relevancia, las puntuaciones de clasificación y las puntuaciones generales de cada resultado.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Título </p> </td> 
      <td colname="col2"> <p>Nombre de la vista de datos. El nombre se muestra en la parte superior derecha cuando se ve la vista de datos. </p> <p>Consulte <a href="../c-about-reports-menu/c-about-data-views.md#task_FD0D2CE53DF84CBD9220AD7CA920011F" type="task" format="dita" scope="local"> Visualización de una vista</a>de datos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Descripción </p> </td> 
      <td colname="col2"> <p>(Opcional) Contiene una descripción de la vista de datos. La descripción se muestra entre el nombre del título de la vista de datos y el campo de texto <span class="wintitle"> Nueva búsqueda</span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetros de búsqueda </p> </td> 
      <td colname="col2"> <p>Permite especificar parámetros de búsqueda predeterminados. Cuando se muestra la vista de datos por primera vez, estos parámetros CGI se anexan automáticamente. </p> <p>No cambie ni elimine <span class="codeph"> sp_cs</span> o <span class="codeph"> sp_f</span>. Estos parámetros son esenciales para la vista de datos independientemente del conjunto de caracteres preferido de la cuenta. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parámetros</a>CGI de búsqueda back-end. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Estado de bloqueo </p> </td> 
      <td colname="col2"> <p>Permite bloquear o desbloquear la vista de datos. </p> <p>Puede ver una vista de datos bloqueada únicamente con una contraseña y un nombre de usuario. El usuario debe ser un miembro actual de la cuenta. </p> <p>Se accede a una vista de datos desbloqueada sin contraseña ni cuenta de usuario. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pedido </p> </td> 
      <td colname="col2"> <p> Permite cambiar el orden de las columnas editando el número en el cuadro de texto <span class="wintitle"> Orden</span> . También puede arrastrar y soltar una fila para cambiar el orden de las columnas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclusión </p> </td> 
      <td colname="col2"> <p> Permite activar o desactivar la visualización de la columna. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mostrar URL como imagen </p> </td> 
      <td colname="col2"> <p>Muestre miniaturas e imágenes en esta columna si el resultado de búsqueda de esta columna devuelve una dirección URL. </p> <p>La dirección URL se elimina del nombre o protocolo del esquema antes de convertirse en un valor del atributo <span class="codeph"> src</span> de una etiqueta de imagen. </p> <p>Si el resultado de búsqueda que se devuelve no tiene el aspecto de una dirección URL a una imagen, se muestra una. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Longitud del campo </p> </td> 
      <td colname="col2"> <p>Define el número de caracteres que se muestran como resultado en la vista de datos. </p> <p>El valor predeterminado es de 100 caracteres. </p> <p>Algunos campos, como la puntuación de clasificación y el campo de fecha, no tienen longitudes de campo ajustables. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copia de una vista de datos {#task_78D4C2799BC84677843ED4CA1CD205AF}

Puede copiar una vista de datos existente en la [!DNL Data Views] página para utilizarla como base para crear una nueva vista de datos.

Después de copiar una vista de datos, puede personalizarla aún más editando la vista.

Consulte [Edición de una vista](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)de datos.

**Para copiar una vista de datos**

1. En el menú de producto, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. En la [!DNL Data Views] página, en la [!DNL Actions] columna de la tabla, haga clic **[!UICONTROL Copy]** en la fila con la vista de datos que desee copiar.
1. En la [!DNL Copy Data View] página, en el campo de [!DNL New Title] texto, introduzca el nuevo nombre que desea asignar a la vista de datos.
1. Haga clic **[!UICONTROL Copy]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una vista de datos {#task_61C32F8F00A549A5A3E7EDDA6F537098}

Puede eliminar una vista de datos en la [!DNL Data Views] página que ya no necesite o utilice.

**Para eliminar una vista de datos**

1. En el menú de producto, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. En la [!DNL Data Views] página, en la [!DNL Actions] columna de la tabla, haga clic **[!UICONTROL Delete]** en la fila con la vista de datos que desee eliminar.
1. En la [!DNL Delete Data View] página, haga clic en **Eliminar**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Visualización de una vista de datos {#task_FD0D2CE53DF84CBD9220AD7CA920011F}

Puede usar [!DNL View] en la [!DNL Data Views] página para mostrar una vista de datos seleccionada.

La vista de datos seleccionada se abre en una ventana separada del explorador.

**Para ver una vista de datos**

1. En el menú de producto, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Realice una de las siguientes acciones:

   * En la [!DNL Data Views] página, en la [!DNL Title] columna de la tabla, haga clic en el nombre de una vista de datos que desee abrir.

   * En la [!DNL Data Views] página, en la [!DNL Actions] columna de la tabla, haga clic **[!UICONTROL View]** en la fila con la vista de datos que desee abrir.

