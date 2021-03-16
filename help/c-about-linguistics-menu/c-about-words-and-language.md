---
description: Puede utilizar Palabras e idioma para determinar la correspondencia entre los términos de búsqueda y el contenido de las páginas web.
solution: Target
title: Acerca de las palabras y el idioma
topic: Lingüística, búsqueda en el sitio y comercialización
uuid: 793d7a40-4609-44b8-a170-536eb1434537
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---


# Acerca de las palabras y el idioma{#about-words-language}

Puede utilizar [!DNL Words & Language] para determinar cómo se corresponden los términos de búsqueda con el contenido de las páginas web.

## Uso de palabras e idioma {#concept_CEB4B9576F3C4E2EB87B352EEC738D79}

Antes de que los efectos de la configuración [!DNL Words & Language] estén disponibles para los visitantes del sitio, incluidos los cambios que realice en esa configuración, debe volver a generar el índice del sitio. La regeneración, a diferencia de la indexación, no implica rastrear las páginas web y tarda solo unos segundos.

## Configuración de la coincidencia de los términos de búsqueda con el contenido web {#task_351A9144A51F4B41923BDBACDEF3B616}

Puede utilizar Palabras e idioma para determinar cómo la búsqueda o comercialización del sitio coinciden los términos de búsqueda con el contenido de las páginas web.

<!-- 

t_configuring_how_search_terms_matched_to_your_web_content.xml

 -->

**Para configurar la correspondencia entre los términos de búsqueda y el contenido web**

1. En el menú del producto, haga clic en **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**.
1. En la página [!DNL Words & Languages], configure las opciones que desee.

   <!-- 
   
   r_words_and_languages_options.xml
   
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
      <td colname="col1"> <p>Distinción entre mayúsculas y minúsculas </p> </td> 
      <td colname="col2"> <p>No está seleccionado de forma predeterminada. </p> <p>Determina si las letras mayúsculas se distinguen de las minúsculas. Por ejemplo, cuando se selecciona "Correcto" se distingue de "Correcto" y los resultados de búsqueda pueden variar entre ambos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sensibilidad diacrítica </p> </td> 
      <td colname="col2"> <p>Seleccionado de forma predeterminada. </p> <p> Determina si las palabras que contienen caracteres diacríticos se distinguen de las palabras que no lo hacen. Por ejemplo, cuando se selecciona, la "pagina" se distingue de la "página". Anule la selección de esta opción si tiene un sitio web que utilice idiomas que no sean el inglés. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Números </p> </td> 
      <td colname="col2"> <p>Seleccionado de forma predeterminada. </p> <p>Determina si las palabras que contienen dígitos están indexadas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorar apóstrofes </p> </td> 
      <td colname="col2"> <p>No está seleccionado de forma predeterminada. </p> <p>Los apóstrofes se eliminan de las consultas. Por ejemplo, una búsqueda de "Árbol" devolverá los mismos resultados que una búsqueda de "Árboles". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorar guiones </p> </td> 
      <td colname="col2"> <p>No está seleccionado de forma predeterminada. </p> <p>Los guiones se eliminan de las consultas. Por ejemplo, una búsqueda de "campana azul" devolverá los mismos resultados que una búsqueda de "campana azul". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Coincidencia alfanumérica parcial </p> </td> 
      <td colname="col2"> <p>No está seleccionado de forma predeterminada. </p> <p>Cuando está seleccionada, esta opción permite dividir tokens en transiciones alfabético-numéricas para permitir coincidencias de texto libre en tokens de producto o parte. </p> <p>Por ejemplo, supongamos que tiene un identificador de producto <span class="codeph"> 910XT </span> en el contenido del cuerpo de una o más páginas de un sitio web. Cuando esta opción está <i>no</i> seleccionada, <span class="keyword"> Search&amp;Promote de Adobe </span> encuentra coincidencias para este identificador de producto al buscar <span class="codeph"> 910XT </span>. Y, con la <span class="uicontrol"> Búsqueda Concat-Div-Enable </span> activada, el <span class="keyword"> Search&amp;Promote de Adobe </span> también encontraría <span class="codeph"> 910 XT </span>. Sin embargo, no encontrará instancias de <span class="codeph"> 910 </span> o <span class="codeph"> XT </span> exclusivamente. </p> <p>Cuando selecciona <span class="uicontrol"> Coincidencia alfanumérica parcial </span>, el indizador divide estos tokens alfanuméricos mixtos en varios tokens. Por ejemplo, un identificador de producto como <span class="codeph"> XYZ123 </span> se indexa en tres tokens: <span class="codeph"> XYZ123 </span>, <span class="codeph"> XYZ </span> y <span class="codeph"> 123 </span>. Esta funcionalidad permite la coincidencia de texto libre en tiempo de búsqueda en cualquiera de estas variantes. </p> <p>En otro ejemplo, supongamos que tiene el identificador de producto <span class="codeph"> AB910XT </span>. Si selecciona <span class="uicontrol"> Coincidencia alfanumérica parcial </span> <i>y</i> tienen activado <span class="uicontrol"> Concat-Div-Enable </span>, <span class="keyword"> el Search&amp;Promote de Adobe </span> lo indexa como <span class="codeph"> AB910XT </span>, <span class="codeph"> AB </span>, <span class="codeph"> 910 </span> y <span class="codeph"> XT </span>. A continuación, cuando un usuario busca <span class="codeph"> 910XT </span>, por ejemplo, la búsqueda se amplía para encontrar también instancias de <span class="codeph"> 910XT </span>, <span class="codeph"> 910 </span> o <span class="codeph"> XT </span>. </p> <p> <p>Nota:  <span class="uicontrol"> Buscar Concat-Div-Enable </span> no está habilitado de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso. </p> </p> <p> <p>Nota:  <span class="uicontrol"> La coincidencia alfanumérica parcial </span> se aplica globalmente a todos los campos indexados. Sin embargo, solo afecta a la coincidencia de texto libre; no afecta a la coincidencia exacta ni a la coincidencia de intervalos. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Coincidencia de sonido </p> </td> 
      <td colname="col2"> <p>Seleccionado de forma predeterminada. </p> <p>Palabras que se emparejan por igual, como "salud" y "salud". Esta función permite al cliente buscar fácilmente a pesar de escribir una palabra mal. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Alternar Word Forms </p> </td> 
      <td colname="col2"> <p>El valor predeterminado es <b>Palabra alternativa predeterminada Forms</b>. </p> <p>Puede seleccionar entre las siguientes opciones de la lista desplegable Alternar Word Forms : 
      <ul id="ul_CAC73FB4D1384312BB5DD327D3D66948"> 
      <li id="li_F4E76CD27EA34AC5BC81E648BC6CBA4C"><b>Ninguna</b> <p>Durante la indexación no se aplican formularios de palabras alternativos ni de derivación. </p> </li> 
      <li id="li_3186FD1F3BC94A5CB66FFF8EA6726D81"><b>Palabra alternativa predeterminada Forms</b> <p>El emparejamiento se realiza automáticamente durante la indexación. </p> </li> 
      <li id="li_5815DE0795E0423C9C84C62B96A3F841"><b>Diccionario de dominio</b> <p>Cualquier diccionario de dominio que establezca como diccionario de derivación se utilizará como fuente de formularios de palabras alternativos. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> Acerca de los diccionarios </a>. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-dictionaries.md#task_541E8453A12F4A8E89CF6F595469F074" type="task" format="dita" scope="local"> Configuración de un diccionario como diccionario de derivación </a>. </p> </li> 
      </ul> </p> <p>Si la derivación de frases está habilitada en el Search&amp;Promote de Adobe <span class="keyword"> </span>, tenga en cuenta que también se producen formularios de palabras alternativos dentro de las frases. </p> <p>Consulte <a href="../c-searchpromote-release-notes/c-rn-06-19-14-version-815.md#concept_E8CEBC65A28A4E61BDE69B4B4DA55E73" format="dita" scope="local"> Notas de la versión 8.15.0 de la Search&amp;Promote (19/6/2014) </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Idioma  </p> </td> 
      <td colname="col2"> <p>El valor predeterminado es <b>inglés (Estados Unidos)</b>. </p> <p>El idioma seleccionado garantiza que los valores numéricos y de fecha se analicen según las convenciones utilizadas en la parte seleccionada del mundo. </p> <p>Cuando <span class="uicontrol"> Alternate Word Forms </span> se establece en <span class="uicontrol"> Default Alternate Word Forms </span> o en <span class="uicontrol"> Domain Dictionary </span>, los formularios de palabras y los fines de palabra cambian según las reglas lingüísticas del idioma seleccionado. </p> <p>De forma predeterminada, la configuración Idioma no se utiliza para determinar el idioma de las páginas leídas desde el sitio web. El idioma de una página de lectura se determina a partir de sus encabezados HTTP o de metaetiquetas dentro de la propia página. Su sitio web puede contener páginas en muchos idiomas diferentes. Cada página se lee e indexa correctamente, independientemente del idioma seleccionado aquí. </p> <p>Si utiliza una codificación de conjunto de caracteres Unicode como UTF-8 para algunas páginas de su sitio web, asegúrese de que el idioma de cada una de esas páginas esté especificado correctamente. Si no existen los encabezados o metaetiquetas HTTP adecuados para los documentos Unicode, puede utilizar <span class="uicontrol"> Configuración </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Inyecciones </span> para especificar el idioma correspondiente. </p> <p>Marque <span class="uicontrol"> ¿Aplicar a documentos sin un idioma especificado? </span> para utilizar la configuración de idioma para páginas leídas desde su sitio web que no tengan una configuración explícita. Utilice esta configuración cuando solo <i>algunos</i> de los documentos no tengan configuración de idioma. Utilice <span class="uicontrol"> Configuración </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Inyecciones </span> si <i>ninguno</i> de los documentos tiene configuración de idioma o si el conjunto de documentos afectados es una lista muy conocida y manejablemente pequeña. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5" type="concept" format="dita" scope="local"> Acerca de las inyecciones </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>¿Usar Decompounder? </p> </td> 
      <td colname="col2"> <p> <p>Nota:  Esta función solo se utiliza para danés y alemán. Además, esta función no está habilitada de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso. Una vez habilitada, el <b>Use Decompounder?</b> solo aparece en la interfaz de usuario si selecciona  <span class="uicontrol"> danés  </span> o  <span class="uicontrol"> alemán  </span> en la lista  <span class="uicontrol"> desplegable  </span> Idioma descrita anteriormente en esta tabla. </p> </p> <p>Al seleccionar <span class="uicontrol"> ¿Usar Decompounder? </span>, el servicio desglosa las palabras compuestas danesas o alemanas, que permiten la indexación de palabras de componentes junto con las palabras compuestas originales. </p> <p>Para ver cómo funciona esta función, introduzca palabras en el campo de texto y haga clic en <span class="uicontrol"> Probar </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Settings]**.
1. Para obtener una vista previa de los resultados de los cambios, haga clic en **[!UICONTROL regenerate your staged site index]** para reconstruir el índice del sitio web provisional.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

