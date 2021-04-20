---
description: Puede utilizar los menús para personalizar la capa de presentación.
solution: Target
subtopic: Navigation
title: Acerca de los menús
topic: Design,Site search and merchandising
uuid: 011050cd-21b6-4150-9503-18fa3f771626
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 1%

---


# Acerca de los menús{#about-menus}

Puede utilizar los menús para personalizar la capa de presentación.

## Uso de menús {#concept_68123CE5CF4447B59217B5D721424E32}

Agregue menús que se asignen a la configuración dentro de la búsqueda. Cada elemento de un menú especifica el valor de la configuración del menú. También puede personalizar las etiquetas de menú.

En la plantilla de presentación, puede hacer referencia a los menús definidos. A continuación, puede colocarlos en cualquier componente HTML que desee, como un control seleccionado. Esta combinación permite a los usuarios personalizar sus resultados de búsqueda. Se admiten tres tipos de menú: ordenar, contar y navegar.

## Adición de un nuevo menú {#task_EE171532D3AE477FAFE8C2F4077A6D73}

Puede agregar menús que se asignen a la configuración dentro de los resultados de búsqueda.

<!-- 

t_adding_a_new_menu.xml

 -->

>[!NOTE]
>
>Asegúrese de hacer referencia al menú en la plantilla de presentación para que esté visible en el sitio web.

**Adición de un nuevo menú**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**.
1. En la página [!DNL Menus], haga clic en **[!UICONTROL Add New Menu]**.
1. En la página [!DNL Add Menu], configure las opciones que desee.

   Estos ajustes afectan tanto al comportamiento como a la presentación predeterminada de una ruta de exploración. Puede anular algunos de estos ajustes mediante la configuración de la plantilla de presentación.

   Consulte [Acerca de los menús](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

   <!-- 
   r_add_menu_options.xml
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
      <td colname="col1"> <p>Nombre del menú </p> </td> 
      <td colname="col2"> <p>Nombre del menú. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo de menú </p> </td> 
      <td colname="col2"> <p>Establece uno de los tres tipos de menú siguientes: </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
      <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> Ordenar  </span> <p>Organiza la búsqueda según cualquiera de los tipos de metadatos definidos. </p> <p>Por ejemplo, puede definir un menú de ordenación con los siguientes tipos de metadatos: tres temas pertinentes; un campo de metadatos personalizado, como un código de disponibilidad; y precio. A los tres artículos se les pueden dar las etiquetas "Ordenar por relevancia", "Ordenar por Disponibilidad" y "Ordenar por Precio", respectivamente. Cuando lo incluye en la plantilla de presentación, el cliente puede utilizar este control para ordenar los resultados de búsqueda. </p> </li> 
      <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> Recuento </span> <p>Define el número de resultados de búsqueda que se mostrarán. Este tipo de menú se asigna al parámetro cgi <span class="varname"> sp_c </span>. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> Parámetros CGI de búsqueda back-end </a>. </p> </li> 
      <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> Navegación </span> <p>Especifica un conjunto de direcciones URL estáticas asociadas a elementos de menú. Normalmente, se utiliza un menú de navegación para crear una barra de navegación de nivel superior en la página de resultados de búsqueda. </p> <p>Por ejemplo, puede crear un menú que contenga mujeres, hombres, niños y niñas, donde los elementos del menú sean algo así como los siguientes: 
      <code>
        /?q1=womens;x1=gender 
      </code>, 
      <code>
        /?q1=mens;x1=gender 
      </code> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Comercialización </p> 
        <!--DONT' KNOW WHAT THIS DOES--> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige el tipo de menú <span class="uicontrol"> Ordenar. </span> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de elementos del menú </p> </td> 
      <td colname="col2"> <p>Especifica el número de elementos de un menú. Si se cambia esta configuración, se añaden o eliminan campos del formulario. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Elemento predeterminado </p> </td> 
      <td colname="col2"> <p>Permite seleccionar qué elemento de menú se muestra de forma predeterminada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor del elemento </p> </td> 
      <td colname="col2"> <p>El valor del elemento depende del tipo de menú que haya establecido. </p> 
        <ul id="ul_2F14E6AA673640578A2D5161FD9D13EF"> 
        <li id="li_5017EC6E4ACB4B8E99E0AA61CBAAFFAE"> Tipo de menú Ordenar <p>Identifica por qué debería ordenar el elemento seleccionado en el menú. Los elementos seleccionados se rellenan con campos de metadatos que se pueden ordenar. </p> <p>Para un solo elemento, puede ordenar por tres campos de metadatos. La ordenación se realiza en el orden especificado. </p> </li> 
        <li id="li_CC6BAFBF969C4367A71B55F08E0758D1"> Tipo de menú Recuento <p>Permite especificar el número de resultados que desea que se devuelvan cuando el cliente seleccione este elemento de menú. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Etiqueta del elemento </p> </td> 
      <td colname="col2"> <p>La etiqueta de elemento depende del tipo de menú que haya establecido. </p> 
        <ul id="ul_957BF01235F84748B5EB7062D6AEAC41"> 
        <li id="li_03FB2E2C96134A2B8E08154F87F0CD55"> Tipo de menú Ordenar <p>Identifica la etiqueta personalizada que desea que vea su cliente cuando vea este elemento en el menú. </p> </li> 
        <li id="li_C9FE2BC46D9443FB85FEB837C7CA45E1"> Tipo de menú Recuento <p>Identifica la etiqueta personalizada que desea que se muestre para este elemento de menú. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Add]**.
1. (Opcional) En la página [!DNL Menus], realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de un menú {#task_0770DBFD0C7046169097FB6F771B9114}

Puede editar la configuración de cualquier menú que haya agregado.

<!-- 

t_editing_a_menu.xml

 -->

>[!NOTE]
>
>Asegúrese de hacer referencia al menú en la plantilla de presentación para que esté visible en el sitio web.

**Edición de menús**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**.
1. En la página [!DNL Menus], haga clic en **[!UICONTROL Edit]** a la derecha del nombre de un menú.
1. En la página [!DNL Edit Menu], configure las opciones que desee.

   Consulte la tabla de opciones en [Adición de un nuevo menú](../c-about-design-menu/c-about-menus.md#task_EE171532D3AE477FAFE8C2F4077A6D73).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) En la página [!DNL Menus], realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de un menú {#task_645E212311A045CD8D9D906878165F47}

Puede eliminar cualquier menú que haya agregado.

<!-- 

t_deleting_a_menu.xml

 -->

**Eliminación de un menú**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**
1. En la página [!DNL Menus], haga clic en **[!UICONTROL Delete]** a la derecha del nombre de un menú.
1. En el cuadro de diálogo [!DNL Confirmation], haga clic en **[!UICONTROL OK]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

