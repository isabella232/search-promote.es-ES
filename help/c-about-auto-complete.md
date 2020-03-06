---
description: Puede configurar varias áreas de Completar automáticamente para controlar la generación del formulario de búsqueda habilitado para completar automáticamente y el archivo autocomplete_data.js, que se incluye como parte del formulario de búsqueda habilitado para completar automáticamente.
seo-description: Puede configurar varias áreas de Completar automáticamente para controlar la generación del formulario de búsqueda habilitado para completar automáticamente y el archivo autocomplete_data.js, que se incluye como parte del formulario de búsqueda habilitado para completar automáticamente.
seo-title: Acerca de la finalización automática
solution: Target
subtopic: Auto-Complete
title: Acerca de la finalización automática
topic: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
translation-type: tm+mt
source-git-commit: 439100ab96f4b597c55b1c1ae38a5778c208e896

---


# Acerca de la finalización automática{#about-auto-complete}

Puede configurar varias áreas de Completar automáticamente para controlar la generación del formulario de búsqueda habilitado para completar automáticamente y el archivo autocomplete_data.js, que se incluye como parte del formulario de búsqueda habilitado para completar automáticamente.

## Acerca de la finalización automática {#concept_093A9CD754864BA79B456FE4BEB64578}

El archivo [!DNL autocomplete_data.js] se vuelve a generar y se publica en la red de contenido de búsqueda cada vez que se guardan cambios en la página Configuración de finalización automática.

## Configuración del autocompletado {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

Puede configurar y configurar las opciones que controlan la generación del formulario de búsqueda habilitado para completar automáticamente y el archivo.

<!-- 

t_configuring_auto-complete.xml

 -->

Después de configurar la función de autocompletar, puede ver la fuente HTML resultante para su revisión. El código fuente HTML es lo que copia y pega en las páginas del sitio web.

Consulte [Vista previa del formulario de búsqueda tal y como aparecería en su...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

Consulte [Configuración de la lista](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)de palabras de finalización automática.

Consulte [Configuración de CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)de finalización automática.

**Para configurar la finalización automática**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Setup]**.
1. En la [!DNL Auto-Complete Setup] página, configure las opciones que desee.

   Consulte también [Vista previa del formulario de búsqueda tal y como aparecería en su...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Sugerencias máximas </p> </td> 
      <td colname="col2"> <p>Especifica el número máximo de elementos que se mostrarán en la lista de sugerencias de autocompletar. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caracteres de entrada mínimos </p> </td> 
      <td colname="col2"> <p>Especifica el número de caracteres que un cliente debe escribir en el formulario de búsqueda de autocompletar antes de que muestre las sugerencias. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número máximo de entradas de caché </p> </td> 
      <td colname="col2"> <p>Especifica el número máximo de sugerencias de autocompletar solicitadas anteriormente para almacenar en caché en el explorador del cliente. Por lo general, debe dejar esta configuración en el valor predeterminado de 1000. </p> <p>Aunque puede deshabilitar completamente el almacenamiento en caché del navegador estableciendo esta opción en 0, no se recomienda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre del formulario </p> </td> 
      <td colname="col2"> <p>Especifica el atributo "name" de la etiqueta "form" del formulario de búsqueda habilitada para autocompletar. Por ejemplo, </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com" target="_blank"&gt; </span> </p> <p>donde <span class="filepath"> SiteSearch </span> es el atributo de nombre de la etiqueta de formulario. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID de etiqueta de div </p> </td> 
      <td colname="col2"> <p>Especifica el atributo de ID de la etiqueta "div" del formulario de búsqueda habilitada para completar automáticamente. Por ejemplo, </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>donde <span class="filepath"> autocompletar </span> es el atributo de la etiqueta div. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID de etiqueta de entrada </p> </td> 
      <td colname="col2"> <p>Especifica el atributo de ID de la etiqueta "input" del formulario de búsqueda habilitada para autocompletar. Por ejemplo, </p> <p> <span class="filepath"> &lt;input type="text" id="q" name="q" /&gt; </span> </p> <p>donde <span class="filepath"> q </span> es el atributo de identificación de la etiqueta de entrada. </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>Mostrar sombra </p> </td>
      <td colname="col2"> <p>Agrega una sombra paralela estética a la lista de sugerencias de autocompletar. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Coincidir solo al principio de la frase </p> </td>
      <td colname="col2"> <p>Solo sugerir resultados que coincidan con el principio del texto de entrada. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Conjunto de caracteres UTF-8 compatible </p> </td>
      <td colname="col2"> <p>Administre correctamente los caracteres que no sean ASCII en términos. </p> </td>
      </tr>
    </tbody> 
   </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuración de la lista de palabras de finalización automática {#task_1F8E0F346263443383F8CFD2C7AB35D4}

Configure la lista de palabras y frases que Autocompletar muestra a un cliente como sugerencias.

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

Consulte [Configuración de la finalización](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)automática.

Consulte [Configuración de CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)de finalización automática.

**Para configurar la lista de palabras de finalización automática**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Word List]**.
1. En la [!DNL Auto-Complete Word List] página, configure las opciones que desee.

   Consulte [Vista previa del formulario de búsqueda tal y como aparecería en su...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Período de búsquedas populares </p> </td> 
      <td colname="col2"> <p> Controla el período de tiempo para la inclusión de palabras y frases de las búsquedas recientes de un cliente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Número máximo de búsquedas </p> </td> 
      <td colname="col2"> <p>Controla el número máximo de palabras y frases buscadas para incluir en la lista de palabras de compleción automática. Se incluyen las palabras y frases principales, que también son las más populares. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre del campo </p> </td> 
      <td colname="col2"> <p>Cada nombre de campo define el nombre de un campo para el que se incluyen valores indexados. Utilice + y - para agregar o quitar nombres de campo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Recuento de valores máximo </p> </td> 
      <td colname="col2"> <p>Define el número máximo de valores de campo permitidos para el nombre de campo seleccionado. Se incluyen los valores principales, que también son los más referenciados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Agregue estas palabras y frases </p> </td> 
      <td colname="col2"> <p> La lista de palabras de compleción automática se rellena con las palabras y frases que aparecen en esta área. </p> <p> Haga clic en <span class="uicontrol"> Editar </span> para ver la lista o para agregar palabras y frases a la lista. Cuando termine, haga clic en <span class="uicontrol"> Guardar cambios </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Eliminar estas palabras y frases </p> </td> 
      <td colname="col2"> <p> Las entradas de esta área no se muestran en la lista de palabras de compleción automática. </p> <p> Haga clic en <span class="uicontrol"> Editar </span> para ver la lista o para agregar palabras y frases a la lista. Cuando termine, haga clic en <span class="uicontrol"> Guardar cambios </span>. </p> <p> En esta lista se permiten expresiones regulares. Para especificar una expresión regular en esta lista, inicie la línea con 
        <userinput>
          regexp 
        </userinput> seguido de un solo espacio, seguido de la expresión regular. Se eliminan todas las líneas de la lista de palabras que coincidan con la expresión regular. </p> <p> <b>Importante</b>: Solo debe utilizar expresiones regulares si ya ha trabajado con ellas en otras aplicaciones. </p> <p>Consulte <a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expresiones regulares </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Omitir caso </p> </td> 
      <td colname="col2"> <p>Se eliminan las entradas duplicadas en la lista de palabras de autocompletar que solo difieren por letras mayúsculas y minúsculas; todas las entradas de la lista de palabras están obligadas a minúsculas. </p> <p>Si desea que las sugerencias de Autocompletar aparezcan "primera letra en mayúsculas" o "todas mayúsculas", agregue la variable 
        <userinput>
          text-transform : capitalizar; 
        </userinput> o 
        <userinput>
          text-transform : mayúscula; 
        </userinput> Propiedades de texto CSS para el contenido CSS de finalización automática, en estilos "/* para el elemento de resultado */". </p> <p>Consulte <a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> Configuración de CSS de finalización automática </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Actualización de reíndice </p> </td> 
      <td colname="col2"> <p>La lista de palabras de compleción automática se regenera automáticamente después de cada reindexación de cuenta correcta. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.
   * Haga clic en **[!UICONTROL Preview Word List]** para guardar los cambios realizados y, a continuación, abra [!DNL Auto-Complete Word List Preview] la página donde podrá revisar la lista de sugerencias de autocompletar. Utilice las opciones de navegación cercanas a la parte superior de la página para revisar y refinar la lista mostrada. Cuando haya terminado, haga clic en **[!UICONTROL Close]** para volver a la [!DNL Auto-Complete Word List] página.

      Consulte [Uso de la opción](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuración de la CSS de finalización automática {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

Utilice CSS de finalización automática para configurar la hoja de estilo en cascada de finalización automática que desea utilizar.

<!-- 

t_configuring_auto-complete_css.xml

 -->

La CSS de finalización automática controla el contenido de [!DNL autocomplete_styles.css], que se incluye como parte del formulario de búsqueda habilitado para completar automáticamente. El CSS que especifique aquí controla la presentación visual de la lista de sugerencias de autocompletar. Para ver un ejemplo de las ideas de presentación visual que son posibles, consulte lo siguiente:

[https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html).

[Configuración de la lista](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)de palabras de finalización automática.

[Configuración del autocompletado](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Cuando haya terminado de configurar la CSS de finalización automática, puede obtener una vista previa del formulario de búsqueda para ver si la CSS especificada es aceptable en apariencia y presentación.

Consulte [Vista previa del formulario de búsqueda tal y como aparecería en su...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

**Importante**: Para aplicar la CSS personalizada de finalización automática, debe eliminar las etiquetas de comentarios de la segunda línea que aparece en el código HTML. A continuación, mueva la misma línea a dentro de la sección del encabezado de la página que contiene el formulario de búsqueda.

Consulte [Copia del código HTML del formulario de búsqueda en el...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**Para configurar CSS de finalización automática**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete CSS]**.
1. En el campo de [!DNL Auto-Complete CSS] texto, pegue o escriba la información de la hoja de estilo en cascada que desea asociar con la lista de sugerencias de autocompletar.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Vista preliminar del formulario de búsqueda tal como aparecería en el sitio web {#task_437B35EFA5424603A08AF8E79E6B4714}

En función de la configuración de Autocompletar y Autocompletar CSS, puede obtener una vista previa del aspecto del formulario de búsqueda si desea agregar el código HTML a su sitio web.

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

Consulte [Configuración de la finalización](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)automática.

Consulte [Configuración de CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)de finalización automática.

Consulte [Copia del código HTML del formulario de búsqueda en el...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Consulte [Uso de colecciones en formularios](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)de búsqueda.

Consulte [Uso de marcos con formularios](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consulte [Ejemplo de formulario](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)de búsqueda avanzada.

Consulte Código [HTML de formulario de búsqueda](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)avanzada.

Consulte Código [](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)de plantilla de formulario de búsqueda avanzada.

**Para obtener una vista previa del formulario de búsqueda tal como aparecería en el sitio web**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Search Form]**.
1. (Opcional) Haga clic en **[!UICONTROL HTML code]** para ver el HTML que copió y pegó en las páginas del sitio web.

## Copia del código HTML del formulario de búsqueda en las páginas del sitio web {#task_A3A01EA800F24C0AA33902387E0362C7}

En función de la configuración de Autocompletar y Autocompletar CSS, puede obtener una vista previa del aspecto del formulario de búsqueda si desea agregar el código HTML a su sitio web.

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

Consulte [Configuración de la finalización](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)automática.

Consulte [Configuración de CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)de finalización automática.

Consulte [Copia del código HTML del formulario de búsqueda en el...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Consulte [Uso de colecciones en formularios](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)de búsqueda.

Consulte [Uso de marcos con formularios](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consulte [Ejemplo de formulario](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)de búsqueda avanzada.

Consulte Código [HTML de formulario de búsqueda](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)avanzada.

Consulte Código [](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)de plantilla de formulario de búsqueda avanzada.

**Para copiar el código HTML del formulario de búsqueda en las páginas del sitio web**

1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**.

   >[!NOTE]
   >
   >No cambie el `form name=` valor en el origen del formulario.

1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Si ha configurado la función de autocompletar CSS y desea que se apliquen los estilos al formulario de búsqueda, elimine las etiquetas de comentarios de la segunda línea que aparece en el código HTML. A continuación, mueva la misma línea hacia dentro de la sección del encabezado de la página que contiene el formulario de búsqueda.
   * Para obtener el máximo rendimiento, mueva las etiquetas que aparecen en la parte inferior del código HTML y colóquelas en la parte inferior de la sección body de cada página que contenga el formulario de búsqueda.

1. Copie el código y péguelo en las páginas web del sitio web donde desee que aparezca el formulario de búsqueda.
