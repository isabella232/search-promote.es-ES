---
description: Utilice el menú Opciones de cuenta para actualizar la configuración de la cuenta, establecer las preferencias de comercialización o eliminar su propia cuenta de Search&Promote.
solution: Target
subtopic: Account Options
title: Acerca del menú Opciones de cuenta
topic: Configuración,Búsqueda de sitios y comercialización
uuid: 0f830033-de9e-4197-8d76-906c818662eb
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 2%

---


# Acerca del menú Opciones de cuenta{#about-the-account-options-menu}

Utilice el menú Opciones de la cuenta para actualizar la configuración de la cuenta, establecer las preferencias de comercialización o eliminar su propia cuenta de Search&amp;Promote.

## Configuración de la cuenta {#task_80A38D0C8E4F453395BD67B81E4B45D9}

Administre la configuración de la cuenta, como el nombre y la dirección del sitio web, la zona horaria y mucho más. O bien, vea su número de cuenta.

**Para configurar los ajustes de la cuenta**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Account Settings]**.
1. En la página [!DNL Account Settings], configure las opciones que desee.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nombre del sitio web </p> </td> 
      <td colname="col2"> <p>Requerido. </p> <p>Un nombre corto que se utiliza para describir su sitio web o cuenta. Esta opción resulta útil si tiene varios sitios web. </p> <p> <p>Nota:  Debe ponerse en contacto con la asistencia técnica para seleccionar uno o varios nombres que desee utilizar. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dirección del sitio web </p> </td> 
      <td colname="col2"> <p>Requerido. </p> <p>La dirección URL del sitio web. La dirección especificada aquí se usa como punto de entrada del sitio web principal. </p> <p>Consulte también <a href="../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45" type="task" format="dita" scope="local"> Adición de varios puntos de entrada de URL que desee indexar </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zona horaria (para informes y programación) </p> </td> 
      <td colname="col2"> <p>Zona horaria que se utiliza para las operaciones de publicación e informes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Validación de atributos de etiqueta de plantilla al guardar </p> </td> 
      <td colname="col2"> <p>Valida todos los atributos en <span class="codeph"> &lt;guided-*&gt; </span> y <span class="codeph"> &lt;search-*&gt; </span> al guardar una plantilla en el Editor de plantillas organizadas. </p> <p>Consulte <a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local"> Edición de una presentación o de una plantilla de transporte </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Validación de referencias de plantilla a objetos GS al guardar </p> </td> 
      <td colname="col2"> <p> Comprueba la existencia de objetos de Búsqueda guiada, como menús, facetas, rutas de exploración, variables personalizadas y plantillas, a los que se hace referencia en las etiquetas <span class="codeph"> &lt;guided-*&gt; </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aplicar una comprobación estricta de sintaxis de plantilla </p> </td> 
      <td colname="col2"> <p>Hace que el validador de plantillas sea más estricto y permite comprobar elementos como comillas desequilibradas y símbolos &lt;&gt;. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de cuenta </p> </td> 
      <td colname="col2"> <p>No se puede editar el número de cuenta. Solo se muestra. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Changes]**.

## Configuración de la integración con Adobe CQ5 {#task_EA2FC2C24960498DAE01A1AB769D2F14}

Puede configurar la integración de la búsqueda/comercialización del sitio con Adobe CQ5.

**Para configurar la integración con Adobe CQ5**

1. Obtenga su ID de miembro e ID de cuenta haciendo lo siguiente:

   * Inicie sesión en su cuenta de búsqueda/comercialización del sitio.
   * En la ruta URL, copie el ID de miembro y el ID de cuenta.

      Por ejemplo, si la ruta URL a su cuenta fuera `https://searchandpromote.mycompany.com/px/home/?sp_id=00123a4b-sp1234a5b6`, el ID de miembro sería `00123a4b` y el ID de cuenta sería `sp1234a5b6`.

1. En Adobe CQ5, utilice la pestaña Cloud Services para crear la configuración de comercialización/búsqueda del sitio.

   Utilice el ID de miembro y el ID de cuenta copiados para las configuraciones correspondientes.

## Configuración de las preferencias de comercialización {#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A}

Administre las preferencias de comercialización, como el generador de reglas predeterminado y el término de búsqueda predeterminado.

**Para configurar las preferencias de comercialización**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Merchandising Preferences]**.
1. En la página [!DNL Merchandising Preferences], configure las opciones que desee.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Umbral dominante del grupo de déclencheur </p> </td> 
      <td colname="col2"> <p> El porcentaje de umbral que se aplicará a los déclencheur basados en resultados "dominantes de grupo" que especifican "usar valor predeterminado de cuenta". </p> <p>Cambiar esta configuración puede afectar inmediatamente a las búsquedas en directo, por lo que debe utilizarse con precaución. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Definición de grupo </p> </td> 
      <td colname="col2"> <p>Número de resultados en un grupo para la consola de comercialización. El máximo es de 50.000. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Campo "ID de documento de comercialización" (MDI) </p> </td> 
      <td colname="col2"> <p> El campo que especifique debe "unificar" los resultados de búsqueda que desea manipular mediante déclencheur y acciones basados en resultados de "resultado único". </p> <p>El uso del campo de URL predefinido funciona en algunos casos, pero no se recomienda. Un meta campo definido por el usuario con un ID único para cada página (como SKU o product_id por ejemplo) sería mucho más eficiente que el uso del campo URL . Al especificar "ninguno", se deshabilitan los déclencheur y las acciones basados en resultados de "resultado único" en el administrador de reglas. Si se cambia esta opción, solo se aplicará a las reglas guardadas a partir de ahora; las reglas existentes siguen utilizando el MDI con el que se guardaron originalmente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Término de búsqueda VRB predeterminado (Generador de reglas visuales) </p> </td> 
      <td colname="col2"> <p> Le permite personalizar el término de búsqueda inicial que se usa en el Generador de reglas visuales. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Búsqueda predeterminada de VRB </p> </td> 
      <td colname="col2"> <p>Esta configuración le permite establecer la búsqueda predeterminada seleccionada inicialmente en el Generador de reglas visuales. </p> <p> Esta configuración solo es relevante para la implementación con varias búsquedas. El VRB permite seleccionar la búsqueda del déclencheur o la acción a la que se aplica el grupo definido. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tiempo de espera de VRB/Simulador </p> </td> 
      <td colname="col2"> <p>VRB y el simulador envían búsquedas a través de un servidor proxy que es más lento que la búsqueda de producción. En determinadas circunstancias, como la carga lenta de recursos, el VRB o el simulador pueden agotar el tiempo de espera. Puede aumentar o disminuir el número de segundos que la interfaz de usuario debe esperar antes de que se detenga. Rara vez es necesario aumentar esta configuración desde el valor predeterminado de 60. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Changes]**.

## Configuración del acceso a su cuenta de Adobe Dynamic Media Classic {#task_CEFF88C2033D41D0B2FE86C435EDAC6D}

Vincule la cuenta de búsqueda/comercialización del sitio a Dynamic Media Classic de Adobe para poder agregar fácilmente anuncios de banners al sitio web mediante los recursos digitales cargados desde Adobe Scene7.

Consulte [Acerca de los titulares](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA).

Consulte [Adición de un banner con Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

**Para configurar el acceso a su cuenta de Adobe de Dynamic Media Classic**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Scene7 Configuration]**.
1. En la página [!DNL Scene7 Configuration], configure las opciones que desee.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Región </p> </td> 
      <td colname="col2"> <p>Requerido. Identifica la región del mundo en la que su cuenta de Dynamic Media Classic accede a los distintos servidores de Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Empresa predeterminada </p> </td> 
      <td colname="col2"> <p>Identifica el nombre de la empresa asociada a su cuenta de Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Correo electrónico </p> </td> 
      <td colname="col2"> <p>Requerido. Identifica la dirección de correo electrónico que se utiliza para el inicio de sesión y las comunicaciones de Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Contraseña </p> </td> 
      <td colname="col2"> <p>Requerido. La contraseña de inicio de sesión de Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Habilitado </p> </td> 
      <td colname="col2"> <p>Habilita todos los controles de Dynamic Media Classic dentro de la búsqueda/comercialización del sitio. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Prueba </p> </td> 
      <td colname="col2"> <p>Comprueba que el nombre de región, la dirección de correo electrónico y los detalles de contraseña de Dynamic Media Classic sean correctos. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Haga clic en **[!UICONTROL Test]** para comprobar que el nombre de su región de Dynamic Media Classic, la dirección de correo electrónico y los detalles de contraseña son correctos.
1. Haga clic **[!UICONTROL Save Changes]**.

## Configuración del redirector de Adobe Analytics {#task_2C9DE333FD7246E4A460FC0F55204160}

Si utiliza [!DNL Adobe Analytics] para rastrear visitantes del sitio, puede utilizar [!DNL Adobe Analytics Redirector] en la búsqueda/comercialización del sitio para rastrear todas las redirecciones HTTP con [!DNL Adobe Analytics].

**Para configurar el redirector de Adobe Analytics**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Adobe Analytics Redirector]**.
1. En la página [!DNL Adobe Analytics Redirector], configure las opciones que desee.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Activar la función de redirector de Adobe Analytics </p> </td> 
      <td colname="col2"> <p>Activa el seguimiento de redirecciones HTTP con Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Servidor de seguimiento </p> </td> 
      <td colname="col2"> <p> Identifica el nombre del servidor de seguimiento de Adobe Analytics. </p> <p>Para averiguar el nombre del servidor de seguimiento, </p> <p> 
      <ol id="ol_D17B77E81F8D40D0948415CD60839BE3"> 
      <li id="li_BE58DBA104D44F0DB6C64AD3F12CEA97"> En Adobe Analytics, haga clic en <span class="uicontrol"> Administración </span> &gt; <span class="uicontrol"> Admin Console </span> &gt; <span class="uicontrol"> Administrador de códigos </span>. </li> 
      <li id="li_67A93D17C3A14874928C6DC4FF2D4784"> En el cuadro de grupo <span class="wintitle"> Opciones </span> , seleccione un grupo de informes en la lista desplegable correspondiente. </li> 
      <li id="li_5AAB004AC58441DBB0F813BDE30EFFD4"> Haga clic en <span class="uicontrol">Generar código </span>. </li> 
      <li id="li_E80368993F4D4DD69E37509FF4348B36"> En la página <span class="wintitle"> Administrador de códigos </span> , haga clic en la pestaña <span class="uicontrol"> Archivo Core Javascript </span>. </li> 
      <li id="li_991BDCDDA41A445F85CEEAAE9A46A304"> En la sección <span class="wintitle"> Config </span>, busque la línea que se parece a la siguiente: <p> <code> s.trackingServer="yourcompany.122.2o7.net" </code> </p> <p>El nombre del servidor de seguimiento, en este caso, es <span class="codeph"> "yourcompany.122.2o7.net" </span> </p> </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID del grupo de informes </p> </td> 
      <td colname="col2"> <p> Identifica el ID del grupo de informes. </p> <p>Para averiguar la ID del grupo de informes, </p> <p> 
      <ol id="ol_4FD7B2459358486DBDB130426131D16A"> 
      <li id="li_9AF624CEB128453C808892EEE385D5D1"> En Adobe Analytics, haga clic en <span class="uicontrol"> Administración </span> &gt; <span class="uicontrol"> Admin Console </span> &gt; <span class="uicontrol"> Grupos de informes </span>. </li> 
      <li id="li_AAC47EAA04144A67BDCB5C7B8D8098E9"> Busque la columna <span class="wintitle"> Report Suite Id </span> en la tabla para encontrar el ID. </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetros personalizados </p> </td> 
      <td colname="col2"> <p>Permite agregar parámetros personalizados a la dirección URL de redireccionamiento de Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Defina las mayúsculas y minúsculas de todos los valores personalizados como </p> </td> 
      <td colname="col2"> <p>Permite estandarizar la carcasa que se utiliza para cualquier valor de parámetro personalizado que haya especificado anteriormente. Adobe Analytics distingue entre mayúsculas y minúsculas, por lo que existe una razón para unificar las mayúsculas y minúsculas de los valores. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstruya el índice del sitio provisional si desea obtener una vista previa de los resultados.

   Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) En la página [!DNL Adobe Analytics Redirector], realice una de las acciones siguientes:

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuración de archivos raíz {#task_5F175C8743FB49A2A003813CBF7C56BF}

Administre los archivos raíz en la carpeta raíz del sitio web.

**Para configurar archivos raíz**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Root Files]**.
1. En la página [!DNL Root Files], busque los archivos raíz que desee cargar.

   <table> 
    <thead> 
    <tr> 
      <th colname="col1" class="entry"> <p>Archivo raíz </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
      <td colname="col1"> <p>favicon.ico </p> </td> 
      <td colname="col2"> <p> Icono del sitio. Normalmente se muestra en la barra de direcciones del explorador del cliente. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>robots.txt </p> </td> 
      <td colname="col2"> <p>Permite o no permite que los bots accedan a ciertas partes del sitio web. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>sitemap.xml </p> </td> 
      <td colname="col2"> <p>El archivo XML con una lista de todas las páginas disponibles en el sitio web. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>crossdomain.xml </p> </td> 
      <td colname="col2"> <p>Permite o no permite que el Flash Player acceda a archivos entre dominios. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Reconstruya el índice del sitio provisional si desea obtener una vista previa de los resultados.

   Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) En la página [!DNL Root Files], realice una de las acciones siguientes:

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Transferencia de la propiedad de la cuenta a otro usuario de la cuenta {#task_47E3C66CC6374274830DA10171E0CF17}

Como propietario de la cuenta, si tiene intención de cancelar su inicio de sesión, primero debe transferir la propiedad a otro usuario de la cuenta activa. Puede utilizar [!DNL Transfer Ownership] para realizar esta tarea.

Puede transferir la propiedad a cualquier usuario de cuenta de comercialización o búsqueda del sitio existente.

Una vez finalizada la transferencia de propiedad, el nuevo propietario de la cuenta recibe una notificación por correo electrónico y el anterior propietario queda exento de las restricciones y responsabilidades de ese puesto.

Solo puede haber un propietario por cuenta. Si transfiere su propiedad a otro usuario, ya no tendrá privilegios de propiedad.

Consulte [Cancelación del inicio de sesión](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

Consulte [Eliminación de una cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32).

Consulte [Eliminación de una cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F).

**Para transferir la propiedad de la cuenta a otra cuenta**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Transfer Ownership]**.
1. En la página [!DNL Transfer Ownership] , haga clic en el usuario al que desee hacerse cargo de su cuenta.
1. Haga clic **[!UICONTROL Transfer]**.

## Eliminación de una cuenta {#task_975178D5B9444BF8B52D72B897A49C32}

Puede eliminar una cuenta por completo de la búsqueda o comercialización del sitio. Al hacerlo, usted y los demás usuarios de su cuenta dejarán de tener acceso a ella.

Cuando elimina la cuenta, ya no se puede usar para indexar o buscar en el sitio activo. Además,

Para permitir que otros usuarios sigan usando esta cuenta, puede transferir la propiedad a un usuario diferente y luego eliminarse a sí mismo como usuario de la cuenta.

Consulte [Transferencia de la propiedad de la cuenta a otro usuario de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17).

Si tiene otras cuentas, después de quitar la cuenta actual, se le dirigirá a la primera cuenta que aparezca en su inicio de sesión.

Consulte [Eliminación de una cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F).

Consulte [Cancelación del inicio de sesión](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

**Para quitar una cuenta**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Remove Account]**.
1. (Opcional) En el campo [!DNL Reason for Removal] introduzca un motivo para la eliminación de la cuenta.
1. Haga clic **[!UICONTROL Remove Account]**.

## Eliminarse de una cuenta {#task_C56F5AB87B664BAAAC2FD2F15003E73F}

Puede quitarse de una cuenta de búsqueda/comercialización del sitio.

Cuando se elimina de una cuenta, ya no se puede acceder a ella y no se puede editar la configuración de la cuenta ni indexar el sitio con ella.

Para recuperar el acceso a la cuenta, pida a un usuario de la cuenta actual que lo restablezca.

Consulte [Cancelación del inicio de sesión](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

Consulte [Eliminación de una cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32).

Consulte [Transferencia de la propiedad de la cuenta a otro usuario de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17).

**Para quitarse de una cuenta**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Remove Yourself]**.
1. Haga clic **[!UICONTROL Remove Yourself]**.
