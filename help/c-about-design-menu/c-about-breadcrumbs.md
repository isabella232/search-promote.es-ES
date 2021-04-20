---
description: Las rutas de exploración son un control de navegación que puede agregar al sitio web. La ruta de exploración proporciona a los clientes información sobre dónde se encuentran dentro de un conjunto de resultados de búsqueda. También les ayuda a volver rápidamente a un paso anterior.
solution: Target
subtopic: Navigation
title: Acerca de las rutas de exploración
topic: Design,Site search and merchandising
uuid: 3e630a72-a631-4f4f-8aa5-adf2882cdf1c
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 1%

---


# Acerca de las rutas de exploración{#about-breadcrumbs}

Las rutas de exploración son un control de navegación que puede agregar al sitio web. La ruta de exploración proporciona a los clientes información sobre dónde se encuentran dentro de un conjunto de resultados de búsqueda. También les ayuda a volver rápidamente a un paso anterior.

## Uso de rutas de exploración {#concept_FB8A943C594A4A1593B118141DA61F03}

Las rutas de exploración rastrean el término buscado y las facetas siguientes que se seleccionaron para reducir el conjunto de resultados.

Utilice la configuración de la ruta de exploración para personalizar el control de la ruta de exploración de la capa de presentación de búsqueda. Si la capa de presentación tiene más de un conjunto de resultados de búsqueda, el control de la ruta actúa en la búsqueda principal de la página.

Puede editar una ruta de exploración para cambiar el comportamiento predeterminado, el ancho máximo del valor y la extensión del valor, y para seleccionar si desea incluir el término de consulta.

## Adición de una nueva ruta de exploración {#task_2FFA94F82AE74F10BDDE7367CDCEAE8B}

Puede agregar una barra de rutas de exploración para que un cliente pueda rastrear dónde se encuentran en el sitio web.

<!-- 

t_adding_a_new_breadcrumb.xml

 -->

>[!NOTE]
>
>Asegúrese de hacer referencia a la ruta en la plantilla de presentación para que esté visible en el sitio web.

**Para agregar una nueva ruta de exploración**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. En la página [!DNL Breadcrumbs], haga clic en **[!UICONTROL Add Breadcrumb]**.
1. En la página [!DNL Add Breadcrumb], configure las opciones que desee.

   Estos ajustes afectan tanto al comportamiento como a la presentación predeterminada de una ruta de exploración. Puede anular algunos de estos ajustes mediante la configuración de la plantilla de presentación.

   <!-- 
   
   r_breadcrumb_options.xml
    
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
      <td colname="col1"> <p>Nombre de la ruta de navegación </p> </td> 
      <td colname="col2"> <p>Nombre de la ruta de exploración. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Comportamiento </p> </td> 
      <td colname="col2"> <p>Establece uno de los tres comportamientos de ruta de exploración siguientes: </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
        <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> Ir  </span> <p>Vaya a elimina todas las rutas después del en el que se hace clic y comienza una nueva búsqueda en ese punto. </p> </li> 
        <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> Eliminar </span> <p>Eliminar elimina de la ruta la ruta en la que hizo clic el cliente y, a continuación, inicia una nueva búsqueda. Este comportamiento es útil cuando desea permitir que el cliente anule los pasos para explorar en profundidad la búsqueda. </p> </li> 
        <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> Borrar  </span> <p>Borrar elimina todas las rutas de exploración. </p> </li> 
      </ul> </p> <p> Por ejemplo, supongamos que tiene una ruta de exploración de 1 &gt; 2 &gt; 3 &gt; 4. Cuando un cliente hace clic en "2", tiene los siguientes resultados, según el comportamiento que haya elegido: </p> <p> 
      <ul id="ul_96FCD8E4C3704B45B59BC18A7A1AC52A"> 
        <li id="li_B880037088DF426F880788EAA3072180">Vaya A - 1 &gt; 2 </li> 
        <li id="li_D0F07A15DCD043EFA4563632ED33A9E2">Quitar - 1 &gt; 3 &gt; 4 </li> 
        <li id="li_D848ED44B4E44538AA92010F9F186224"> Colocar : se abandona toda la ruta de exploración, lo que hace que el cliente vuelva al punto antes de comenzar a explorar en profundidad. </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ancho máximo del valor </p> </td> 
      <td colname="col2"> <p>Especifica la longitud de cada valor en la ruta de exploración. La configuración se especifica como un número de caracteres. </p> <p>Por ejemplo, un valor de 6 significa que la ruta de exploración puede tener hasta 6 caracteres, incluidos espacios. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Extensión de valor </p> </td> 
      <td colname="col2"> <p>Especifica los puntos suspensivos que se utilizarán cuando se trunca una ruta de exploración. </p> <p>De forma predeterminada, un "..." (elipses). </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir término de consulta </p> </td> 
      <td colname="col2"> <p>Controla la presencia de términos de consulta en una ruta de exploración. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Habilitar rutas de exploración definidas por el usuario </p> </td> 
      <td colname="col2"> <p>Marque para permitirle utilizar los elementos definidos por el usuario en las rutas de exploración utilizando los parámetros <span class="codeph"> uX=[name]&amp;[name]=[value] </span> en la dirección URL. Puede utilizar reglas de procesamiento para gestionar estos parámetros del modo que desee. </p> <p>Por ejemplo, si esta función está habilitada y tiene la dirección URL, <code> https://search.host.com/?1=category&amp;q1=Clothes&amp;u2= 
          type&amp;type=Men&amp;x3=kind&amp;q3=Sweater </code> en caso de que tenga facetas <span class="codeph"> <span class="varname"> categoría </span> </span> y <span class="codeph"> <span class="varname"> </span> </span>, la ruta será similar a <span class="codeph"> Ropa &gt; Hombres &gt; Suéter </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombres de rutas definidos por el usuario </p> </td> 
      <td colname="col2"> <p>Lista separada por comas de todos los nombres posibles de elementos de ruta de exploración definidos por el usuario. </p> <p>Esta opción solo está disponible si marca <span class="uicontrol"> Habilitar rutas de exploración definidas por el usuario </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Add]**.
1. (Opcional) En la página [!DNL Breadcrumbs], realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una ruta de exploración {#task_583481D9A23E4E0F97AEB18E72CBE13F}

Puede editar la configuración de cualquier ruta de exploración que haya agregado.

<!-- 

t_editing_a_breadcrumb.xml

 -->

>[!NOTE]
>
>Asegúrese de hacer referencia a la ruta en la plantilla de presentación para que esté visible en el sitio web.

**Para editar una ruta de exploración**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. En la página [!DNL Breadcrumbs], haga clic en **[!UICONTROL Edit]** a la derecha del nombre de una ruta de exploración.
1. En la página [!DNL Edit Breadcrumb], configure las opciones que desee.

   Consulte la tabla de opciones en [Adición de una nueva ruta de exploración](../c-about-design-menu/c-about-breadcrumbs.md#task_2FFA94F82AE74F10BDDE7367CDCEAE8B).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) En la página **[!UICONTROL Breadcrumb]**, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una ruta de exploración {#task_401C6E481A744284906E15A29E04F757}

Puede eliminar cualquier ruta de exploración que haya agregado.

<!-- 

t_deleting_a_breadcrumb.xml

 -->

**Eliminación de una ruta de exploración**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. En la página [!DNL Breadcrumbs], haga clic en **[!UICONTROL Delete]** a la derecha del nombre de una ruta de exploración.
1. En el cuadro de diálogo [!DNL Confirmation], haga clic en **[!UICONTROL OK]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

