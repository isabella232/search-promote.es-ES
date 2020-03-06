---
description: Puede utilizar los letreros para administrar las publicidades de letreros en el sitio web.
seo-description: Puede utilizar los letreros para administrar las publicidades de letreros en el sitio web.
seo-title: Acerca de banners
solution: Target
title: Acerca de banners
topic: Design,Site search and merchandising
uuid: 653b567d-5cf3-41a0-a260-a6912d0fd20d
translation-type: tm+mt
source-git-commit: 7f1b5d94e8002992d62ec1e3dce11f9c5605fde8

---


# Acerca de banners {#about-banners}

Puede utilizar los letreros para administrar las publicidades de letreros que hay en el sitio web.

## Uso de pancartas {#concept_5BBE01FEC6134393B43CC917C8CC64DA}

<!-- 

c_about_banners.xml

 -->

Existen dos métodos que puede utilizar para agregar publicidades de titular al sitio web.

El primer método consiste en agregar letreros mediante Target, Search&amp;Promote. Los letreros son fragmentos de código HTML que se muestran en el momento en que un cliente busca en el sitio web. La pancarta puede incluir texto o una imagen en formato GIF, JPEG o PNG, o una combinación de ambos. Puede seleccionar entre los tamaños preestablecidos o definir sus propias dimensiones personalizadas para que se ajusten a la página. El código HTML que se utiliza para mostrar la pancarta también puede especificar elementos como el estilo de fuente que se va a utilizar y el borde. Este método de adición de letreros ofrece funcionalidad básica y no requiere software adicional.

El segundo método consiste en utilizar Adobe Dynamic Media Classic, un servicio de administración y publicación de medios dinámicos. Una cuenta válida de Adobe Dynamic Media Classic le permite administrar y entregar contenido de letreros directamente en Target, Search&amp;Promote, mediante Dynamic Media Classic. En la búsqueda y comercialización del sitio, se configura el acceso a su cuenta de Dynamic Media Classic. A continuación, abra el navegador de medios de Dynamic Media Classic y seleccione un recurso de medios dinámicos que desee que sirva como pancarta.

>[!NOTE]
>
>Antes de utilizar los recursos de medios dinámicos como pancartas en la búsqueda o comercialización del sitio, los recursos se cargan y preparan para su publicación en Scene7 Publishing System. Puede cargar recursos desde la búsqueda o comercialización del sitio y prepararlos automáticamente para su publicación en Scene7 Publishing System. O bien, puede cargar y publicar recursos desde Scene7 Publishing System.

## Integración de letreros con Adobe Scene7 Publishing System {#section_D4D7ADEA6A6348E68EDA138E184FE579}

Puede utilizar los tipos de recursos de Dynamic Media Classic como pancartas en la búsqueda o comercialización del sitio, incluidas imágenes, pancartas dinámicas y plantillas, como plantillas de imagen o plantillas Flash.

Las plantillas son archivos de imagen direccionables en capas creados de forma dinámica, como archivos con capas en aplicaciones de edición de imágenes como Adobe Photoshop®. A diferencia de un archivo de imagen estático, una plantilla puede incluir parámetros. Mediante parámetros, puede personalizar las propiedades de imagen variables y el contenido de la imagen.

>[!NOTE]
>
>También puede crear plantillas a partir de diseños mediante Publicación de plantillas en Scene7 Publishing System y archivos de Adobe Illustrator y Adobe InDesign.

Consulte Publicación [de](https://help.adobe.com/en_US/scene7/using/WSFBFBAD30-2694-4b18-B7CE-894F9FC5CDDF.html) plantillas en la Guía del usuario de Dynamic Media Classic (Scene7).

Una plantilla puede contener cualquier número de capas de imagen y de texto. Puede convertir un archivo estático que contenga capas, como un archivo PSD con capas, en una plantilla o crear plantillas en Dynamic Media Classic. Puede crear capas de texto en plantillas con las fuentes cargadas en Scene7 Publishing System. Después de agregar texto a una plantilla, puede darle formato cambiando su justificación, fuentes, tamaño de fuente y color.

Con la pantalla Parámetros de Dynamic Media Classic, puede convertir cualquier aspecto de una plantilla en un parámetro direccionable. De este modo, puede cambiar qué imagen en capas utilizar o qué valor de texto utilizar en la plantilla. Los parámetros se pasan con la cadena URL, lo que permite cambiar cualquier parámetro para personalizar dinámicamente la imagen de respuesta generada desde el servidor de imágenes.

Puede obtener más información sobre cómo utilizar Dynamic Media Classic para crear plantillas y parametrizar las propiedades de las capas para poder utilizarlas en letreros.

Consulte Conceptos básicos [de plantilla](https://help.adobe.com/en_US/scene7/using/WS60B68844-9054-4099-BF69-3DC998A04D3C.html) en la Guía del usuario de Dynamic Media Classic (Scene7).

**Carga y publicación de recursos**

Debe cargar y publicar recursos en Dynamic Media Classic para poder utilizarlos en los letreros de la búsqueda o comercialización del sitio. Este requisito previo también incluye los recursos que utiliza una plantilla de imagen o una plantilla Flash. Utilice su cuenta de Dynamic Media Classic para cargar y publicar recursos digitales. O bien, puede utilizar la búsqueda o comercialización del sitio para cargar un recurso digital y, a continuación, hacer que Dynamic Media Classic lo publique automáticamente en función de la configuración de carga. Si intenta elegir un recurso que aún no se ha cargado ni publicado, se le notificará en la interfaz de usuario y se le dará la opción de cargarlo antes de continuar.

Puede obtener más información sobre la carga y publicación de recursos digitales con Scene7 Publishing System.

Consulte [Carga y publicación de recursos](https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html) en la Guía del usuario de Dynamic Media Classic (Scene7).

>[!NOTE]
>
>Para utilizar la funcionalidad de carga en el visor de recursos de Dynamic Media Classic, asegúrese de que la cuenta de Dynamic Media Classic que utiliza ya tiene la función de &quot;Administrador de la empresa de SPS&quot; establecida.

Consulte Ajustes [de](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) administración en la Guía del usuario de Dynamic Media Classic (Scene7).

**Cambio de los parámetros de plantilla de Dynamic Media Classic en un letrero mediante reglas comerciales**

Si ha agregado un recurso de Dynamic Media Classic como letrero, puede utilizarlo [!DNL Visual Rule Builder] en [!DNL Business Rules] para agregarlo a cualquier área de letrero del sitio web. Por ejemplo: agrega la pancarta a las páginas de resultados de búsqueda, como lo haría con cualquier otra pancarta. También puede anular los valores de parámetro predeterminados en las plantillas de Dynamic Media Classic personalizándolos según sus necesidades específicas. Este tipo de funcionalidad le permite personalizar plantillas de Dynamic Media Classic con diferentes mensajes de marketing e hipervínculos a diferentes extremos.

Consulte también [Adición de una nueva regla](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)comercial.

Consulte también [Edición de una regla](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087)comercial.

## Adición de una pancarta {#task_549D02B5F73B4158B105A94E39D937B7}

Puede utilizar [!DNL Banners] para administrar las publicidades de titular y su ubicación en el sitio web. Al agregar un letrero, se hace referencia externamente a la imagen mediante fragmentos de código HTML que se muestran en el momento de la búsqueda.

<!-- 

t_adding_a_new_banner.xml

 -->

Si tiene una cuenta válida de Adobe Dynamic Media Classic, puede agregar anuncios de letreros a través de Scene7 Publishing System.

Consulte [Adición de letreros con Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

Consulte [Configuración del acceso a su cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D)de Adobe Dynamic Media Classic.

**Para agregar una pancarta**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. En la lista [!DNL Banners] desplegable de la **[!UICONTROL Add Banner]** página, seleccione **[!UICONTROL HTML code]**.
1. En el cuadro de diálogo [!DNL Add Banner] , configure las opciones que desee.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nombre </p> </td> 
      <td colname="col2"> <p>Requerido. Identifica el nombre del letrero. El nombre se utiliza para hacer referencia a la pancarta cuando se agrega en el Generador de reglas visuales en reglas comerciales. El nombre no aparece en la pancarta misma. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" type="task" format="dita" scope="local"> Adición de una nueva regla comercial.</a> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>HTML de pancarta </p> </td> 
      <td colname="col2"> <p> Permite pegar el código HTML asociado a la pancarta. </p> <p>Se acepta cualquier código HTML, incluido el código CSS rodeado por 
        <userinput>
          &lt;estilo&gt; 
        </userinput> o código JavaScript rodeado por 
        <userinput>
          &lt;script&gt; 
        </userinput> etiquetas. Por ejemplo, el siguiente bloque de código es para una pancarta de texto de tipo Horizontal top: <code> &lt;div&nbsp;style="width:&nbsp;684px;&nbsp;background-image:&nbsp;url('https://www.brough.com/blackb.gif');&nbsp; 
          padding-top:&nbsp;10px;&nbsp;padding-bottom:&nbsp;10px;&nbsp;color:&nbsp;white;&nbsp;font-family:&nbsp;verdana;&nbsp; 
          text-align:&nbsp;center;&nbsp;font-size:&nbsp;20px;"&gt;&nbsp;Sound&nbsp;Study&nbsp;ships&nbsp;free!&nbsp;&lt;/div&gt; </code>En el ejemplo siguiente, el bloque de código es para una imagen de bienvenida completa: <code> &lt;img&amp;nbsp;src='https://geometrixx.com/images/GEOAds/geometrixx-beauty-home-01.jpg'&amp;nbsp;border="0"&amp;nbsp;/&gt; </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo  </p> </td> 
      <td colname="col2"> <p>Especifica los siguientes tipos de pancartas: 
        <ul id="ul_6423AEDB9E664049989EB529D63C4A62"> 
          <li id="li_BF6CD60B3ED748D49CFFB9C5D607661C"> <span class="uicontrol"> [nuevo tipo] </span> <p>Permite especificar el tipo de pancarta que desea, incluidas las dimensiones y el nombre. </p> </li> 
          <li id="li_1A29AB22AD644E60A12298187B5E898E"> <span class="uicontrol"> Presentación completa </span> <p>La dimensión establecida de este tipo de pancarta es de 680 píxeles de ancho y 650 píxeles de alto. De forma opcional, puede especificar el nombre del tipo o aceptar el nombre predeterminado, que es el nombre del tipo de pancarta en sí. </p> </li> 
          <li id="li_2BE06D013CB54DDE851051BFC038BB57"> <span class="uicontrol"> Superior horizontal </span> <p> La pancarta se coloca en el área superior del sitio web. Este tipo resulta útil si desea agregar hipervínculos a la izquierda o a la derecha del letrero. La dimensión establecida de este tipo de pancarta es de 468 píxeles de ancho y 60 píxeles de alto. De forma opcional, puede especificar el nombre del tipo o aceptar el nombre predeterminado, que es el nombre del tipo de pancarta en sí. </p> </li> 
          <li id="li_EC35AB92234749F08AA8A9BD26D0EA8D"> <span class="uicontrol"> Parte superior horizontal - Ancho completo </span> <p>Este tipo es el predeterminado cuando se agrega una nueva pancarta. La pancarta se coloca en el área superior del sitio web y ocupa toda la anchura de la página. La dimensión establecida de este tipo de pancarta es de 670 píxeles de ancho y 150 píxeles de alto. De forma opcional, puede especificar el nombre del tipo o aceptar el nombre predeterminado, que es el nombre del tipo de pancarta en sí. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Etiquetas </p> </td> 
      <td colname="col2"> <p>Agrega etiquetas o "palabras clave" que desea asociar con la pancarta. Si utiliza muchos letreros, la adición de etiquetas puede ayudarle a restringir la búsqueda de letreros para que pueda localizar rápidamente el letrero adecuado según sus necesidades. También puede eliminar cualquier etiqueta que haya agregado. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de letreros {#task_D4081083BE7B40F5A003D1A2F1435AEA}

Utilícelo [!DNL Edit Banner] para cambiar el nombre del letrero, el HTML del letrero, el tipo de pancarta y las etiquetas asociadas.

<!-- 

t_editing_a_banner.xml

 -->

Si agregó un letrero mediante la búsqueda o comercialización del sitio, también lo editará con Adobe Dynamic Media Classic.

Consulte también [Edición de letreros con Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

**Para editar una pancarta**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. En la [!DNL Banners] página, haga clic en ![](assets/icon_edit_16.gif).

   encima de una miniatura de pancarta que desee editar.
1. En la [!DNL Edit Banner] página, configure las opciones que desee.

   Consulte la tabla de opciones en [Adición de un letrero](../c-about-design-menu/c-about-banners.md#task_549D02B5F73B4158B105A94E39D937B7).
1. Cuando haya terminado de editar la pancarta, haga clic en **[!UICONTROL Save]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Adición de una pancarta con Adobe Dynamic Media Classic {#task_AD1E0C00A9E04B1FA819EB93288786B3}

Puede utilizar [!DNL Banners] para administrar las publicidades de titular del sitio web. Al agregar un letrero con Adobe Dynamic Media Classic, puede elegir entre cualquier recurso digital que haya cargado en Scene7 Publishing System.

<!-- 

t_adding_a_banner_using_adobe_scene7.xml

 -->

Para agregar un letrero con Adobe Dynamic Media Classic, asegúrese de haber configurado el acceso a su cuenta válida de Dynamic Media Classic.

Consulte [Configuración del acceso a su cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D)de Adobe Dynamic Media Classic.

**Adición de letreros mediante Adobe Dynamic Media Classic**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Banners.]**
1. En la [!DNL Banners] lista **[!UICONTROL Add Banner]** desplegable de la página, haga clic en **[!UICONTROL Adobe Scene7]**.
1. En el cuadro de diálogo [!DNL Pick an Asset] , en el panel izquierdo, utilice las opciones de navegación de la interfaz de usuario para localizar la carpeta que contiene el recurso digital que desea utilizar para un letrero.

   Con excepción de las opciones de navegación de recursos, el resto de las opciones dependen del recurso digital que haya seleccionado para agregar o editar.

   Utilice las opciones de navegación de recursos para localizar un recurso que desee utilizar para un letrero nuevo en la búsqueda o comercialización del sitio. Las opciones de navegación se aplican a todos los tipos de recursos digitales seleccionados.

   >[!NOTE]
   >
   >Las opciones de navegación de recursos no aparecen cuando se edita la pancarta en el cuadro de [!DNL Change Parameters] diálogo.

   Consulte [Edición de letreros con Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   **Opciones de navegación de recursos**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción de navegación </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/S7_folders.png"> </p> </td> 
      <td colname="col2"> <p>Permite seleccionar la cuenta de Dynamic Media Classic para una empresa en particular en la lista desplegable y también desplazarse por las carpetas de recursos digitales de esa cuenta. </p> <p>Al seleccionar una carpeta, el panel derecho del cuadro de diálogo <span class="wintitle"> Elegir un recurso </span> muestra todos los recursos digitales disponibles que se encuentran en esa carpeta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_folderhistory.png"> </p> </td> 
      <td colname="col2"> <p>Permite avanzar o retroceder en el historial de navegación de carpetas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_reloadfolder.png"> </p> </td> 
      <td colname="col2"> <p>Actualiza la lista de recursos digitales que se muestran para una carpeta seleccionada. </p> <p>Es posible que deba hacer clic en este control si mueve, elimina o cambia el nombre de un recurso seleccionado mediante la lista desplegable <span class="uicontrol"> Acciones </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_list_or_grid.png"> </p> </td> 
      <td colname="col2"> <p>Muestra los recursos digitales en una vista de lista. La lista muestra el icono o la imagen en miniatura asociados a cada recurso, el nombre del archivo, el tipo de recurso digital, las dimensiones (cuando corresponde) y la fecha en que se editó por última vez. </p> <p>La vista de cuadrícula muestra los recursos digitales de la carpeta seleccionada como iconos, miniaturas o ambos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_actionsdropdown.png"> </p> </td> 
      <td colname="col2"> <p>En la vista de lista, puede mover, eliminar o cambiar el nombre de un recurso digital seleccionado. </p> <p>En la vista de cuadrícula, puede mover o eliminar uno o varios recursos digitales seleccionados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_upload.png"> </p> </td> 
      <td colname="col2"> <p>Abre el cuadro de diálogo <span class="wintitle"> Cargar </span> , donde puede cargar un recurso digital seleccionado desde el escritorio o desde un servidor externo para que pueda utilizarlo como letrero. </p> <p>Después de cargar el recurso, un trabajo de publicación se programa automáticamente en Scene7 Publishing System. </p> <p>Consulte la tabla de opciones en <a href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita" scope="local"> Adición de letreros con Adobe Dynamic Media Classic </a>. </p> <p>Puede obtener más información sobre la carga y publicación de recursos digitales con Scene7 Publishing System. </p> <p>Consulte <a href="https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html" scope="external" format="html"> Carga y publicación de recursos </a> en la Guía del usuario de Scene7 Publishing System. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_searchfield.png"> </p> </td> 
      <td colname="col2"> <p>Permite buscar un recurso digital por palabra clave o por ubicación de archivo dentro de la carpeta seleccionada y sus subcarpetas asociadas. </p> <p>Al hacer clic en el campo de búsqueda, automáticamente se agrega un campo de filtro opcional. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>Agrega otro filtro de recursos para que pueda reducir aún más la lista de recursos digitales mostrados por tipo o por una fecha específica. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_Kindfilter.png"> </p> </td> 
      <td colname="col2"> <p>Restrinja la lista de recursos digitales mostrados para mostrar solo aquellos de un tipo determinado, como Flash, Imagen, Plantilla o Cualquiera. </p> <p>Haga clic en <img src="assets/s7_deletefilter.png"> para eliminar el filtro de la búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_datefilter.png"> </p> </td> 
      <td colname="col2"> <p>Restrinja la lista de recursos digitales mostrados para mostrar solo los creados o editados antes de una fecha determinada o después de una fecha determinada. </p> <p>Haga clic en <img src="assets/s7_deletefilter.png" /> para eliminar el filtro de la búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_assetzoom.png"> </p> </td> 
      <td colname="col2"> <p>Permite arrastrar el control deslizante hacia la izquierda o la derecha para reducir o ampliar la vista completa del panel de recursos digitales, respectivamente. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opciones de propiedades**

   Las opciones de Propiedades aparecen si selecciona una plantilla Flash, una plantilla de imagen o una imagen. Según el recurso digital que elija, no todas las opciones están disponibles.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Propiedades, opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nombre </p> </td> 
      <td colname="col2"> <p>Nombre descriptivo de la plantilla o imagen, sin espacios en blanco. Si lo desea, puede incluir la especificación de tamaño de imagen en el nombre para ayudar a los usuarios a identificar mejor el recurso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formato </p> </td> 
      <td colname="col2"> <p>Identifica el formato de la imagen o plantilla de imagen. </p> <p>Puede elegir entre los siguientes formatos: </p> 
        <ul id="ul_9A19421BCC424CF585645049DCB87F10"> 
        <li id="li_A4913D783BD547F9AFA1A259C56EC2B3">jpeg </li> 
        <li id="li_66237D7BE8754FB0B0088CE5A02C0214">png </li> 
        <li id="li_4EDDFD7C8AB04677BEC20EFC9AEBBF1F">png-alpha </li> 
        <li id="li_4FCB03C29AE647ACBAF5105016DF7579">gif </li> 
        <li id="li_B884BD7DFF1845FAA9C58EF09B888A77">gif-alpha </li> 
        </ul> <p>Esta opción no se aplica a las plantillas Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Calidad </p> </td> 
      <td colname="col2"> <p>Controla el nivel de compresión de las imágenes en formato JPEG o GIF. Esta configuración afecta tanto al tamaño del archivo como a la calidad de la imagen. La escala de calidad es de 1 a 100. </p> <p>Al arrastrar el control deslizante hacia la izquierda o la derecha, la imagen de la ventana de vista previa se actualiza para reflejar el cambio de calidad. </p> <p>Esta opción no se aplica a las plantillas Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Anchura </p> </td> 
      <td colname="col2"> <p>Especifica la anchura del recurso digital, en píxeles. Esta dimensión es la anchura con la que los clientes que visitan el sitio web ven el recurso. </p> <p>Esta opción no se aplica a las plantillas Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Altura </p> </td> 
      <td colname="col2"> <p>Especifica la altura del recurso digital, en píxeles. Esta dimensión es la altura en la que el recurso lo ven los clientes que visitan el sitio web. </p> <p>Esta opción no se aplica a las plantillas Flash. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opciones de vínculo de pancarta**

   Las opciones de Vínculo de pancarta solo aparecen si ha seleccionado una imagen o una plantilla de imagen para la pancarta.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción Vínculo de pancarta </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Dirección URL del vínculo </p> </td> 
      <td colname="col2"> <p>Especifica la dirección URL con la que desea que el letrero se vincule cuando un cliente haga clic en la imagen. </p> <p>Si no desea que la pancarta se vincule a nada, deje el campo URL del vínculo en blanco. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Target </p> </td> 
      <td colname="col2"> <p>Especifica dónde se abre la pancarta vinculada, como una nueva ventana del explorador o una nueva ficha. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Modificar vínculos, opción**

   La opción Modificar vínculos aparece únicamente si ha seleccionado una plantilla Flash para el letrero.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Modificar vínculos, opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img placement="inline" id="image_EBB8159690C74D4692B5DF945B045E0B" src="assets/icon_edit_16.gif" /> </p> </td> 
      <td colname="col2"> <p>Permite editar el campo de vínculo URL que se utiliza en la plantilla Flash. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opciones de Reemplazar texto**

   Las opciones Reemplazar texto solo aparecen si selecciona una plantilla Flash para el letrero que tenga capas de texto editables.

   Los cambios que realice en el texto de la plantilla Flash se reflejarán en la ventana Vista previa.

   >[!NOTE]
   >
   >Si agrega un comando de búsqueda y reemplazo para reemplazar &quot;vaca&quot; por &quot;manzana&quot; y luego crea un segundo comando para reemplazar &quot;manzana&quot; por &quot;naranja&quot;, el segundo comando no tendrá efecto.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Reemplazar texto, opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>Agrega un campo de búsqueda y reemplazo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_deletefilter.png"> </p> </td> 
      <td colname="col2"> <p>Elimina un campo de búsqueda y reemplazo y restaura el texto utilizado anteriormente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Búsqueda  </p> </td> 
      <td colname="col2"> <p>Permite introducir un término de búsqueda de texto no vinculado dentro de las capas de la plantilla Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sustituya </p> </td> 
      <td colname="col2"> <p>Permite especificar el texto que desea insertar en lugar del texto que busca. </p> <p>Al pulsar <span class="uicontrol"> Intro </span> en este campo, la ventana de vista previa se actualiza con el texto de reemplazo. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opciones de parámetros**

   Las opciones de parámetros solo aparecen si selecciona una plantilla de imagen o una plantilla Flash para la pancarta. Las opciones de parámetro reales varían según cómo se haya creado y parametrizado la plantilla en Scene7 Publishing System. Por ejemplo, la plantilla puede parametrizar campos que le permiten cambiar cosas como texto, estilo de fuente, precio, códigos especiales utilizados para el envío gratuito, el tamaño de la imagen dentro de la pancarta o incluso buscar una imagen diferente para utilizarla.

   >[!NOTE]
   >
   >Tenga en cuenta que cualquier cambio que realice en los parámetros puede ser anulado por las reglas comerciales. Los parámetros solo funcionan como predeterminados cuando no se crean reglas comerciales que cambiarían los parámetros de otro modo.

   Consulte [Adición de una nueva regla](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7)comercial.

   See [Editing a business rule](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

   **Alternar las opciones de visibilidad de capa**

   La opción Alternar visibilidad de capa solo se aplica si selecciona una plantilla Flash para el letrero.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Alternar visibilidad de capa, opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_togglelayervisibility.png"> </p> </td> 
      <td colname="col2"> <p>Permite activar o desactivar la visibilidad de las distintas capas que componen el archivo de plantilla Flash. </p> <p>Cada vez que se activa o desactiva la visibilidad de una capa, se actualiza la ventana de vista previa para actualizar la visualización. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   (Opcional) Si el recurso digital que desea utilizar para un letrero no está disponible en la carpeta seleccionada, es posible que tenga que cargarlo. Haga clic en **[!UICONTROL Upload]** y, a continuación, seleccione el archivo y las opciones que desee. El archivo se carga en la carpeta seleccionada.

   >[!NOTE]
   >
   >Si desea utilizar la función de carga en el visor de recursos de Scene7, asegúrese de que la cuenta de Scene7 que utiliza ya tiene definida la función &quot;Administrador de la empresa de SPS&quot;.

   Consulte Ajustes [de](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) administración en la Guía del usuario de Scene7 Publishing System.

   **Opciones básicas**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Examinar </p> </td> 
      <td colname="col2"> <p> Permite buscar el archivo que desea cargar, publicar y, a continuación, seleccionar para utilizarlo como letrero. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Sobrescribir </p> </td> 
      <td colname="col2"> <p>Los archivos que cargue reemplazarán los archivos existentes con el mismo nombre de archivo, dentro de la carpeta seleccionada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Preferencia de correo electrónico </p> </td> 
      <td colname="col2"> <p> Le permite elegir la notificación por correo electrónico que recibirá para la carga, o bien puede optar por no recibir notificaciones de nada relacionado con el trabajo de carga. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opciones avanzadas**

   Al cargar archivos de imagen PostScript (EPS) o Illustrator (AI), puede darles formato de varias formas. Puede rasterizar los archivos, convertirlos a FXG para la publicación de plantillas, mantener el fondo transparente, elegir una resolución y elegir un espacio de color.

   Los archivos PSD (Photoshop Document) se utilizan con mayor frecuencia en Dynamic Media Classic para crear plantillas. Al cargar un archivo PSD, puede crear una plantilla de Dynamic Media Classic automáticamente a partir del archivo (seleccione la **[!UICONTROL Create Template]** opción).

   Scene7 Publishing System crea varias imágenes a partir de un archivo PSD con capas si se utiliza el archivo para crear una plantilla; crea una imagen para cada capa.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Nombre del grupo de opciones </p> </th> 
      <th colname="col02" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Opciones de perfil de color </p> </td> 
      <td colname="col02"> <p>Perfil de color </p> </td> 
      <td colname="col2"> <p> Permite elegir entre las siguientes opciones: </p> 
        <ul id="ul_6927BC08CA2647EDB2C85DAD2B82AE31"> 
        <li id="li_CA3F44FF9C0F4CE987DCB0AF9303C2E4"> <span class="uicontrol"> Convertir a SRGB </span> <p>Convierte a SRGB (Standard Red Green Blue). SRGB es el espacio de color recomendado para mostrar imágenes en páginas web. </p> </li> 
        <li id="li_FCCEE6B14CCD4246ADA152932010ABF1"> <span class="uicontrol"> Mantener espacio de color original </span> <p>Conserva el espacio de color original. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opciones de edición de imágenes </p> </td> 
      <td colname="col02"> <p>Crear máscara a partir de ruta de recorte </p> </td> 
      <td colname="col2"> <p>Cree una máscara para la imagen en función de la información de ruta de recorte. Esta opción se aplica a las imágenes creadas con aplicaciones de edición de imágenes en las que se ha creado una ruta de recorte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opciones de PostScript </p> <p>Opciones de Illustrator </p> </td> 
      <td colname="col02"> <p>Procesando </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> La opción Rasterizar </span> convierte los gráficos vectoriales del archivo al formato de mapa de bits. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opciones de Postscript </p> <p>Opciones de Illustrator </p> </td> 
      <td colname="col02"> <p> Resolución </p> </td> 
      <td colname="col2"> <p> Determina la configuración de resolución. Esta configuración determina cuántos píxeles se muestran por pulgada en el archivo. El valor predeterminado es 150. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opciones de PostScript </p> <p>Opciones de Illustrator </p> </td> 
      <td colname="col02"> <p> Espacio de color </p> </td> 
      <td colname="col2"> <p>Permite elegir un espacio de color para el archivo de Illustrator. El espacio de color RGB es preferible para la visualización en línea. </p> <p>Puede elegir entre las siguientes opciones de espacio de color: </p> 
        <ul id="ul_0E83E2762A574480B243F963A7FB2ACD"> 
        <li id="li_B9FEC7D220D04CCABACD30839051DAE4"> <span class="uicontrol"> Detectar automáticamente </span> <p> Conserva el espacio de color del archivo PDF. </p> </li> 
        <li id="li_ED0EB3B12BCF41C7AFC435447010B6FF"> <span class="uicontrol"> Forzar RGB </span> <p> Convierte al espacio de color RGB. </p> </li> 
        <li id="li_3FB5DD8887C540BC97148A4D63B38F72"> <span class="uicontrol"> Forzar CMYK </span> <p> Convierte al espacio de color CMYK. </p> </li> 
        <li id="li_6C018D3A4B254880AD41896E9F4AF3D9"> <span class="uicontrol"> Forzar como escala de grises </span> <p> Convierte al espacio de color Escala de grises. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opciones de PostScript </p> <p>Opciones de Illustrator </p> </td> 
      <td colname="col02"> <p> Mantener fondo transparente </p> </td> 
      <td colname="col2"> <p>Mantiene la transparencia de fondo del archivo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opciones de Photoshop </p> </td> 
      <td colname="col02"> <p> Mantener capas </p> </td> 
      <td colname="col2"> <p>Extrae las capas del PSD, si las hay, en recursos individuales. Las capas de recursos permanecen asociadas al PSD. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opciones de Photoshop </p> </td> 
      <td colname="col02"> <p>Crear plantilla </p> </td> 
      <td colname="col2"> <p> Crea una plantilla a partir de las capas del archivo PSD. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opciones de Photoshop </p> </td> 
      <td colname="col02"> <p> Extraer texto </p> </td> 
      <td colname="col2"> <p> Extrae el texto para que los clientes puedan buscar palabras clave dentro de una pancarta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opciones de Photoshop </p> </td> 
      <td colname="col02"> <p> Ampliar capas </p> </td> 
      <td colname="col2"> <p>Extiende el tamaño de las capas de imagen extraídas al tamaño de la capa de fondo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opciones de Photoshop </p> </td> 
      <td colname="col02"> <p> Nombres de capas </p> </td> 
      <td colname="col2"> <p>Las capas del archivo PSD se cargan como imágenes independientes. Puede seleccionar entre las siguientes opciones para decidir cómo desea asignar un nombre a estas imágenes en Scene7 Publishing System: </p> 
        <ul id="ul_C2A25177A07740CA90B32C638304D39F"> 
        <li id="li_477D5BFF7238454BBF0E04B22DE378F7"> <span class="uicontrol"> Usar nombre de capa del archivo PSD </span> <p>Asigna a las imágenes los nombres de sus capas en el archivo PSD. Por ejemplo, una capa denominada <span class="codeph"> Etiqueta de precio </span> en el archivo PSD original se convierte en una imagen denominada <span class="codeph"> Etiqueta de precio </span>. Sin embargo, si los nombres de capa del archivo PSD son nombres de capa predeterminados de Photoshop (Fondo, Capa 1, Capa 2, etc.), las imágenes recibirán el nombre de sus números de capa en el archivo PSD, no de sus nombres de capa predeterminados. </p> </li> 
        <li id="li_EB4173B884FC41328CFBDE27DA6D43AA"> <span class="uicontrol"> Usar nombre de archivo PSD y número de anexo </span> <p>Asigna a las imágenes los nombres de sus capas en el archivo PSD, sin tener en cuenta los nombres de las capas originales. Las imágenes reciben el nombre del archivo de Photoshop y un número de capa anexado. Por ejemplo, la segunda capa de un archivo llamado Anuncio de <span class="codeph"> primavera.psd </span> se denomina Anuncio de <span class="codeph"> primavera_2 </span> aunque tenga un nombre no predeterminado en Photoshop. </p> </li> 
        <li id="li_10B2D2DE2FD24BD08DB56D1D95ABA53D"> <span class="uicontrol"> Usar nombre de archivo PSD y nombre o número de capa </span> <p>Nombra las imágenes después del archivo PSD seguido del nombre o el número de capa. El número de capa se utiliza si los nombres de capa del archivo PSD son nombres de capa predeterminados de Photoshop. Por ejemplo, una capa denominada <span class="codeph"> Etiqueta de precio </span> en un archivo PSD con el nombre <span class="codeph"> Anuncio primavera </span> se denomina <span class="codeph"> Anuncio primavera_Etiqueta de precio </span>. Una capa con el nombre predeterminado <span class="codeph"> Capa 2 </span> se denomina <span class="codeph"> Anuncio primavera_2 </span>. </p> </li> 
        <li id="li_5E57AC0719D4484B9C9BD14DB42B4455"> <span class="uicontrol"> Creación de una carpeta basada en el nombre de archivo PSD </span> <p>Crea una carpeta para las imágenes de capa utilizando el nombre de archivo del archivo PSD. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opciones de Photoshop </p> </td> 
      <td colname="col02"> <p>Anclaje </p> </td> 
      <td colname="col2"> <p>Especifique cómo se anclan las imágenes en plantillas que se generan a partir de la composición en capas producida a partir del archivo PSD. </p> <p>De forma predeterminada, el anclaje es el centro. Un anclaje central permite que las imágenes de reemplazo ocupen mejor el mismo espacio, independientemente de la proporción de aspecto de la imagen de reemplazo. Las imágenes con un aspecto diferente que reemplazan a esta imagen, al hacer referencia a la plantilla y utilizar la sustitución de parámetros, ocupan efectivamente el mismo espacio. Cambie a una configuración diferente si la aplicación requiere que las imágenes de reemplazo ocupen el espacio asignado en la plantilla. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opciones de PDF </p> </td> 
      <td colname="col02"> <p>Procesando </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> La opción Rasterizar </span> extrae las páginas del archivo PDF y convierte los gráficos vectoriales en imágenes de mapa de bits. 
        <!--Choose this option to create an eCatalog. (This option is thedefault.)--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opciones de PDF </p> </td> 
      <td colname="col02"> <p> Resolución </p> </td> 
      <td colname="col2"> <p>Determina la configuración de resolución. Esta configuración determina cuántos píxeles se muestran por pulgada en el archivo PDF. El valor predeterminado es 150. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opciones de PDF </p> </td> 
      <td colname="col02"> <p> Espacio de color </p> </td> 
      <td colname="col2"> <p>Permite elegir un espacio de color para el archivo PDF. La mayoría de los archivos PDF tienen imágenes en color RGB y CMYK. El espacio de color RGB es preferible para la visualización en línea. </p> <p>Puede elegir entre las siguientes opciones de espacio de color: </p> 
        <ul id="ul_44A8C39DEB21473F9375E3962F14D3C6"> 
        <li id="li_1046FA0017934C5EB7C0100F8F78507D"> <span class="uicontrol"> Detectar automáticamente </span> <p> Conserva el espacio de color del archivo PDF. </p> </li> 
        <li id="li_561CCF705EDD451993D2DA2EB33F05F7"> <span class="uicontrol"> Forzar RGB </span> <p> Convierte al espacio de color RGB. </p> </li> 
        <li id="li_D9E8CF61C40140979484EDEF7DAD2C44"> <span class="uicontrol"> Forzar CMYK </span> <p> Convierte al espacio de color CMYK. </p> </li> 
        <li id="li_F3606B45C0F84BA594263EA12243F67A"> <span class="uicontrol"> Forzar como escala de grises </span> <p> Convierte al espacio de color Escala de grises. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Opciones de PDF </p> </td> 
      <td colname="col02"> <p>Generar catálogo electrónico automáticamente a partir de PDF de varias páginas </p> </td> 
      <td colname="col2"> <p> Crea automáticamente un catálogo electrónico a partir del archivo PDF. El catálogo electrónico recibe el nombre del archivo PDF que ha cargado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Opciones de PDF </p> </td> 
      <td colname="col02"> <p>Extraer palabras clave </p> </td> 
      <td colname="col2"> <p>Extrae palabras del archivo PDF para que el archivo pueda buscarse por palabras clave. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. En el panel derecho, haga clic en la imagen, plantilla o archivo Flash que desee.

   Aparece la ventana [!DNL Pick An Asset] emergente.
1. (Opcional) En la lista desplegable de la ventana [!DNL Pick An Asset] emergente, realice una de las [!DNL Actions] siguientes acciones:

   * Haga clic **[!UICONTROL Move]**. En el cuadro de diálogo [!DNL Select a folder to move to] , seleccione la carpeta a la que desea mover el recurso digital. Haga clic **[!UICONTROL Move]**.

      También puede seleccionar varios recursos digitales que desee mover a otra carpeta.

   * Haga clic **[!UICONTROL Delete]**. En el cuadro de diálogo [!DNL Delete Selected Assets] , haga clic en **[!UICONTROL Delete]**.

      También puede seleccionar varios recursos digitales que desee eliminar de la carpeta.

   * Haga clic **[!UICONTROL Rename]**. En el campo de texto del cuadro de diálogo [!DNL Enter a new name for] , escriba un nombre nuevo para el recurso digital. Haga clic **[!UICONTROL Rename]**.

1. (Opcional) En función del recurso digital que haya seleccionado, en el panel izquierdo de la ventana [!DNL Pick an Asset] emergente, configure las opciones que desee.
1. Haga clic en el recurso para seleccionarlo y utilizarlo como letrero.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de letreros con Adobe Dynamic Media Classic {#task_C3E782477FBF428ABEA220751781ACA9}

Utilícelo [!DNL Edit Banner] para cambiar las propiedades y los parámetros de un letrero que ha agregado con Adobe Dynamic Media Classic.

<!-- 

t_editing_a_banner_using_adobe_scene7.xml

 -->

Si agregó un letrero agregando código HTML, edite el letrero mediante la búsqueda o comercialización del sitio.

Consulte también [Edición de letreros](../c-about-design-menu/c-about-banners.md#task_D4081083BE7B40F5A003D1A2F1435AEA).

**Para editar una pancarta con Adobe Dynamic Media Classic**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. En la [!DNL Banners] página, haga clic ![](assets/icon_edit_16.gif) sobre una miniatura de pancarta que tenga un icono S7 en la esquina inferior izquierda de la ventana de la pancarta.
1. En la [!DNL Change Parameter] página, configure las opciones que desee.
1. Cuando haya terminado de editar la pancarta, haga clic en **[!UICONTROL Save]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de pancartas {#task_32F3BADC481E4E8984B2AA04B96052EB}

Puede eliminar las pancartas escalonadas que ya no necesite o que desee usar de una en una o como grupo.

<!-- 

t_deleting_banners.xml

 -->

**Para eliminar pancartas**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Opcional) Realice una o varias de las acciones siguientes:

   * En la [!DNL Banners] página, seleccione el tipo de pancarta que desee buscar en la lista **[!UICONTROL Find banner of type]** desplegable. Si lo desea, especifique un nombre de etiqueta en el campo de **[!UICONTROL with tag]** texto o un nombre de tipo de pancarta en el campo de **[!UICONTROL with name]** texto. Haga clic **[!UICONTROL Find.]**

   * En la lista **[!UICONTROL Sort]** desplegable, seleccione cómo desea ordenar la lista de letreros.
   * En la lista **[!UICONTROL Show]** desplegable, seleccione el número de pancartas que desea cargar en la página actual que está viendo.

1. Realice uno de los siguientes pasos:

   * En la esquina superior izquierda de cualquier cuadro de pancarta, haga clic en la casilla de verificación de cada pancarta que desee eliminar.
   * En la barra superior de la [!DNL Banners] página, marque **[!UICONTROL Select all]** para seleccionar todos los letreros que se cargan en la página que se muestra actualmente.

1. En la lista **[!UICONTROL Bulk Actions]** desplegable, haga clic en **[!UICONTROL Delete]**.
1. En el cuadro de diálogo [!DNL Confirmation Action] , haga clic en **[!UICONTROL OK]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Vista previa de pancartas {#task_6AB1F81A984A4DC2ACACD1FE030545E2}

Puede examinar las pancartas agregadas a la [!DNL Banners] página para ver su tamaño completo. No se muestra ninguna CSS de la plantilla que afecte a la pancarta.

<!-- 

t_previewing_banners.xml

 -->

**Para obtener una vista previa de los letreros**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Opcional) Realice una o varias de las acciones siguientes:

   * En la [!DNL Banners] página, seleccione el tipo de pancarta que desee buscar en la lista **[!UICONTROL Find banner of type]** desplegable. Si lo desea, especifique un nombre de etiqueta en el campo de **[!UICONTROL with tag]** texto o un nombre de tipo de pancarta en el campo de **[!UICONTROL with name]** texto. Haga clic **[!UICONTROL Find.]**

   * En la lista **[!UICONTROL Sort]** desplegable, seleccione cómo desea ordenar la lista de letreros.
   * En la lista **[!UICONTROL Show]** desplegable, seleccione el número de pancartas que desea cargar en la página actual que está viendo.

1. En la página, haga clic en una miniatura de la pancarta para ver su tamaño completo. [!DNL Banners]
1. Realice uno de los siguientes pasos:

   * En el cuadro de diálogo de vista previa de letreros, haga clic en la flecha izquierda o derecha para navegar y ver los letreros de tamaño completo que ha agregado.
   * Haga clic en el botón Cerrar para cerrar el cuadro de diálogo de vista previa de letreros y volver a la [!DNL Banners] página.

## Inserción de letreros activos {#task_161F4FEC8362474296A566E64BF05B97}

Puede insertar una o varias pancartas seleccionadas en directo en el sitio web.

<!-- 

t_pushing_banners_live.xml

 -->

O bien, si lo prefiere, puede insertar todos los cambios en directo en cualquier pancarta utilizando la **[!UICONTROL Push Live]** opción situada cerca de la parte inferior de la [!DNL Banners] página.

Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

**Para insertar pancartas en directo**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Opcional) Realice una o varias de las acciones siguientes:

   * En la [!DNL Banners] página, seleccione el tipo de pancarta que desee buscar en la lista **[!UICONTROL Find banner of type]** desplegable. Si lo desea, especifique un nombre de etiqueta en el campo de **[!UICONTROL with tag]** texto o un nombre de tipo de pancarta en el campo de **[!UICONTROL with name]** texto. Haga clic **[!UICONTROL Find]**.

   * En la lista **[!UICONTROL Sort]** desplegable, seleccione cómo desea ordenar la lista de letreros.
   * En la lista **[!UICONTROL Show]** desplegable, seleccione el número de pancartas que desea cargar en la página actual que está viendo.

1. Realice uno de los siguientes pasos:

   * En la esquina superior izquierda de cualquier cuadro de pancarta, haga clic en la casilla de verificación de cada pancarta que desee eliminar.
   * En la barra superior de la [!DNL Banner] página, marque **[!UICONTROL Select all]** para seleccionar todos los letreros que se cargan en la página que se muestra actualmente.

1. En la lista **[!UICONTROL Bulk Actions]** desplegable, haga clic en **[!UICONTROL Push live]**.
1. En el cuadro de diálogo [!DNL Confirmation Action] , haga clic en **[!UICONTROL OK]**.
1. (Opcional) En la [!DNL Banners] página, haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

   Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.
