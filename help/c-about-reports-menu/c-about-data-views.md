---
description: Vistas de datos muestra los resultados de la búsqueda con los meta campos. Cada columna es un meta campo y cada fila es el resultado de una consulta de búsqueda. Personalice las vistas de datos eligiendo y reorganizando columnas. Las vistas de datos también pueden tener títulos y descripciones personalizados.
solution: Target
title: Acerca de las vistas de datos
topic-legacy: Reports,Site search and merchandising
uuid: 18930551-960d-40c2-b5b7-0807a2e11134
exl-id: 9ef5eaef-85d6-41e9-af44-b4775755e5bf
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 1%

---

# Acerca de las vistas de datos{#about-data-views}

Vistas de datos muestra los resultados de la búsqueda con los meta campos. Cada columna es un meta campo y cada fila es el resultado de una consulta de búsqueda. Personalice las vistas de datos eligiendo y reorganizando columnas. Las vistas de datos también pueden tener títulos y descripciones personalizados.

## Uso de Vistas de datos {#concept_DCA897D074464BC1861AA47B40CC86C3}

Cada cuenta tiene la conveniencia de crear varias vistas de datos. Utilice la página Vistas de datos para crear y editar estas vistas de datos.

Después de agregar una vista de datos, debe editarla para configurarla y personalizarla.

Consulte [Edición de una vista de datos](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516).

Puede copiar una vista de datos existente para utilizarla como base para crear una nueva vista de datos.

Consulte [Copia de una vista de datos](../c-about-reports-menu/c-about-data-views.md#task_78D4C2799BC84677843ED4CA1CD205AF).

## Adición de una vista de datos {#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D}

Puede agregar una vista de datos a la página [!DNL Data Views] para mostrar los valores de cada meta campo con una consulta de búsqueda.

Después de agregar una vista de datos, debe editarla para configurarla y personalizarla.

Consulte [Edición de una vista de datos](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516).

**Adición de una vista de datos**

1. En el menú del producto, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. En la página [!DNL Data Views], haga clic en **[!UICONTROL Add New Data View]**.
1. En el cuadro de diálogo [!DNL Add New Data View], en el campo [!DNL Title], introduzca el nombre de la vista de datos que desea crear.
1. Haga clic **[!UICONTROL Add]**.

## Edición de una vista de datos {#task_258A367896C24DD498C755925EA8F516}

Al agregar una vista de datos a la página [!DNL Data Views], utilice Editar para cambiar el nombre y la descripción de la vista de datos o para mover, mostrar u ocultar la visualización de cada meta campo.

También puede bloquear o desbloquear una vista de datos seleccionada.

Consulte [Adición de una vista de datos](../c-about-reports-menu/c-about-data-views.md#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D).

**Edición de una vista de datos**

1. En el menú del producto, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. En la página [!DNL Data Views], en la columna [!DNL Actions] de la tabla, haga clic **[!UICONTROL Edit]** en la fila con la vista de datos que desea cambiar.
1. En la página [!DNL Data Views Editor], configure las opciones que desee.

   El Editor de vista de datos tiene todos los controles para ocultar, mostrar y mover columnas de campo en la página Vista de datos.

   Al ver una vista de datos, la tabla resultante también muestra los siguientes campos de columna adicionales que no son editables: Clasificación, relevancia y puntuación (general). Estos tres campos especiales representan las puntuaciones de relevancia, las puntuaciones de clasificación y las puntuaciones generales de cada resultado.

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
      <td colname="col2"> <p>Nombre de la vista de datos. El nombre se muestra en la parte superior derecha cuando se ve la vista de datos. </p> <p>Consulte <a href="../c-about-reports-menu/c-about-data-views.md#task_FD0D2CE53DF84CBD9220AD7CA920011F" type="task" format="dita" scope="local"> Visualización de una vista de datos</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Descripción </p> </td> 
      <td colname="col2"> <p>(Opcional) Contiene una descripción de la vista de datos. La descripción se muestra entre el nombre del título de la vista de datos y el campo de texto <span class="wintitle"> Nueva búsqueda</span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetros de búsqueda </p> </td> 
      <td colname="col2"> <p>Permite especificar parámetros de búsqueda predeterminados. Cuando la vista de datos se muestra por primera vez, estos parámetros CGI se anexan automáticamente. </p> <p>No cambie ni elimine <span class="codeph"> sp_cs</span> o <span class="codeph"> sp_f</span>. Estos parámetros son esenciales para la vista de datos independientemente del conjunto de caracteres preferido de la cuenta. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parámetros CGI de búsqueda back-end</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Estado de bloqueo </p> </td> 
      <td colname="col2"> <p>Permite bloquear o desbloquear la vista de datos. </p> <p>Puede ver una vista de datos bloqueados únicamente con una contraseña y un nombre de usuario. El usuario debe ser un miembro actual de la cuenta. </p> <p>Se accede a una vista de datos desbloqueada sin contraseña ni cuenta de usuario. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pedido </p> </td> 
      <td colname="col2"> <p> Permite cambiar el orden de las columnas editando el número en el cuadro de texto <span class="wintitle"> Ordenar</span>. También puede arrastrar y soltar una fila para cambiar el orden de las columnas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclusión </p> </td> 
      <td colname="col2"> <p> Permite activar o desactivar la visualización de la columna. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mostrar URL como imagen </p> </td> 
      <td colname="col2"> <p>Mostrar miniaturas e imágenes en esta columna si el resultado de la búsqueda de esta columna devuelve una dirección URL. </p> <p>La URL se elimina de su protocolo o nombre de esquema antes de convertirse en un valor del atributo <span class="codeph"> src</span> de una etiqueta de imagen. </p> <p>Si el resultado de búsqueda que se devuelve no parece una dirección URL a una imagen, se muestra un . </p> </td> 
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

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copia de una vista de datos {#task_78D4C2799BC84677843ED4CA1CD205AF}

Puede copiar una vista de datos existente en la página [!DNL Data Views] para utilizarla como base para crear una nueva vista de datos.

Después de copiar una vista de datos, puede personalizarla aún más editando la vista.

Consulte [Edición de una vista de datos](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516).

**Para copiar una vista de datos**

1. En el menú del producto, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. En la página [!DNL Data Views], en la columna [!DNL Actions] de la tabla, haga clic en **[!UICONTROL Copy]** en la fila con la vista de datos que desea copiar.
1. En la página [!DNL Copy Data View], en el campo de texto [!DNL New Title], introduzca el nuevo nombre que desea asignar a la vista de datos.
1. Haga clic **[!UICONTROL Copy]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una vista de datos {#task_61C32F8F00A549A5A3E7EDDA6F537098}

Puede eliminar una vista de datos en la página [!DNL Data Views] que ya no necesite ni utilice.

**Eliminación de una vista de datos**

1. En el menú del producto, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. En la página [!DNL Data Views], en la columna [!DNL Actions] de la tabla, haga clic en **[!UICONTROL Delete]** en la fila con la vista de datos que desea eliminar.
1. En la página [!DNL Delete Data View], haga clic en **Eliminar**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Visualización de una vista de datos {#task_FD0D2CE53DF84CBD9220AD7CA920011F}

Puede utilizar [!DNL View] en la página [!DNL Data Views] para mostrar una vista de datos seleccionada.

La vista de datos que seleccione se abre en una ventana independiente del explorador.

**Para ver una vista de datos**

1. En el menú del producto, haga clic en **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Realice una de las siguientes acciones:

   * En la página [!DNL Data Views], en la columna [!DNL Title] de la tabla, haga clic en el nombre de una vista de datos que desee abrir.

   * En la página [!DNL Data Views], en la columna [!DNL Actions] de la tabla, haga clic **[!UICONTROL View]** en la fila con la vista de datos que desea abrir.
