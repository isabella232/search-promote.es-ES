---
description: Puede configurar varias áreas de Autocompletar para controlar la generación del formulario de búsqueda habilitado para autocompletar y el archivo autocomplete_data.js, que se incluye como parte del formulario de búsqueda habilitado para autocompletar.
solution: Target
subtopic: Auto-Complete
title: Acerca de la finalización automática
topic-legacy: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
exl-id: a1d08c0a-6c68-4da2-88d2-fe953d333536
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 1%

---

# Acerca del autocompletado{#about-auto-complete}

Puede configurar varias áreas de Autocompletar para controlar la generación del formulario de búsqueda habilitado para autocompletar y el archivo autocomplete_data.js, que se incluye como parte del formulario de búsqueda habilitado para autocompletar.

## Acerca de la finalización automática {#concept_093A9CD754864BA79B456FE4BEB64578}

El archivo [!DNL autocomplete_data.js] se regenera y publica en la red de contenido de búsqueda cada vez que se guardan cambios en la página Configuración de autocompletar.

## Configuración del autocompletado {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

Puede configurar las opciones que controlan la generación del formulario de búsqueda habilitado para autocompletar y el archivo.

<!-- 

t_configuring_auto-complete.xml

 -->

Después de configurar la autocompleción, puede ver la fuente HTML resultante para su revisión. La fuente HTML es lo que copia y pega en las páginas del sitio web.

Consulte [Vista previa del formulario de búsqueda tal como aparecería en su...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

Consulte [Configuración de la lista de palabras de finalización automática](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4).

Consulte [Configuración de CSS de autocompletar](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

**Para configurar la finalización automática**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Setup]**.
1. En la página [!DNL Auto-Complete Setup], configure las opciones que desee.

   Consulte también [Vista previa del formulario de búsqueda tal como aparecería en su...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

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
      <td colname="col1"> <p>Máximo de entradas de caché </p> </td> 
      <td colname="col2"> <p>Especifica el número máximo de sugerencias de autocompletado solicitadas anteriormente para almacenar en caché en el explorador del cliente. Por lo general, debe dejar esta configuración en el valor predeterminado de 1000. </p> <p>Aunque puede deshabilitar completamente el almacenamiento en caché del explorador estableciendo esta opción en 0, no se recomienda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre del formulario </p> </td> 
      <td colname="col2"> <p>Especifica el atributo "name" de la etiqueta "form" del formulario de búsqueda habilitado para autocompletar. Por ejemplo, </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com" target="_blank"&gt; </span> </p> <p>donde <span class="filepath"> SiteSearch </span> es el atributo name de la etiqueta form. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID de etiqueta div </p> </td> 
      <td colname="col2"> <p>Especifica el atributo de ID de la etiqueta "div" del formulario de búsqueda habilitada para autocompletar. Por ejemplo, </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>donde <span class="filepath"> autocomplete </span> es el atributo de la etiqueta div. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID de etiqueta de entrada </p> </td> 
      <td colname="col2"> <p>Especifica el atributo de ID de la etiqueta "input" del formulario de búsqueda habilitada para autocompletar. Por ejemplo, </p> <p> <span class="filepath"> &lt;input type="text" id="q" name="q" /&gt; </span> </p> <p>donde <span class="filepath"> q </span> es el atributo id de la etiqueta de entrada. </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>Mostrar sombra </p> </td>
      <td colname="col2"> <p>Agrega una sombra desplegable de cosmética a la lista de sugerencias de autocompletar. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Coincidir solo al principio de la frase </p> </td>
      <td colname="col2"> <p>Solo sugerir resultados que coincidan con el principio del texto de entrada . </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Compatibilidad con el conjunto de caracteres UTF-8 </p> </td>
      <td colname="col2"> <p>Administre correctamente los caracteres que no sean ASCII en los términos. </p> </td>
      </tr>
    </tbody> 
   </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuración de la lista de palabras de autocompletar {#task_1F8E0F346263443383F8CFD2C7AB35D4}

Configure la lista de palabras y frases que la función de completado automático muestra a un cliente como sugerencias.

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

Consulte [Configuración de la finalización automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Consulte [Configuración de CSS de autocompletar](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

**Para configurar la lista de palabras de completado automático**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Word List]**.
1. En la página [!DNL Auto-Complete Word List], configure las opciones que desee.

   Consulte [Vista previa del formulario de búsqueda tal como aparecería en su...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

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
      <td colname="col2"> <p> Controla el período de tiempo para la inclusión de palabras y frases de búsquedas recientes de un cliente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Recuento máximo de búsqueda </p> </td> 
      <td colname="col2"> <p>Controla el número máximo de palabras y frases buscadas que se incluirán en la lista de palabras autocompletada. Se incluyen las palabras y frases principales, que también son las más populares. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre del campo </p> </td> 
      <td colname="col2"> <p>Cada nombre de campo define el nombre de un campo para el que se incluyen valores indexados. Utilice + y - para añadir o quitar nombres de campo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Recuento máximo de valores </p> </td> 
      <td colname="col2"> <p>Define el recuento máximo de valores de campo permitidos para el nombre de campo seleccionado. Se incluyen los valores principales, que también son los más referenciados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Agregar estas palabras y frases </p> </td> 
      <td colname="col2"> <p> La lista de palabras de autocompletar se rellena con las palabras y frases que se enumeran en esta área. </p> <p> Haga clic en <span class="uicontrol"> Editar </span> para ver la lista o para agregar palabras y frases a la lista. Cuando haya terminado, haga clic en <span class="uicontrol"> Guardar cambios </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Eliminar estas palabras y frases </p> </td> 
      <td colname="col2"> <p> Las entradas de esta área no se muestran en la lista de palabras de autocompletar. </p> <p> Haga clic en <span class="uicontrol"> Editar </span> para ver la lista o para agregar palabras y frases a la lista. Cuando haya terminado, haga clic en <span class="uicontrol"> Guardar cambios </span>. </p> <p> En esta lista se permiten expresiones regulares. Para especificar una expresión regular en esta lista, empiece la línea con <code>regexp</code> seguida de un solo espacio, seguido de la expresión regular. Se eliminará cualquier línea de la lista de palabras que coincida con la expresión regular. </p> <p> <b>Importante</b>: Solo debe utilizar expresiones regulares si ya ha trabajado con ellas en otras aplicaciones. </p> <p>Consulte <a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expresiones regulares </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorar mayúsculas y minúsculas </p> </td> 
      <td colname="col2"> <p>Se eliminan las entradas duplicadas en la lista de palabras de autocompletar que solo difieren en mayúsculas/minúsculas alfabéticas; todas las entradas de la lista de palabras están obligadas a minúsculas. </p> <p>Si desea que las sugerencias de Autocompletar aparezcan en "primera letra en mayúsculas" o "todo en mayúsculas", agregue la variable 
        <code>
          text-transform : capitalize; 
        </code> o 
        <code>
          text-transform : uppercase; 
        </code> Propiedades de texto CSS al contenido de CSS de finalización automática, en "/* estilos para el elemento de resultado */". </p> <p>Consulte <a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> Configuración de CSS de autocompletar </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Actualización en reindexación </p> </td> 
      <td colname="col2"> <p>La lista de palabras de autocompletar se regenera automáticamente después de cada reindexación de cuenta correcta. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.
   * Haga clic en **[!UICONTROL Preview Word List]** para guardar los cambios realizados y, a continuación, abra la página [!DNL Auto-Complete Word List Preview] donde podrá revisar la lista de sugerencias de autocompletar. Utilice las opciones de navegación cercanas a la parte superior de la página para revisar y refinar la lista mostrada. Cuando haya terminado, haga clic en **[!UICONTROL Close]** para volver a la página [!DNL Auto-Complete Word List].

      Consulte [Uso de la opción Historial](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuración del CSS de autocompletar {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

Utilice la CSS de compleción automática para configurar la hoja de estilos en cascada de autocompletar que desea utilizar.

<!-- 

t_configuring_auto-complete_css.xml

 -->

La función de autocompletar CSS controla el contenido de [!DNL autocomplete_styles.css], que se incluye como parte del formulario de búsqueda habilitado para autocompletar. El CSS que especifique aquí controla la presentación visual de la lista de sugerencias de autocompletar. Para ver un ejemplo de las ideas de presentación visual que son posibles, consulte lo siguiente:

[https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html).

[Configuración de la lista de palabras de finalización automática](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4).

[Configuración de la finalización automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Cuando haya terminado de configurar la CSS de completado automático, podrá obtener una vista previa del formulario de búsqueda para ver si la CSS que ha especificado es aceptable en apariencia y diseño.

Consulte [Vista previa del formulario de búsqueda tal como aparecería en su...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

**Importante**: Para aplicar el CSS de autocompletado personalizado, debe eliminar las etiquetas de comentario de la segunda línea que aparece en el código HTML. A continuación, mueva la misma línea a dentro de la sección del encabezado de la página que contiene el formulario de búsqueda.

Consulte [Copia del código HTML del formulario de búsqueda en el...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**Para configurar la CSS de autocompletar**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete CSS]**.
1. En el campo de texto [!DNL Auto-Complete CSS], pegue o escriba la información de hoja de estilo en cascada que desee asociar a la lista de sugerencias de autocompletar.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Vista preliminar del formulario de búsqueda tal como aparecería en su sitio web {#task_437B35EFA5424603A08AF8E79E6B4714}

Según la configuración de la CSS de completado automático y de completado automático, puede obtener una vista previa del aspecto del formulario de búsqueda si desea agregar el código HTML a su sitio web.

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

Consulte [Configuración de la finalización automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Consulte [Configuración de CSS de autocompletar](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

Consulte [Copia del código HTML del formulario de búsqueda en el...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Consulte [Uso de colecciones en formularios de búsqueda](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Consulte [Uso de marcos con formularios](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consulte [Ejemplo de formulario de búsqueda avanzada](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Consulte [Código HTML de formulario de búsqueda avanzada](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9).

Consulte [Código de plantilla de formulario de búsqueda avanzada](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579).

**Obtener una vista previa del formulario de búsqueda tal como aparecería en el sitio web**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Search Form]**.
1. (Opcional) Haga clic en **[!UICONTROL HTML code]** para ver el HTML que copia y pega en las páginas de su sitio web.

## Copia del código HTML del formulario de búsqueda en las páginas del sitio web {#task_A3A01EA800F24C0AA33902387E0362C7}

Según la configuración de la CSS de completado automático y de completado automático, puede obtener una vista previa del aspecto del formulario de búsqueda si desea agregar el código HTML a su sitio web.

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

Consulte [Configuración de la finalización automática](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Consulte [Configuración de CSS de autocompletar](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

Consulte [Copia del código HTML del formulario de búsqueda en el...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Consulte [Uso de colecciones en formularios de búsqueda](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Consulte [Uso de marcos con formularios](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Consulte [Ejemplo de formulario de búsqueda avanzada](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Consulte [Código HTML de formulario de búsqueda avanzada](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9).

Consulte [Código de plantilla de formulario de búsqueda avanzada](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579).

**Para copiar el código HTML del formulario de búsqueda en las páginas del sitio web**

1. En el menú del producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**.

   >[!NOTE]
   >
   >No cambie el valor `form name=` en el origen del formulario.

1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Si ha configurado la CSS de autocompletar y desea que se apliquen los estilos al formulario de búsqueda, elimine las etiquetas de comentario de la segunda línea que aparece en el código HTML. A continuación, mueva la misma línea hasta dentro de la sección del encabezado de la página que contiene el formulario de búsqueda.
   * Para obtener el máximo rendimiento, mueva las etiquetas que aparecen en la parte inferior del código HTML y colóquelas en la parte inferior de la sección de cuerpo de cada página que contenga el formulario de búsqueda.

1. Copie el código y péguelo en las páginas web del sitio web donde desee que aparezca el formulario de búsqueda.
