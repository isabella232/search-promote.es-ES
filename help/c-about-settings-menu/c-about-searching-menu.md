---
description: Utilice el menú Búsqueda para definir palabras, colecciones, restricciones, vista previa y marcos excluidos.
seo-description: Utilice el menú Búsqueda para definir palabras, colecciones, restricciones, vista previa y marcos excluidos.
seo-title: Acerca del menú Búsqueda
solution: Target
subtopic: Searching
title: Acerca del menú Búsqueda
topic: Settings,Site search and merchandising
uuid: 072111fc-a32b-4acb-8337-cb21bcdb5542
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Acerca del menú Búsqueda{#about-the-searching-menu}

Utilice el menú Búsqueda para definir palabras, colecciones, restricciones, vista previa y marcos excluidos.

## Acerca de las búsquedas {#concept_207105CF26B1448F8A3D223787C56AB8}

Puede utilizar Búsquedas para definir y personalizar las búsquedas con nombre a las que pueden hacer referencia las plantillas de presentación.

<!-- 

c_about_searches.xml

 -->

En la plantilla de presentación puede hacer referencia a cualquier búsqueda con nombre definida dentro del módulo Búsquedas. A su vez, esto le permite personalizar fácilmente el tipo de búsqueda que se realiza para un conjunto determinado de plantillas.

Para excluir de los resultados de la búsqueda las frases y palabras comunes más utilizadas, consulte [Configuración de palabras](../c-about-linguistics-menu/c-about-excluded-words.md#task_60BF6BB7A66C48479D2BBB32C0F38CDE)excluidas.

Para definir áreas específicas en las que se pueden realizar búsquedas en el sitio web, consulte [Adición de colecciones](../c-about-settings-menu/c-about-searching-menu.md#task_07732D0F00104E59AD421297A704B2F6).

Para especificar un marco de destino para los vínculos de resultados de búsqueda, consulte [Uso de marcos con formularios](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Para restringir las búsquedas basadas en el referente HTTP, la dirección IP o el esquema de solicitud (HTTP o HTTPS), consulte [Configuración de valores en Vista previa](../c-about-settings-menu/c-about-searching-menu.md#task_CE267A0FF621474E80AB43B67B1C28D7).

## Sugerencias de búsqueda {#section_22F0E2BCF259459FA5F49FBCC0F09A7C}

Para obtener resultados de búsqueda más específicos, puede utilizar las siguientes sugerencias de búsqueda.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sugerencia de búsqueda </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Revisar ortografía </p> </td> 
   <td colname="col2"> <p>Asegúrese de que los términos de búsqueda estén escritos correctamente. Si <span class="uicontrol"> Coincidencia de sonido similar </span> está habilitada en <span class="uicontrol"> Lingüística </span> &gt; <span class="uicontrol"> Palabras e idiomas </span>, el motor de búsqueda intenta encontrar palabras que suenen similares a los términos de búsqueda. Sin embargo, siempre es mejor intentar escribir correctamente los términos de búsqueda. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> Acerca de palabras e idioma </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar varias palabras </p> </td> 
   <td colname="col2"> <p>Ejemplo: 
     <userinput>
       nuestro producto gratuito 
     </userinput> </p> <p>Las consultas de varias palabras devuelven resultados más refinados que las consultas de una sola palabra. </p> <p>Por ejemplo, 
     <userinput>
       nuestro producto gratuito 
     </userinput> devuelve resultados más relevantes que simplemente 
     <userinput>
       producto 
     </userinput>. </p> <p>Recuerde que los resultados relevantes se devuelven incluso si no contienen todos los términos de consulta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar palabras similares </p> </td> 
   <td colname="col2"> <p>Ejemplo: 
     <userinput>
       seguridad de la seguridad de la seguridad de la privacidad 
     </userinput> </p> <p>Cuanto más similares sean las palabras que se puedan utilizar en una consulta de búsqueda, más relevantes serán los resultados de búsqueda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilizar mayúsculas y minúsculas apropiadas </p> </td> 
   <td colname="col2"> <p>Ejemplo: 
     <userinput>
       Referencia de plantilla de búsqueda 
     </userinput> </p> <p>Ponga en mayúsculas los nombres adecuados. Si utiliza una palabra en minúsculas, el motor de búsqueda coincide con cualquier caso de la palabra. </p> <p>Por ejemplo, si escribe 
     <userinput>
       OR 
     </userinput>, el motor de búsqueda devuelve todos los documentos que contienen las palabras "búsqueda", "búsqueda" y "BÚSQUEDA". Sin embargo, si escribe 
     <userinput>
       Búsqueda  
     </userinput>, el motor de búsqueda devuelve documentos que sólo contienen la palabra en mayúsculas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar comillas </p> </td> 
   <td colname="col2"> <p>Ejemplo: 
     <userinput>
       "nuestra promesa a ti" 
     </userinput> </p> <p>Utilice las comillas para encontrar palabras que deben aparecer adyacentes entre sí, como "nuestra promesa a usted". Sin las comillas que lo rodean, los resultados de la búsqueda incluyen las palabras "nuestro", "nuestra", "nuestra", "a" y "usted", pero no necesariamente en ese orden. En su lugar, las palabras pueden aparecer en cualquier lugar y en cualquier orden dentro del documento. </p> <p> si utiliza el formulario de búsqueda avanzada con botones de opción para <span class="uicontrol"> cualquier </span>, todo <span class="uicontrol"> y </span>frase <span class="uicontrol"> , sólo puede utilizar comillas cuando </span>se haya seleccionado <span class="uicontrol"> </span> alguna. Las comillas se omiten si se selecciona <span class="uicontrol"> todo </span> o <span class="uicontrol"> frase </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilice + (más) o - (menos) </p> </td> 
   <td colname="col2"> <p>Ejemplo: 
     <userinput>
       +"idioma de plantilla" 
     </userinput> </p> <p>Utilice + para indicar que un término o frase de búsqueda debe aparecer en los resultados de la búsqueda. </p> <p>Usar: para indicar que un término o frase de búsqueda debe estar ausente de los resultados de búsqueda. </p> <p>Debe contener una frase entre comillas. No deje espacios entre el signo más o menos y el término de búsqueda, como en el ejemplo anterior. </p> <p> si utiliza el formulario de búsqueda avanzada con botones de opción para <span class="uicontrol"> cualquier </span>, todo <span class="uicontrol"> y </span>frase <span class="uicontrol"> , sólo puede utilizar comillas cuando </span>se haya seleccionado <span class="uicontrol"> </span> alguna. Los modificadores más y menos se omiten si <span class="uicontrol"> se selecciona toda </span> la frase o <span class="uicontrol"> frase </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar búsquedas de campo </p> </td> 
   <td colname="col2"> <p>Ejemplos: </p> <p> 
     <ul id="ul_F7CFF7652894402E8D19D6BA49792530"> 
      <li id="li_27492EF933C5437CB2C499746EC8CF39"> 
       <userinput>
         título:acerca de 
       </userinput> </li> 
      <li id="li_BD21505122104FD0B16A4DAD777811DA"> 
       <userinput>
         desc: "Nuestro equipo" 
       </userinput> </li> 
      <li id="li_8264630F8B3D46BF872EFEB1D69DB6BE"> 
       <userinput>
         claves:inicio de sesión 
       </userinput> </li> 
      <li id="li_EBB81CBFC6DA45E99A524890DCD56E9F"> 
       <userinput>
         cuerpo:seguridad 
       </userinput> </li> 
      <li id="li_6A852E35D6984A2C94144AB6C6D2DFA0"> 
       <userinput>
         alt:"unir ahora" 
       </userinput> </li> 
      <li id="li_F4C5699360484D12ACD62BBFB84A7904"> 
       <userinput>
         url:help 
       </userinput> </li> 
      <li id="li_B2DBBA2239E74D98868D92B3EDEF5B51"> 
       <userinput>
         target:Adobe 
       </userinput> </li> 
     </ul> </p> <p>Las búsquedas de campos permiten crear búsquedas específicas de palabras que aparecen en una parte específica de un documento. </p> <p>Puede realizar una búsqueda de campo en texto de cuerpo (cuerpo:), texto de título (título:), texto alt (alt:), descripción meta (desc:), palabras clave meta (claves:), dirección URL (url:) o palabras clave meta (objetivo:). Utilice minúsculas para el nombre del campo y seguida inmediatamente de dos puntos. No hay espacios entre los dos puntos y el término de búsqueda. </p> <p>Las búsquedas de campo solo van seguidas de una palabra o frase. Las frases deben estar entre comillas. </p> <p>si está utilizando el formulario de búsqueda avanzada con un cuadro de lista para el nombre del campo, sólo puede escribir los nombres de campo antes de una palabra o frase cuando <span class="uicontrol"> se haya seleccionado alguno </span> . Los nombres de campo específicos se omiten si se selecciona cualquier otro campo de formulario de búsqueda avanzada en el cuadro de lista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Usar caracteres comodín </p> </td> 
   <td colname="col2"> <p>Ejemplos: </p> <p> 
     <ul id="ul_D8E3867EB15641B0A6E55AD546CCB4DD"> 
      <li id="li_CB8B8FC15EB14B13BB33BB69F5206303"> 
       <userinput>
         wh* 
       </userinput> </li> 
      <li id="li_5350A934648C4C81BD6C0875061B426B"> 
       <userinput>
         "wh* are" 
       </userinput> </li> 
      <li id="li_7965A2F7186F40039D2F0736299D11B1"> 
       <userinput>
         415-*-* 
       </userinput> </li> 
     </ul> </p> <p>Las búsquedas con comodines expanden el número de coincidencias para una solicitud en particular. El carácter * se utiliza como carácter comodín. </p> <p>Por ejemplo, buscar 
     <userinput>
       wh* 
     </userinput> encuentra las palabras "qué", "por qué", "cuándo", "si" y cualquier otra palabra que empiece por "wh". Buscando *her* encuentra las palabras "aquí", "si", "juntos", "reuniendo" y cualquier otra palabra que contenga "ella" en cualquier parte de la palabra. </p> <p>Puede combinar caracteres comodín con modificadores + y -, comillas para frases, así como los especificadores de búsqueda de campos. </p> <p>La búsqueda 
     <userinput>
       +wh* -se*ch 
     </userinput> busca todas las páginas que tengan una palabra que comience por "wh" y que no contenga una palabra que comience por "se" y que termine por "ch". </p> <p>La búsqueda 
     <userinput>
       "wh* are" 
     </userinput> encuentra las frases "donde están", "qué son", "por qué son", etc. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Adición de una nueva definición de búsqueda {#task_98D3A168AB5D4F30A1ADB6E0D48AB648}

Puede utilizar el panel [!DNL GS Add Search] para configurar y agregar una nueva definición de búsqueda para los componentes de Búsqueda guiada, como facetas, rutas de exploración, navegación de página, menús y búsquedas recientes, en la capa de presentación.

<!-- 

t_adding_a_new_definition.xml

 -->

Después de agregar la nueva definición de búsqueda, asegúrese de hacer referencia a ella en la plantilla de presentación para que aparezca.

Consulte [Acerca de las plantillas](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Para agregar una nueva definición de búsqueda**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**.
1. En la [!DNL Searches] página, haga clic en **[!UICONTROL Add New Search]**.
1. En la **[!UICONTROL GS Add Search]** página, configure las opciones que desee.

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   Tenga en cuenta que las reglas de procesamiento que seleccionan la plantilla de presentación pueden anular algunas de estas opciones.

   Consulte [Adición de una nueva definición](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648) de búsqueda o [Edición de una definición](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461)de búsqueda.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nombre de búsqueda </p> </td> 
      <td colname="col2"> <p>Identifica el nombre de la búsqueda definida. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fuente </p> </td> 
      <td colname="col2"> <p>Permite seleccionar la búsqueda back-end que desee utilizar. Puede seleccionar entre <span class="wintitle"> SiteSearch </span> o <span class="wintitle"> Comercialización </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Cuenta </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Search&amp;Promote </span> como fuente. </p> <p>Le permite seleccionar la cuenta de comercialización/búsqueda del sitio que desee buscar. Normalmente, una búsqueda se realiza en la cuenta que está utilizando. Sin embargo, la plantilla de presentación puede utilizar una búsqueda back-end para cualquiera de las otras cuentas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre del servidor/IP </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Comercialización </span> como fuente. </p> <p>Especifica el nombre completo del <span class="wintitle"> servidor Comercialización </span> al que debe acceder la <span class="wintitle"> búsqueda </span> Comercialización. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Puerto del servidor </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Comercialización </span> como fuente. </p> <p>Especifica el número de puerto del <span class="wintitle"> servidor </span> de comercialización. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pirámide </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Comercialización </span> como fuente. </p> <p>Especifica la pirámide dentro del <span class="wintitle"> servidor de comercialización </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número De Resultados </p> </td> 
      <td colname="col2"> <p>Especifica el número de resultados de búsqueda que desea devolver. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de resultados de la primera página (si es diferente) </p> </td> 
      <td colname="col2"> <p>Especifica el número de resultados que se devuelven en la primera página. Utilice esta opción si necesita que sea diferente de otras páginas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número De Columnas </p> </td> 
      <td colname="col2"> <p>Especifica el número de columnas por las que se dividen los resultados de búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo De Búsqueda </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Search&amp;Promote </span> como fuente. </p> <p>Permite seleccionar entre los tres tipos de búsqueda siguientes. </p> <p> 
        <ul id="ul_2F6FA9EFD8DB49EEAB866C3D070E2644"> 
          <li id="li_ECFEBEDD86FF4DE2BB768423B3B91B5E"> <span class="uicontrol"> todo </span> <p>Busca documentos que contengan todas las palabras de la cadena de consulta. </p> <p>El uso de "+" y "-" antes de que las palabras de búsqueda se desactiven y se ignoren esos caracteres. </p> </li> 
          <li id="li_62EB215BDDE74DF0BF76B3BD5B96776F"> <span class="uicontrol"> cualquiera </span> <p>Se permite el uso de prefijos de palabras "+" y "-". </p> </li> 
          <li id="li_3D71982C0BBA41AFA353069AF3F2F6D8"> <span class="uicontrol"> frase </span> <p>La cadena de consulta se trata como si fuera una frase citada y se omiten todas las comillas escritas por el usuario. </p> <p>El uso de "+" y "-" antes de que las palabras de búsqueda se desactiven y se ignoren esos caracteres. </p> </li> 
        </ul> </p> <p> Si desea que cada palabra de una consulta seleccione potencialmente un valor de faceta, la búsqueda principal siempre debe utilizar <span class="uicontrol"> todo </span>. </p> <p>Puede revisar las sugerencias de búsqueda con respecto al uso de los modificadores + y - en una consulta de búsqueda. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">Acerca de las búsquedas </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Colección </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Search&amp;Promote </span> como fuente. </p> <p>Identifica la colección dentro del índice que desea buscar. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Promosearch </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Search&amp;Promote </span> como fuente. </p> <p>Permite utilizar una selección aleatoria de los resultados de búsqueda, según el <span class="uicontrol"> Número de resultados </span> que haya especificado. </p> <p>Promosearch es un concepto heredado. Como tal, recomendamos que utilice el nuevo sistema de administración de titulares dentro de la búsqueda o comercialización del sitio. </p> <p>Consulte <a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">Acerca de los titulares </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aplicar parámetros de faceta </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si eligió <span class="uicontrol"> Search&amp;Promote </span> como fuente y seleccionó <span class="uicontrol"> Promosearch </span>. </p> <p>Especifica que una búsqueda promocional utiliza las facetas seleccionadas para reducir las promociones. La mayoría de las cuentas de promoción no utilizan esta opción. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Proporcione la promoción predeterminada si no hay ninguna promoción coincidente </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si eligió <span class="uicontrol"> Search&amp;Promote </span> como fuente y seleccionó <span class="uicontrol"> Promosearch </span>. </p> <p>Especifica que se produce otra búsqueda de promoción si la búsqueda inicial de una promoción no encuentra nada. La segunda búsqueda de una promoción coloca la palabra clave. En su lugar, busca cualquier promoción en la que un campo de metadatos "is_default" esté establecido en "yes". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Resaltar búsqueda </p> </td> 
      <td colname="col2"> <p>Extrae un número seleccionado de resultados de la búsqueda principal que desea resaltar en una "zona heroica". </p> <p>Normalmente, las búsquedas de resaltado tienen criterios de búsqueda similares a la búsqueda principal pero con un mecanismo de clasificación diferente para resaltar ciertos resultados. El software elimina los duplicados de la búsqueda principal. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Búsqueda base </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si seleccionó <span class="uicontrol"> Resaltar búsqueda </span>. </p> <p>Le permite seleccionar la búsqueda que tiene los resultados de los que está resaltando los resultados. Los duplicados se eliminan de esta búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Prioridad de DeDupe </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si seleccionó <span class="uicontrol"> Resaltar búsqueda </span>. </p> <p>Permite realizar varias búsquedas de resaltado. </p> <p>Cuando tenga varias búsquedas de resaltado, debe especificar la prioridad de la anulación de duplicación, donde "1" es la prioridad más alta. </p> <p>Por ejemplo, supongamos que tiene dos búsquedas resaltadas: los mejores vendedores y los nuevos productos. Teóricamente. es posible que un supervendedor sea también un producto nuevo. En este caso, desea eliminar el duplicado de los nuevos productos y de la búsqueda principal. Por lo tanto, usted establece la prioridad de los bestsellers en 1 y la prioridad de los nuevos productos en 2. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetro </p> </td> 
      <td colname="col2"> <p>Permite agregar parámetros CGI a la búsqueda. </p> <p>Consulte <a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita"> Parámetros CGI de búsqueda back-end </a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Add]**.
1. (Opcional) En la [!DNL Searches] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una definición de búsqueda {#task_AF1FFB1AEF874C13AB359C28F74BF461}

Puede utilizar el panel para volver a configurar una definición de búsqueda existente para la capa de presentación Búsqueda guiada. [!DNL Staged GS Edit Search]

<!-- 

t_editing_a_search_definition.xml

 -->

Después de editar la definición de búsqueda, asegúrese de que ha hecho referencia a ella en la plantilla de presentación para que aparezca.

Consulte [Acerca de las plantillas](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Para editar una definición de búsqueda**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**.
1. En la tabla de la [!DNL Searches] página, haga clic **[!UICONTROL Edit]** en la fila de la definición que desee cambiar.
1. En la **[!UICONTROL GS Edit Search]** página, configure las opciones que desee.

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   Tenga en cuenta que las reglas de procesamiento que seleccionan la plantilla de presentación pueden anular algunas de estas opciones.

   Consulte [Adición de una nueva definición](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648) de búsqueda o [Edición de una definición](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461)de búsqueda.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nombre de búsqueda </p> </td> 
      <td colname="col2"> <p>Identifica el nombre de la búsqueda definida. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fuente </p> </td> 
      <td colname="col2"> <p>Permite seleccionar la búsqueda back-end que desee utilizar. Puede seleccionar entre <span class="wintitle"> SiteSearch </span> o <span class="wintitle"> Comercialización </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Cuenta </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Search&amp;Promote </span> como fuente. </p> <p>Le permite seleccionar la cuenta de comercialización/búsqueda del sitio que desee buscar. Normalmente, una búsqueda se realiza en la cuenta que está utilizando. Sin embargo, la plantilla de presentación puede utilizar una búsqueda back-end para cualquiera de las otras cuentas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre del servidor/IP </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Comercialización </span> como fuente. </p> <p>Especifica el nombre completo del <span class="wintitle"> servidor Comercialización </span> al que debe acceder la <span class="wintitle"> búsqueda </span> Comercialización. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Puerto del servidor </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Comercialización </span> como fuente. </p> <p>Especifica el número de puerto del <span class="wintitle"> servidor </span> de comercialización. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pirámide </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Comercialización </span> como fuente. </p> <p>Especifica la pirámide dentro del <span class="wintitle"> servidor de comercialización </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número De Resultados </p> </td> 
      <td colname="col2"> <p>Especifica el número de resultados de búsqueda que desea devolver. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número de resultados de la primera página (si es diferente) </p> </td> 
      <td colname="col2"> <p>Especifica el número de resultados que se devuelven en la primera página. Utilice esta opción si necesita que sea diferente de otras páginas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número De Columnas </p> </td> 
      <td colname="col2"> <p>Especifica el número de columnas por las que se dividen los resultados de búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo De Búsqueda </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Search&amp;Promote </span> como fuente. </p> <p>Permite seleccionar entre los tres tipos de búsqueda siguientes. </p> <p> 
        <ul id="ul_E1D8B3DE9DB24DE4813D53F6298A03A6"> 
          <li id="li_C3DD7AA7699B477A9EE0731CFC012630"> <span class="uicontrol"> todo </span> <p>Busca documentos que contengan todas las palabras de la cadena de consulta. </p> <p>El uso de "+" y "-" antes de que las palabras de búsqueda se desactiven y se ignoren esos caracteres. </p> </li> 
          <li id="li_4C66B9EFEFA042908A4D3730F9F54EB0"> <span class="uicontrol"> cualquiera </span> <p>Se permite el uso de prefijos de palabras "+" y "-". </p> </li> 
          <li id="li_37E9AD42A61C4E31A0816DFB8E71118D"> <span class="uicontrol"> frase </span> <p>La cadena de consulta se trata como si fuera una frase citada y se omiten todas las comillas escritas por el usuario. </p> <p>El uso de "+" y "-" antes de que las palabras de búsqueda se desactiven y se ignoren esos caracteres. </p> </li> 
        </ul> </p> <p> Si desea que cada palabra de una consulta seleccione potencialmente un valor de faceta, la búsqueda principal siempre debe utilizar <span class="uicontrol"> todo </span>. </p> <p>Puede revisar las sugerencias de búsqueda con respecto al uso de los modificadores + y - en una consulta de búsqueda. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">Acerca de las búsquedas </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Colección </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Search&amp;Promote </span> como fuente. </p> <p>Identifica la colección dentro del índice que desea buscar. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Promosearch </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si elige <span class="uicontrol"> Search&amp;Promote </span> como fuente. </p> <p>Permite utilizar una selección aleatoria de los resultados de búsqueda, según el <span class="uicontrol"> Número de resultados </span> que haya especificado. </p> <p>Promosearch es un concepto heredado. Como tal, recomendamos que utilice el nuevo sistema de administración de titulares dentro de la búsqueda o comercialización del sitio. </p> <p>Consulte <a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">Acerca de los titulares </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aplicar parámetros de faceta </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si eligió <span class="uicontrol"> Search&amp;Promote </span> como fuente y seleccionó <span class="uicontrol"> Promosearch </span>. </p> <p>Especifica que una búsqueda promocional utiliza las facetas seleccionadas para reducir las promociones. La mayoría de las cuentas de promoción no utilizan esta opción. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Proporcione la promoción predeterminada si no hay ninguna promoción coincidente </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si eligió <span class="uicontrol"> Search&amp;Promote </span> como fuente y seleccionó <span class="uicontrol"> Promosearch </span>. </p> <p>Especifica que se produce otra búsqueda de promoción si la búsqueda inicial de una promoción no encuentra nada. La segunda búsqueda de una promoción coloca la palabra clave. En su lugar, busca cualquier promoción en la que un campo de metadatos "is_default" esté establecido en "yes". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Resaltar búsqueda </p> </td> 
      <td colname="col2"> <p>Extrae un número seleccionado de resultados de la búsqueda principal que desea resaltar en una "zona heroica". </p> <p>Normalmente, las búsquedas de resaltado tienen criterios de búsqueda similares a la búsqueda principal pero con un mecanismo de clasificación diferente para resaltar ciertos resultados. El software elimina los duplicados de la búsqueda principal. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Búsqueda base </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si seleccionó <span class="uicontrol"> Resaltar búsqueda </span>. </p> <p>Le permite seleccionar la búsqueda que tiene los resultados de los que está resaltando los resultados. Los duplicados se eliminan de esta búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Prioridad de DeDupe </p> </td> 
      <td colname="col2"> <p>Esta opción solo está disponible si seleccionó <span class="uicontrol"> Resaltar búsqueda </span>. </p> <p>Permite realizar varias búsquedas de resaltado. </p> <p>Cuando tenga varias búsquedas de resaltado, debe especificar la prioridad de la anulación de duplicación, donde "1" es la prioridad más alta. </p> <p>Por ejemplo, supongamos que tiene dos búsquedas resaltadas: los mejores vendedores y los nuevos productos. Teóricamente. es posible que un supervendedor sea también un producto nuevo. En este caso, desea eliminar el duplicado de los nuevos productos y de la búsqueda principal. Por lo tanto, usted establece la prioridad de los bestsellers en 1 y la prioridad de los nuevos productos en 2. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetro </p> </td> 
      <td colname="col2"> <p>Permite agregar parámetros CGI a la búsqueda. </p> <p>Consulte <a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita"> Parámetros CGI de búsqueda back-end </a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) En la [!DNL Searches] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una definición de búsqueda {#task_1D8E991E4C4146B7A7311FAE5DAA3742}

Puede eliminar una definición de búsqueda de guía que ya no necesite ni use.

<!-- 

t_deleting_a_search_definition.xml

 -->

Consulte [Acerca de las plantillas](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Para eliminar una definición de búsqueda**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**.
1. En la [!DNL Searches] página, en la tabla, haga clic **[!UICONTROL Delete]** en la fila de la definición que desee eliminar.
1. En el cuadro de diálogo [!DNL Confirmation] , haga clic en **[!UICONTROL OK]**.
1. (Opcional) En la [!DNL Searches] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del Administrador de palabras clave de resultados anclados {#concept_0C5F152C029C485D8872C6795CBCD7C7}

Puede fijar manualmente los resultados de búsqueda en una ubicación específica. Estos resultados anclados se asocian con una consulta o palabras clave de búsqueda específicas. Puede usar [!DNL Pinned Result Keyword Manager] para administrar todas las palabras clave con resultados anclados.

<!-- 

c_about_pinned_results_keyword_manager.xml

 -->

## Reglas de búsqueda de palabras clave que seguir {#section_ED67A24BE884468286F34FA5DFF826D7}

La consulta de búsqueda que se introduce en el panel tiene las siguientes reglas:

* Los espacios al inicio y al final se eliminan de la consulta.
* No se permiten caracteres de búsqueda especiales como los siguientes:

   * Coincidencia de comodines con asteriscos (*).
   * No se debe tener o no se debe tener el uso de más o menos (+ o -).
   * No hay ningún especificador de campos con el carácter de dos puntos (:).
   * Sin comas ni comillas dobles (, o &quot;).

* Se permiten varios términos o palabras separados por espacios en la consulta.
* Las letras mayúsculas se convierten en minúsculas.

Los términos de búsqueda se recuerdan exactamente como están; debe utilizar los mismos términos de búsqueda para obtener los mismos resultados.

Los resultados anclados no admiten distinción entre mayúsculas y minúsculas. Todas las palabras clave tienen sus letras mayúsculas convertidas en minúsculas.

## Reordenación de los resultados de búsqueda {#section_46FBE5279C7740A09D6DC9F54FE104AA}

Al buscar una palabra clave en el [!DNL Stage Add New Keyword] [!DNL Staged Edit Keyword] panel o en el panel, los resultados de la búsqueda reflejan lo que podría suceder después de la siguiente operación de índice. Puede reordenar los resultados de búsqueda en la tabla utilizando uno de los tres métodos diferentes.

El primer método se realiza mediante la casilla de verificación **[!UICONTROL Pinned]** . La casilla de verificación se utiliza para fijar un resultado a una posición específica. Al seleccionar la casilla de verificación, todos los resultados de búsqueda que se encuentran encima de ella también se fijan. Esta funcionalidad garantiza que todos los resultados por encima de esa casilla de verificación aparezcan en ese orden específico. Al desanclar un resultado de búsqueda, éste cae por debajo de todos los resultados anclados actualmente.

El segundo método consiste en arrastrar y soltar en la tabla. Puede mover un resultado a una nueva posición con la función de arrastrar y soltar. Después de arrastrar un resultado a una nueva ubicación, todos los resultados por encima de la nueva ubicación se fijarán. Este anclaje automático garantiza que el resto de los resultados aparecerán por encima del resultado arrastrado recientemente.

El tercer método es establecer el orden de los resultados anclados introduciendo una posición específica en la columna &quot;#&quot;. A diferencia de lo que sucede con la función de arrastrar y soltar, el orden de los resultados de búsqueda simulados solo es obvio la próxima vez que abra el [!DNL Staged Edit Keyword] panel. Al configurar el número de pedido de una fila sin fijar se garantiza que al menos muchos elementos se fijen. Al definir el número de pedido de una fila que está anclada actualmente, se establece el orden de ese elemento dentro de los elementos que están anclados actualmente. Sin embargo, no aumenta el número de elementos anclados.

Al guardar los resultados de la búsqueda, puede volver a ver los resultados introduciendo la misma consulta en el campo Palabra clave.

## Acerca de los resultados de búsqueda anclados {#section_46780B7812F249F3B45503161C4FBDEE}

Los resultados de búsqueda se ordenan con frecuencia según la puntuación de relevancia. Sin embargo, un resultado de búsqueda anclado ignora la puntuación de relevancia e intenta anular el orden natural con su posición predeterminada. Al garantizar que el resultado permanezca relativamente donde está, es necesario fijar otros resultados de búsqueda conocidos por encima.

Los resultados de búsqueda que se muestran en el panel simulan lo que aparece después del siguiente índice. Sin embargo, los cambios del documento original o determinados cambios de configuración en el Centro de miembros pueden producir resultados con discrepancias. Por ejemplo, cambiar el contenido de un documento no se conoce hasta después del índice.

Los resultados anclados aparecen en un orden similar o similar después del índice porque ignoran la relevancia. Los resultados no anclados vuelven a su posición natural después de un índice; no se garantiza el orden de los resultados sin fijar.

## Adding a new keyword {#task_8CED128DADD34D0DAD2C64B64D0D6B06}

Puede agregar nuevas palabras clave y sus resultados anclados.

<!-- 

t_adding_a_new_keyword.xml

 -->

Cuando agrega una nueva palabra clave, puede reordenar los resultados de búsqueda y fijarlos a una posición específica.

**Para agregar una nueva palabra clave**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**.
1. En la [!DNL Pinned Keyword Results Manager] página, haga clic en **[!UICONTROL Add New Keyword]**.
1. En la [!DNL Add New Keyword] página, en el **[!UICONTROL Keyword]** campo, introduzca una consulta de búsqueda y, a continuación, haga clic en **[!UICONTROL Search Keyword]**.

   <!-- 
   
   r_keyword_options.xml
   
   -->

   Puede utilizar el botón Editar tabla para ajustar la forma en que se ve la tabla de resultados de búsqueda. Por ejemplo, puede utilizar la lista de columnas para mostrar u ocultar columnas específicas. También puede reorganizar el orden de las columnas mediante la función de arrastrar y soltar.

   En la tabla siguiente se describen las propiedades de columna que se encuentran en el editor de tablas.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Columna </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Pedido </p> </td> 
      <td colname="col2"> <p>Especifica el orden numérico del aspecto de las columnas. Puede arrastrar y soltar las columnas para actualizar automáticamente el orden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre del campo </p> </td> 
      <td colname="col2"> <p>Identifica el nombre del encabezado de columna que aparece en la tabla Resultados de la búsqueda <span class="wintitle"> simulada </span> del panel Agregar nueva palabra clave <span class="wintitle"> escalonada </span> y del panel Editar palabra clave <span class="wintitle"> en etapas </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclusión </p> </td> 
      <td colname="col2"> <p>La columna aparece en la Tabla de resultados anclados si se marca la casilla. Si el cuadro está vacío o no está seleccionado, la columna desaparece de la tabla. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mostrar URL como imagen </p> </td> 
      <td colname="col2"> <p>Si el campo meta asignado a esta columna tiene direcciones URL para gráficos o imágenes, al marcar esta casilla se colocan etiquetas de imagen HTML alrededor de él y aparece la imagen. Las imágenes que faltan o los vínculos incorrectos están vacíos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Longitud del campo </p> </td> 
      <td colname="col2"> <p>Permite introducir la longitud máxima del texto para mostrar antes de que se trunque con elipses (...). Si la columna está configurada para mostrar las direcciones URL como imágenes, este campo no tiene ningún efecto. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Reordene los resultados de la búsqueda.
   * Haga clic **[!UICONTROL Edit Table]** para ajustar la vista de la [!DNL Simulated Search Results] tabla. Cuando haya terminado, haga clic en **[!UICONTROL Save Changes]** para volver al [!DNL Add New Keyword] panel.

1. Haga clic **[!UICONTROL Save Search Results]**.
1. (Opcional) Si desea obtener una vista previa de los resultados, vuelva a generar el índice del sitio escalonado.

   Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.
1. (Opcional) En la [!DNL Pinned Results Keyword Manager] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una palabra clave {#task_30C550A7350B4394B5B43536368A84B1}

Puede editar las palabras clave existentes y sus resultados anclados.

<!-- 

t_editing_a_keyword.xml

 -->

Al editar una palabra clave, puede reordenar los resultados de búsqueda y fijarlos a una posición específica.

**Para editar una palabra clave**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**.
1. En la [!DNL Pinned Keyword Results Manager] página, en la tabla, haga clic **[!UICONTROL Edit]** en la fila de la palabra clave que desee cambiar.
1. En la [!DNL Edit Keyword] página, en el **[!UICONTROL Keyword]** campo, introduzca una consulta de búsqueda y, a continuación, haga clic en **[!UICONTROL Search Keyword]**.

   Asegúrese de seguir las reglas para la búsqueda de palabras clave.

   <!-- 
   
   r_keyword_options.xml
   
   -->

   Puede utilizar el botón Editar tabla para ajustar la forma en que se ve la tabla de resultados de búsqueda. Por ejemplo, puede utilizar la lista de columnas para mostrar u ocultar columnas específicas. También puede reorganizar el orden de las columnas mediante la función de arrastrar y soltar.

   En la tabla siguiente se describen las propiedades de columna que se encuentran en el editor de tablas.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Columna </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Pedido </p> </td> 
      <td colname="col2"> <p>Especifica el orden numérico del aspecto de las columnas. Puede arrastrar y soltar las columnas para actualizar automáticamente el orden. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre del campo </p> </td> 
      <td colname="col2"> <p>Identifica el nombre del encabezado de columna que aparece en la tabla Resultados de la búsqueda <span class="wintitle"> simulada </span> del panel Agregar nueva palabra clave <span class="wintitle"> escalonada </span> y del panel Editar palabra clave <span class="wintitle"> en etapas </span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclusión </p> </td> 
      <td colname="col2"> <p>La columna aparece en la Tabla de resultados anclados si se marca la casilla. Si el cuadro está vacío o no está seleccionado, la columna desaparece de la tabla. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mostrar URL como imagen </p> </td> 
      <td colname="col2"> <p>Si el campo meta asignado a esta columna tiene direcciones URL para gráficos o imágenes, al marcar esta casilla se colocan etiquetas de imagen HTML alrededor de él y aparece la imagen. Las imágenes que faltan o los vínculos incorrectos están vacíos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Longitud del campo </p> </td> 
      <td colname="col2"> <p>Permite introducir la longitud máxima del texto para mostrar antes de que se trunque con elipses (...). Si la columna está configurada para mostrar las direcciones URL como imágenes, este campo no tiene ningún efecto. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Reordene los resultados de la búsqueda.
   * Haga clic **[!UICONTROL Edit Table]** para ajustar la vista de la [!DNL Simulated Search Results] tabla.

      Consulte [Adición de una nueva palabra clave](../c-about-settings-menu/c-about-searching-menu.md#task_8CED128DADD34D0DAD2C64B64D0D6B06).

      Cuando haya terminado, haga clic en **[!UICONTROL Save Changes]** para volver al [!DNL Add New Keyword] panel.

1. Haga clic **[!UICONTROL Save Search Results]**.
1. (Opcional) Si desea obtener una vista previa de los resultados, vuelva a generar el índice del sitio escalonado.

   Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.
1. (Opcional) En la [!DNL Pinned Results Keyword Manager] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una palabra clave {#task_F17D6357D6DD416495E6D4117899D81D}

Puede eliminar palabras clave que ya no necesite ni use.

<!-- 

t_deleting_a_keyword.xml

 -->

Cuando agrega una nueva palabra clave, puede reordenar los resultados de búsqueda y fijarlos a una posición específica.

**Para eliminar una palabra clave**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**.
1. En la [!DNL Pinned Keyword Results Manager] página, en la tabla, haga clic **[!UICONTROL Delete]** en la fila de la palabra clave que desee eliminar.
1. En la [!DNL Delete Keyword] página, haga clic en **[!UICONTROL Delete]**.
1. (Opcional) Si desea obtener una vista previa de los resultados, vuelva a generar el índice del sitio escalonado.

   Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.
1. (Opcional) En la [!DNL Pinned Results Keyword Manager] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las colecciones {#concept_62E42ACE53D54EEE9273433B86259127}

Puede utilizar las colecciones para permitir que los clientes busquen áreas específicas de un sitio web para que puedan encontrar rápidamente lo que buscan.

<!-- 

c_about_collections.xml

 -->

Consulte [Acerca de las búsquedas](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

Consulte [Uso de colecciones en formularios](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)de búsqueda.

Por ejemplo: los clientes pueden buscar una colección de direcciones URL relacionadas con las ventas de productos o con los servicios de asistencia. Antes de que los clientes puedan utilizar las colecciones que especifique, asegúrese de actualizar el formulario de búsqueda en el menú Buscar formulario.

Antes de que los clientes vean los efectos de la configuración de colecciones, vuelva a generar el índice del sitio.

Puede probar las colecciones introduciendo una de las direcciones URL del sitio web en el campo opcional **[!UICONTROL Test Collections]** y, a continuación, haciendo clic en **[!UICONTROL Test]**. Se devuelve la colección a la que pertenece la página especificada.

Cada colección se especifica en una sola línea con un nombre y una máscara URL. Una máscara URL puede constar de lo siguiente:

* una ruta completa como `https://www.mydomain.com/products.html`
* una ruta parcial como `https://www.mydomain.com/products`
* una expresión regular

   Para que una máscara sea una expresión regular, inserte la palabra clave `regexp` entre el nombre de la colección y la máscara de URL.

   Consulte Expresiones [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Cada línea del campo Colecciones puede contener una sola máscara de dirección URL. Sin embargo, puede especificar varias máscaras URL para el mismo nombre de colección en líneas diferentes. El siguiente ejemplo contiene cuatro nombres de colección diferentes y cinco máscaras URL:

```
Company Info https://www.yoursite.com/company 
Products https://www.yoursite.com/products 
FAQs regexp ^.*/faqs 
Support https://www.yoursite.com/email_support/ 
Support https://www.yoursite.com/phone_support/
```

En este ejemplo, después de actualizar el formulario de búsqueda para incluir estas colecciones, los clientes pueden seleccionar y buscar cada colección definida de forma individual. La `Support` colección incluye archivos que coinciden con las dos máscaras de URL, de modo que los archivos de ambos `www.yoursite.com/email_support/` y `www.yoursite.com/phone_support` se buscan cuando se selecciona esta colección.

## Adición de colecciones {#task_07732D0F00104E59AD421297A704B2F6}

Puede agregar colecciones para permitir que los clientes busquen áreas específicas del sitio web para que puedan encontrar rápidamente lo que buscan.

<!-- 

t_adding_collections.xml

 -->

Asegúrese de volver a generar el índice del sitio para que los resultados de las máscaras URL sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

**Para agregar colecciones**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Collections]**.
1. En el [!DNL Collections] campo, introduzca un nombre de colección y una dirección de máscara URL, uno por línea.
1. (Opcional) En la [!DNL Collections] página, en el **[!UICONTROL Test Collections]** campo, introduzca una máscara de URL de prueba en el sitio web y, a continuación, haga clic en **[!UICONTROL Test]**.

   Se muestra una ventana de salida de la colección de prueba que muestra la dirección URL y el nombre de la colección.
1. Cuando termine de agregar colecciones, haga clic en **[!UICONTROL Save Changes]**.
1. (Opcional) Si desea obtener una vista previa de los resultados, vuelva a generar el índice del sitio escalonado.

   Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.
1. (Opcional) En la [!DNL Collections] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las restricciones {#concept_B5B527E04EBF4E9AB5956EEF881DDBF1}

Antes de realizar una búsqueda, se examinan la dirección URL y la dirección IP de referencia para determinar si es posible realizar una búsqueda desde esa ubicación. Lo que especificó en [!DNL Restrictions] determina si la búsqueda está permitida. Si no se permite una búsqueda, se devuelve una página de error genérica al solicitante.

<!-- 

c_about_restrictions.xml

 -->

Puede especificar la configuración de restricción como máscaras URL de referente o máscaras de dirección IP. Ambos tipos de restricciones utilizan máscaras para permitir búsquedas y excluir máscaras para denegarlas.

Se permite una búsqueda si pasa los criterios de restricción de dirección IP y dirección URL del referente. Si alguna de estas opciones no permite la búsqueda, ésta falla, independientemente de otras restricciones que la permitan.

Por ejemplo: si el campo &quot;referente HTTP&quot; de una solicitud de búsqueda coincide con una máscara de dirección URL de referente &quot;excluir&quot;, la búsqueda falla, incluso si la dirección IP solicitante coincide con una máscara de dirección IP &quot;incluir&quot;. Si ninguna máscara coincide con la dirección URL o IP del referente, la ubicación se incluye de forma predeterminada.

Introduzca cada máscara de inclusión o de exclusión en una sola línea.

## Adición de máscara de dirección URL de referente o restricciones de máscara de dirección IP {#task_E6FF2DD83E8D4B00A0E2809DC13A56C9}

Puede especificar la configuración de restricción como &quot;Máscaras URL de referente&quot; o &quot;Máscaras de dirección IP&quot;. Ambos tipos de restricciones utilizan máscaras para permitir búsquedas y excluir máscaras para denegarlas. Se permite una búsqueda si pasa los criterios de restricción de dirección IP y dirección URL del referente.

<!-- 

t_adding_url_mask_or_jp_address_restrictions.xml

 -->

**Para agregar la máscara de dirección URL del referente o restricciones de máscara de dirección IP**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Restrictions]**.
1. En la [!DNL Restrictions] página, configure las opciones de restricción que desee. Escriba las direcciones de máscara de dirección URL del referente, las direcciones de máscara de dirección IP o, opcionalmente, una dirección URL de una página web personalizada que se muestra a los clientes a los que no se permite realizar búsquedas en el sitio.

   <!-- 
   
   r_restriction_options.xml
   
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
      <td colname="col1"> <p>Máscaras de URL de referente </p> </td> 
      <td colname="col2"> <p>Se lee la dirección URL del referente desde el encabezado del referente HTTP. La primera máscara que coincide con la dirección URL del referente determina si se permite la búsqueda, si la máscara es una máscara de inclusión. O bien, determina si no se permite la búsqueda, si la máscara es una máscara de exclusión. Si no hay ninguna máscara que coincida con la dirección URL del referente, se incluye esa dirección URL y se permite la búsqueda. </p> <p> Si la plantilla de búsqueda contiene un nuevo formulario de búsqueda o si la plantilla de búsqueda puede contener vínculos como "Siguiente 10", "Anterior 10" o "Ocultar resúmenes", la plantilla de resultados de búsqueda se mostrará como una máscara de "inclusión". La forma más sencilla de hacerlo es con la expresión regular, como en el ejemplo siguiente: </p> <p> <span class="codeph"> incluir regexp ^https?://[^/]*\.atomz\.com/.*[?&amp;]sp_a=sp1000130e.*$ </span> </p> <p>El ejemplo siguiente contiene cinco máscaras URL de referente diferentes: </p> <p> <code> include&nbsp;https://www.mydomain.com/search/ 
          include&nbsp;https://search.mydomain.com/ 
          include&nbsp;regexp&nbsp;^https://www.mydomain.com/help/.*/search/ 
          include&nbsp;regexp&nbsp;^https?://[^/]*\.atomz\.com/.*[?&amp;]sp_a=sp1000130e.*$ 
          exclude&nbsp;* </code> </p> <p>Si las máscaras URL del referente son las siguientes: </p> <p> <code> https://www.mydomain.com/search/searchpage.html&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://search.mydomain.com/advanced/&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/search/advanced/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          https://www.anotherdomain.com/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          blank&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscaras de direcciones IP </p> </td> 
      <td colname="col2"> <p>La primera máscara que coincide con la dirección IP determina si se permite la búsqueda, si la máscara es una máscara de inclusión. O bien, determina si se permite o no la búsqueda si la máscara es una máscara de exclusión. Si ninguna máscara coincide con la dirección IP solicitante, se incluye esa dirección IP y se permite la búsqueda. </p> <p>El siguiente ejemplo muestra cuatro máscaras de dirección IP diferentes. </p> <p> <code> include&nbsp;64.128.192.* 
          include&nbsp;192.168. 
          include&nbsp;regexp&nbsp;^209\.42\.97\.[1-5]+ 
          exclude&nbsp;* </code> </p> <p>Si las máscaras de dirección IP de referencia son las siguientes: </p> <p> <code> 64.128.192.10&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          192.168.10.127&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          209.42.97.14&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          64.128.193.10&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          192.169.10.14&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          209.42.97.68&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Permitir sólo búsquedas que utilicen HTTPS </p> </td> 
      <td colname="col2"> <p>Restringir búsquedas a HTTPS. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dirección URL a la que se deben enviar las solicitudes no permitidas </p> </td> 
      <td colname="col2"> <p> Los usuarios restringidos se redirigen a la dirección URL que introduzca aquí. Esta opción proporciona un medio para crear su propia página de error personalizada y mostrarla a los clientes a los que no se permite realizar búsquedas en el sitio. </p> <p>Si no especifica una dirección URL, se devuelve una página de error genérica cuando un usuario restringido intenta buscar en el sitio. </p> </td> 
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

## Acerca de la vista previa {#concept_DF293FD3B02C467F8842C8C21D62F294}

La cadena de consulta y los parámetros establecidos en [!DNL Preview] se utilizan cada vez que se prueba o se obtiene una vista previa de un formulario de búsqueda en el software.

<!-- 

c_about_preview.xml

 -->

See also [About Searches](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

## Configuración de valores en Vista previa {#task_CE267A0FF621474E80AB43B67B1C28D7}

Los valores de vista previa que defina se utilizan cada vez que se prueba o previsualiza un formulario de búsqueda en el software.

<!-- 

t_setting_values_in_preview.xml

 -->

**Definición de valores en Vista previa**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Preview]**.
1. En la [!DNL Preview] página, configure las opciones que desee.

   <!-- 
   
   r_preview_options.xml
   
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
      <td colname="col1"> <p>Consulta </p> </td> 
      <td colname="col2"> <p>De forma predeterminada, la cadena de consulta se establece en <span class="codeph"> * </span>, que generalmente devuelve resultados. Sin embargo, puede especificar una consulta más específica para el contenido del sitio web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetros </p> </td> 
      <td colname="col2"> <p>Los parámetros se establecen con un nombre y un valor. Puede especificar tantos parámetros adicionales como necesite. Por ejemplo, puede especificar criterios de búsqueda adicionales con los parámetros <span class="codeph"> sp_q_1 </span> y <span class="codeph"> sp_x_1 </span> . El valor del parámetro <span class="codeph"> sp_q_1=windows&amp;sp_x_1=platform </span> crea una búsqueda de vista previa que busca el valor "windows" en la etiqueta meta "platform" de las páginas buscadas, además de la consulta principal. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parámetros CGI de búsqueda back-end </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Host </p> </td> 
      <td colname="col2"> <p>Si el sitio web utiliza etiquetado de dominio privado, establezca el nombre de host adecuado para obtener una vista previa precisa de los resultados de búsqueda. </p> <p>Para obtener información sobre el etiquetado de dominios privados, póngase en contacto con el servicio de asistencia al cliente. </p> </td> 
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

## Acerca de las fuentes {#concept_FEBFEE51A3AB49F88CBA0D16E2AD6916}

El índice de búsqueda se ve como una base de datos grande del sitio web. Con suficiente información de las etiquetas meta correctas, la información se recopila y organiza, o se distribuye, en fuentes de datos. Puede enviar estas fuentes de datos a otro servicio, como un destinatario de terceros.

<!-- 

c_about_feeds.xml

 -->

Una vez que el sitio web se haya rastreado e indexado, puede generar fuentes automáticas y enviarlas a motores de búsqueda orgánicos de terceros y motores de compra. Puede crear las siguientes fuentes de flujo:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tipo de fuente </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Recommendations </p> </td> 
   <td colname="col2"> <p>Recomendaciones las fuentes proporcionan funciones de distribución de datos con Adobe Recommendations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fuente genérica </p> </td> 
   <td colname="col2"> <p>Puede implementar muchas fuentes con el tipo Fuente genérica. Se realiza una consulta de búsqueda personalizada en el índice del sitio web. Los datos se devuelven mediante plantillas de búsqueda personalizadas que utilizan el mismo lenguaje de plantilla para mostrar los resultados de la búsqueda. Este tipo de flexibilidad significa que puede enviar fuentes a muchos más proveedores, no solo a tipos de fuentes específicos. </p> <p>Puede agregar la plantilla de transporte (búsqueda) siguiendo las instrucciones del siguiente tema de ayuda: </p> <p>Consulte <a href="../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012" type="task" format="dita" scope="local"> Adición de una nueva presentación o archivo de plantilla de transporte </a>. </p> <p> Después de agregar la plantilla, edítela con las etiquetas de plantilla de búsqueda para definir qué campos de metadatos de búsqueda desea incluir, junto con su formato. </p> <p>Consulte <a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local"> Edición de una presentación o una plantilla de transporte </a>. </p> <p>Consulte <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Buscar etiquetas de plantilla </a>. </p> <p>Asegúrese de recordar el nombre del archivo de plantilla de transporte. Utilice el nombre para enlazar la fuente genérica a la plantilla cuando especifique los criterios de la fuente. </p> <p>Si ha trabajado anteriormente con otras fuentes, recuerde que debe asignar los campos de fuente a los campos de metadatos de búsqueda. Las fuentes genéricas no tienen este paso específico en el <span class="uicontrol"> asistente Crear </span> fuente. En su lugar, la plantilla especifica los metadatos y el formato de los metadatos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Comerciante de Google </p> </td> 
   <td colname="col2"> <p>El Centro de comercialización de Google permite a las personas vender productos a través de varios servicios de Google. Cuenta con un componente de distribución de datos donde puede enviar una lista de productos disponibles para la venta de forma periódica. </p> <p>Al igual que con cualquier proveedor de fuentes de terceros, el Centro de mercadotecnia de Google cuenta con estándares específicos que usted cumple antes de que considere legítima la fuente. Para obtener más información, póngase en contacto con su representante de clientes y visite la documentación de Google Merchant. A continuación se muestra un breve resumen de lo que el Centro de mercadotecnia de Google considera al validar una fuente: </p> 
    <ul id="ul_3D84D4A6A4BF4C08860F86403F8F9CD6"> 
     <li id="li_5B6516CC7BC7493B8B8E8AFB454E573F">Cada producto tiene una página de productos; una dirección URL dedicada. </li> 
     <li id="li_5A6D5AD5E1B54A94B224D19E888B5443"> Cada variante de producto tiene una entrada separada en la fuente. </li> 
     <li id="li_89748D3241B34A4493576DAC38681988"> Cada producto tiene una dirección URL de imagen, preferiblemente procedente del servidor. Las variantes de producto tienen imágenes específicas que muestran sus variaciones reales. En otras palabras, los diferentes colores de zapatos no deben compartir la misma imagen. </li> 
     <li id="li_A594AD19480F41EAA72181355F28447B"> Cada producto tiene información específica como disponibilidad, condición, descripción, categoría y precio. </li> 
     <li id="li_0955B3A6ED2746D2B7CB42DC8AB27D3A">En general, cada producto tiene un identificador único como ISBN, UPC, JAN o EAN, entre otros. </li> 
     <li id="li_2C371653F1C5471FA638F3A3818ABC17">En general, cada producto se clasifica con la taxonomía de productos de Google. </li> 
     <li id="li_6EB392A5A0BE490FAED5BC5E83228E32"> Los productos de ropa tienen campos adicionales requeridos como sexo, grupo de edad, color y tamaño. </li> 
     <li id="li_44B91FA9A95F4172A2F03F8206E9081E"> Los impuestos y el envío se especifican como una configuración de cuenta dentro del Centro de mercadotecnia de Google o producto por producto, dentro de esta fuente. </li> 
     <li id="li_71A63E9905B840C0A04F6CDAA23C9AB0"> Los productos hechos a medida y ciertos productos de ropa pueden quedar exentos de algunas de las reglas, pero debes contactar con Google para obtener permiso y detalles sobre tales exenciones. </li> 
    </ul> <p>Existen muchos detalles que rigen la validación de fuentes. Consulte la documentación de Google Merchant para obtener información sobre la administración de fuentes. Google realiza con frecuencia cambios en las especificaciones, por lo tanto consulte la documentación con frecuencia. </p> <p>La fuente asociada con Google Merchant Center se conoce con frecuencia como la fuente de búsqueda de productos de Google. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mapas de sitios de Google </p> </td> 
   <td colname="col2"> <p>Los mapas de sitios de Google le permiten influir en la forma en que Google rastrea su sitio web. Una fuente de datos sindicada, un mapa del sitio en este caso, se envía periódicamente a los mapas de sitios de Google. El mapa del sitio contiene direcciones URL accesibles a Internet y se puede asociar con cada dirección URL información específica, como la fecha de la última modificación o la prioridad de la página. Proporcionar a Google esa información puede aumentar la frecuencia y la probabilidad de que una página específica sea rastreada e indexada. En algunos casos, un mapa del sitio se utiliza para anunciar una lista de vínculos a los que su explorador no puede acceder en circunstancias normales. </p> <p>Si está interesado en crear un mapa de sitios de Google con nuestra función de fuente, póngase en contacto con su representante de clientes. Google ha puesto su servicio de Google Sitemap a disposición del público en general y proporciona documentación en su página de herramientas de Google Webmaster. </p> <p> <b>Requisitos para crear una fuente de Google Sitemap</b> </p> <p>Para crear una fuente de Google Sitemap, asegúrese de tener una cuenta de Google Webmaster Tools con Google Sitemap ya configurado. Consulte la documentación de las herramientas de Google Webmaster para configurar el mapa de sitios de Google. </p> <p>También debe determinar cómo se entregan los archivos de mapa del sitio. En general, los archivos de mapa del sitio provienen de su dominio y, específicamente, de la raíz del sitio web. El modelo sencillo es que los archivos se entreguen mediante FTP a los servidores. La otra solución es redirigir la solicitud de los archivos de mapa del sitio a la red de contenido de búsqueda y comercialización del sitio. Póngase en contacto con su representante de consultoría para coordinar y configurar la entrega de fuentes de mapa del sitio. </p> </td> 
  </tr> 
 </tbody> 
</table>

Si está interesado en las fuentes automáticas, póngase en contacto con los servicios profesionales para obtener ayuda. Cada fuente tiene requisitos estrictos en lo que respecta a la calidad de los datos y la transmisión de los archivos.

El tipo de fuente seleccionado afecta a las opciones que aparecen al crear un campo con el **[!UICONTROL Create Feed]** asistente. Cada tipo de fuente tiene diferentes formatos de datos. Asegúrese de seguir el formato de datos correcto para evitar el rechazo de una fuente por parte de un destinatario o la publicación de datos inadecuados para sus clientes. Además del formato de datos, los proveedores suelen tener una o más formas preferidas de recibir los datos. Consulte la documentación del proveedor sobre sus fuentes.

Un desafío con la creación de una fuente es la coincidencia de los datos entre la búsqueda/comercialización del sitio y la fuente. Normalmente, los datos recuperados del rastreo de índice tienen un formato incorrecto o faltan. La siguiente es una lista de preguntas que pueden ayudarle a centrarse en lo que debe buscar al crear una fuente.

* ¿Qué tipo de relación comercial tiene con el destinatario de la fuente?
* ¿Tiene que registrarse y crear una cuenta con el destinatario de la fuente?
* ¿Quién va a monitorear y cuidar los problemas que surgen con la fuente con respecto al proveedor? En general, es su responsabilidad administrar la cuenta del proveedor. Por ejemplo: Google Sitemap requiere una cuenta WebMaster y alguien para monitorear el estado del mapa del sitio.
* ¿Cuál es el formato de datos de la fuente?
* ¿Coincide el índice con la codificación de caracteres de la fuente? Los formatos de datos delimitados por tabuladores y por comas se convierten en un problema cuando los datos tienen tabuladores o comas.
* ¿Qué sucede cuando tiene fichas o comas en los datos?
* ¿Hay alguna página en el índice con datos vacíos?
* ¿Puede el destinatario de la fuente aceptar datos vacíos? Es posible que pueda resolver los datos vacíos editando los criterios de cómo el software recupera los datos.
* ¿El formato de datos se ajusta a lo que quiere el destinatario de la fuente? Por ejemplo, algunos destinatarios de fuentes son específicos sobre cómo se muestran los precios y la moneda.
* ¿Tiene el proveedor un número máximo de artículos que puede aceptar? Puede resolver este problema potencial limitando los resultados con los criterios de búsqueda.
* ¿Cómo desea el proveedor recibir la fuente? Los envíos FTP y el alojamiento HTTP son compatibles.

## Creación de una fuente {#task_63179C1FC359497483CD6CE13FD1C250}

Puede crear una o varias fuentes de datos.

<!-- 

t_creating_a_feed.xml

 -->

**Para crear una fuente**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. En la [!DNL Feeds] página, seleccione un tipo de fuente en la lista **[!UICONTROL Create Feed]** desplegable.
1. En función del tipo de fuente seleccionado, en el cuadro de [!DNL Create Feed] diálogo, defina las opciones como se identifican en cada panel del asistente.

   <!-- 
   
   r_feed_options.xml
   
   -->

   Según el tipo de fuente que esté creando o editando, las opciones disponibles difieren ligeramente.

   **Adobe Recommendations**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Panel </p> </th> 
      <th colname="col2" class="entry"> <p>Nombre del panel Asistente </p> </th> 
      <th colname="col3" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nombre de la fuente </p> </td> 
      <td colname="col3"> <p>Especifica el nombre de la fuente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Mapas de campo </p> </td> 
      <td colname="col3"> <p>Le permite asignar campos de fuente específicos del proveedor a los campos de metadatos de búsqueda y comercialización del sitio. Este paso de asignación en el asistente es importante porque permite a las fuentes correlacionar la información entre los campos del índice y los campos de los datos de las fuentes. En la mayoría de los casos, excepto en el caso de las fuentes <span class="wintitle"> genéricas </span>, las correlaciones se guardan en una plantilla de búsqueda generada dinámicamente. </p> <p>Cada fila de la tabla <span class="wintitle"> Mapas de campo </span> representa una asignación de campo. En la columna Agregar o quitar de la tabla, haga clic en <span class="uicontrol"> + </span> para agregar una nueva fila de asignación de campos; haga clic en <span class="uicontrol"> - </span> para eliminar la fila de asignación de campos seleccionada de la tabla. Para asociar un campo de fuente con los campos de metadatos de búsqueda/comercialización de un sitio, utilice las listas desplegables correspondientes para elegir los campos deseados. </p> <p> <b>Asignaciones de campos para Adobe Recommendations</b> </p> <p>La fuente de datos de Recomendaciones es un archivo CSV, columnas de datos separadas por comas. El orden de aparición de cada asignación en la tabla Mapas de campo es importante, ya que determinan el orden de las columnas en el archivo de fuente CSV. Cree las filas de asignaciones en el orden siguiente: cada fila es obligatoria: </p> <p> 
        <ol id="ol_49C739D04DD340168DC6C1F794544C35"> 
          <li id="li_A95D9C5A353746A3A0D38F200AC2EEA2"> id </li> 
          <li id="li_044763D4C7054CEB948C94590735D74F"> name </li> 
          <li id="li_832F07CA0E3F4E10A4AE30171F3E8541"> categoryId </li> 
          <li id="li_2A33FB42F7E942ED881BA1F478542C4D"> message </li> 
          <li id="li_A76E66B2366845B0B63ED5C200531ADD"> thumbnailURL </li> 
          <li id="li_518CCD5E7E404521AB8199981BA86F76"> value </li> 
          <li id="li_14A0A8FCC2B34B758E1FBB98E3F2DFB2"> pageURL </li> 
          <li id="li_36D22F1603394AF89E0C7ADB18AAAAB7"> inventory </li> 
          <li id="li_ABDB9C762BBC4F27B82FEA4425A8DDC4"> margin </li> 
        </ol> </p> <p> <b>Uso avanzado</b> </p> <p>Después de asignar los nueve primeros campos de fuente requeridos como se describe más arriba, puede crear sus propios campos personalizados. En la lista desplegable <span class="wintitle"> Campos de fuente </span> , haga clic en <span class="uicontrol"> Personalizar </span>. En el campo de texto asociado, introduzca un nombre de etiqueta personalizado para ese campo. Esta opción personalizada resulta útil si una fuente necesita campos especiales específicos del proveedor. </p> <p> <p>Nota:  Aunque las especificaciones de Fuente de recomendación establecen que cada nombre de campo debe tener el prefijo "entity", en este caso no es necesario. </p> </p> <p>También puede crear un campo de metadatos personalizado. En la lista desplegable <span class="wintitle"> Campos de metadatos </span> , haga clic en <span class="uicontrol"> Personalizar </span>. En el campo de texto asociado, introduzca un valor de campo de metadatos personalizado. El valor se inserta en la plantilla pregenerada y también se puede utilizar para insertar etiquetas de plantilla de búsqueda personalizadas. </p> <p>Consulte <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Buscar etiquetas de plantilla </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>Criterios de búsqueda </p> </td> 
      <td colname="col3"> <p>Cuando se generan los archivos de fuente, se utiliza una consulta de búsqueda para filtrar los datos. Los filtros que se utilizan para la consulta de búsqueda se definen en este panel. </p> 
        <ul id="ul_799ECF61C03A44878C7182F8B88CC3AD"> 
        <li id="li_0763F600A4FB4650ACC28BF337EB50AF"> <span class="uicontrol"> Meta-Field </span> <p>Define qué campo de metadatos desea filtrar. </p> <p> <b>Uso avanzado</b> </p> <p>Dado que el sistema de filtrado es una consulta de búsqueda estándar, puede seleccionar <span class="uicontrol"> Formulario libre </span> en la lista desplegable para introducir los parámetros de búsqueda CGI y sus valores. Se requiere el escape de URL. Se omite el argumento de búsqueda <span class="codeph"> sp_q </span> . Puede crear varias filas de cuadros de texto de forma libre. Entre cada fila, los argumentos se delimitan automáticamente con &amp;. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Buscar parámetros CGI </a>. </p> </li> 
        <li id="li_756B776902AE4A0E95524442D663343E"> <span class="uicontrol"> Criterios </span> <p>Define la operación de filtrado. La operación de filtrado seleccionada en la lista desplegable aplica el valor constante introducido en la tercera columna. </p> </li> 
        <li id="li_7ADEDB8747B241D78AC50F1AC75AE695"> <span class="uicontrol"> Valor </span> <p>Valor constante. </p> </li> 
        <li id="li_4039A9BC2F74460B83BFF662B58DAA1B"> <span class="uicontrol"> Acción </span> <p>Agrega una nueva fila de asignación de campos o elimina la fila resaltada actualmente. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Envío de archivo </p> </td> 
      <td colname="col3"> <p>Permite configurar la programación para enviar los archivos de fuente y establecer el método que desea utilizar para cargar los archivos. </p> 
        <ul id="ul_55E253F83BDA46BAABF2BE38F0918E80"> 
        <li id="li_877A376B5B30422FAC816E31D50EA508"> <span class="uicontrol"> Programa </span> <p>Define la frecuencia máxima con la que se envía una fuente. Al seleccionar <span class="uicontrol"> Nunca </span> se desactiva la fuente. Otros valores definen el período que espera la fuente antes de volver a enviarla. La decisión de cuándo enviar la fuente se toma en cada índice. En otras palabras, al final del índice, se comprueba una fuente para ver si ha caducado y debe actualizarla y enviarla el proveedor. Además, se utiliza como método para evitar que una cuenta se envíe en exceso a un proveedor. Algunos proveedores tienen directivas contra fuentes de fuentes de datos que se cargan con demasiada frecuencia. Asegúrese de comprobar la directiva del proveedor de fuentes de datos sobre la frecuencia de los envíos. 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--ick <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_760F5068D3ED46C582AE41392A2CA342"> <span class="uicontrol"> Cargar método </span> <p>La mayoría de las fuentes tiene dos formas de distribuir los archivos: FTP y red de contenido alojado. </p> 
          <ul id="ul_666759EDDD034537AA7C0ED936A2F315"> 
          <li id="li_B4AD5CEEBB7B41C0B8DC291B95DC5F83"> <span class="uicontrol"> FTP </span> <p>Los servidores de búsqueda y comercialización del sitio utilizan FTP pasivo. </p> <p>FTP es la única manera de insertar un archivo en otro servidor. </p> <p> <span class="uicontrol"> Servidor FTP </span> : especifica el nombre del servidor FTP. No incluya el protocolo ni preceda a "ftp://". </p> <p> <span class="uicontrol"> Nombre de usuario de FTP </span> : especifica el nombre de la cuenta de FTP. </p> <p> <span class="uicontrol"> Contraseña de FTP </span> : especifica la contraseña de la cuenta de FTP. </p> <p> <span class="uicontrol"> Nombre de archivo FTP </span> : especifica el nombre del archivo que se va a transmitir. Este nombre es una plantilla si la fuente genera varios archivos, lo que generalmente incrementa un número al final del nombre pero antes de la extensión. Por ejemplo: basename.xml, basename1.xml, basename2.xml, ... , basename-Nth.xml </p> <p> <span class="uicontrol"> Directorio FTP </span> : si se requiere una ruta de directorio específica, debe escribirla aquí. No incluya el nombre de archivo en la ruta. </p> </li> 
          <li id="li_C082D3993C6C469B9067F207703BE619"> <span class="uicontrol"> Red de contenido alojado </span> <p>La red de contenido es el medio de proporcionar archivos desde los servidores Web de búsqueda/comercialización del sitio. El destinatario de la fuente la extrae de los servidores web mediante una solicitud HTTP. La única información para configurarlo es el nombre del archivo de red de <span class="uicontrol"> contenido </span>. El nombre del archivo es el nombre base del archivo que se proporciona. Utilice sólo nombres de archivo con una extensión de nombre de archivo. Según la fuente, el nombre de archivo es una plantilla para varios archivos en la que la fuente puede generar varios archivos con el siguiente formato: basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml. </p> <p>Una vez introducido el nombre de archivo base y guardada correctamente la fuente, la dirección URL del archivo de red de contenido se muestra en el panel Verificación del asistente. La dirección URL se activa después de que la fuente se haya procesado correctamente. El proveedor puede obtener los datos de la fuente desde esta dirección URL. Varios archivos utilizan la misma ruta de URL. Sin embargo, asegúrese de reemplazar o cambiar el nombre de archivo según el esquema de enumeración. </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>Verificación </p> </td> 
      <td colname="col3"> <p>Al acceder al panel <span class="wintitle"> Verificación </span> , la fuente se guarda en ese momento. Sin embargo, los archivos de fuente reales no se guardan hasta más tarde. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_0C6EFB38E06F401696084863D85CBD0D"> 
        <li id="li_07FC9F04C7F640048546F9DC5D91DA1D"> <span class="uicontrol"> Vista de datos </span> <p>Permite hacer clic en el vínculo para comprobar el resultado de la fuente mediante una vista de datos que se muestra en el formulario de tabla. La vista de datos también puede ayudarle a solucionar los problemas al mostrarle qué campos meta se seleccionan y cómo cualquier criterio de búsqueda especificado del panel Criterios de <span class="wintitle"> búsqueda </span> del asistente afecta la salida de la fuente. La vista de datos se genera de forma dinámica, por lo que está disponible en todo momento. </p> </li> 
        <li id="li_67046A56D08C48298E5A3E1F9C4A8AF3"> <span class="uicontrol"> Archivos de fuente </span> <p>Después de que los servidores de búsqueda y comercialización del sitio generen los archivos de fuente, puede utilizar la lista desplegable <span class="uicontrol"> Archivos de fuente </span> para ver los archivos de los servidores. Aparece una nueva ficha del navegador o una nueva ventana del navegador con el contenido de la fuente. Este método es útil para ayudarle a solucionar problemas de fuentes con problemas de formato. Tenga en cuenta que no ve los archivos desde el destino final ni desde los propios proveedores. </p> <p> Si la fuente es nueva, la lista desplegable estará vacía hasta que genere archivos de fuente. </p> </li> 
        <li id="li_99D66C7AD87A475CB3D831D514DB78A0"> <span class="uicontrol"> Vínculo de red de contenido </span> <p>Si ha seleccionado <span class="uicontrol"> Red de contenido alojado </span> como método de carga en el panel Envío de <span class="wintitle"> archivos </span> del asistente, la URL se mostrará aquí. Si todavía no ha generado ningún archivo de fuente, la dirección URL no será válida hasta que la fuente se genere correctamente. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Fuente genérica**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Panel </p> </th> 
      <th colname="col2" class="entry"> <p>Nombre del panel Asistente </p> </th> 
      <th colname="col3" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nombre de la fuente </p> </td> 
      <td colname="col3"> <p>Especifica el nombre de la fuente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Criterios de búsqueda </p> </td> 
      <td colname="col3"> <p>Cuando se generan los archivos de fuente, se utiliza una consulta de búsqueda para filtrar los datos. Los filtros que se utilizan para la consulta de búsqueda se definen en este panel. </p> 
        <ul id="ul_C750687E69A647D0A4440FF1B6CC7E05"> 
        <li id="li_B5C3B8523D71472E9508A04E23AC0211"> <span class="uicontrol"> Meta-Field </span> <p>Define qué campo de metadatos desea filtrar. </p> <p> <b>Uso avanzado</b> </p> <p>Dado que el sistema de filtrado es una consulta de búsqueda estándar, puede seleccionar <span class="uicontrol"> Formulario libre </span> en la lista desplegable para introducir los parámetros de búsqueda CGI y sus valores. Se requiere el escape de URL. Se omite el argumento de búsqueda <span class="codeph"> sp_q </span> . Puede crear varias filas de cuadros de texto de forma libre. Entre cada fila, los argumentos se delimitan automáticamente con &amp;. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Buscar parámetros CGI </a>. </p> </li> 
        <li id="li_D1E49834BBEA42CC8C49AE7D72037C53"> <span class="uicontrol"> Criterios </span> <p>Define la operación de filtrado. La operación de filtrado seleccionada en la lista desplegable aplica el valor constante introducido en la tercera columna. </p> </li> 
        <li id="li_D5F0651B834F4EACAD15A2D154A0737B"> <span class="uicontrol"> Valor </span> <p>Valor constante. </p> </li> 
        <li id="li_FC8F382BD20C4518BC2230D4B4954591"> <span class="uicontrol"> Acción </span> <p>Agrega una nueva fila de asignación de campos o elimina la fila resaltada actualmente. </p> </li> 
        </ul> <p>Las fuentes genéricas necesitan especificar un parámetro CGI especial. Para enlazar la plantilla especial asociada con esta fuente, debe definir el parámetro <span class="codeph"> sp_t </span> . Establezca el valor de <span class="codeph"> sp_t </span> en el nombre del archivo de plantilla de transporte. Por ejemplo, si ha agregado un archivo de plantilla de transporte denominado <span class="codeph"> super_feed.tpl </span>, cree un parámetro de búsqueda CGI personalizado como <span class="codeph"> sp_t=super_feed </span>. El cuadro de texto para introducir <span class="codeph"> sp_t </span> no aparece hasta que se selecciona <span class="uicontrol"> Forma libre </span> en la lista desplegable <span class="wintitle"> Campo </span> meta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>Envío de archivo </p> </td> 
      <td colname="col3"> <p>Permite configurar la programación para enviar los archivos de fuente y establecer el método que desea utilizar para cargar los archivos. </p> 
        <ul id="ul_30E830C41F6A4526822AF1FD3083075A"> 
        <li id="li_79EAFDBD2B9F411EA985CAEC1BAF3926"> <span class="uicontrol"> Programa </span> <p>Define la frecuencia máxima con la que se envía una fuente. Al seleccionar <span class="uicontrol"> Nunca </span> se desactiva la fuente. Otros valores definen el período que espera la fuente antes de volver a enviarla. La decisión de cuándo enviar la fuente se toma en cada índice. En otras palabras, al final del índice, se comprueba una fuente para ver si ha caducado y debe actualizarla y enviarla el proveedor. Además, se utiliza como método para evitar que una cuenta se envíe en exceso a un proveedor. Algunos proveedores tienen directivas contra fuentes de fuentes de datos que se cargan con demasiada frecuencia. Asegúrese de comprobar la directiva del proveedor de fuentes sobre la frecuencia de los envíos. 
          <!--he time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--<uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_20BF70A19E7E45BA91CD972E2FCE0EA4"> <span class="uicontrol"> Cargar método </span> <p>La mayoría de las fuentes tiene dos formas de distribuir los archivos: FTP y red de contenido alojado. </p> 
          <ul id="ul_5888C2E9097645CE89938EE09F8CB4F1"> 
          <li id="li_EA9ED19F3BEA4BEAB1A9F2C2FAFF85F7"> <span class="uicontrol"> FTP </span> <p>Los servidores de búsqueda y comercialización del sitio utilizan FTP pasivo. </p> <p>FTP es la única manera de insertar un archivo en otro servidor. </p> <p> <span class="uicontrol"> Servidor FTP </span> : especifica el nombre del servidor FTP. No incluya el protocolo ni preceda a "ftp://". </p> <p> <span class="uicontrol"> Nombre de usuario de FTP </span> : especifica el nombre de la cuenta de FTP. </p> <p> <span class="uicontrol"> Contraseña de FTP </span> : especifica la contraseña de la cuenta de FTP. </p> <p> <span class="uicontrol"> Nombre de archivo FTP </span> : especifica el nombre del archivo que se va a transmitir. Este nombre es una plantilla si la fuente genera varios archivos, lo que generalmente incrementa un número al final del nombre pero antes de la extensión. Por ejemplo: basename.xml, basename1.xml, basename2.xml, ... , basename-Nth.xml </p> <p> <span class="uicontrol"> Directorio FTP </span> : si se requiere una ruta de directorio específica, debe escribirla aquí. No incluya el nombre de archivo en la ruta. </p> </li> 
          <li id="li_181268A7EE40456CA1DB768E8C66EEB9"> <span class="uicontrol"> Red de contenido alojado </span> <p>La red de contenido alojado es el medio de servir archivos de los servidores Web de búsqueda/comercialización del sitio. El destinatario de la fuente la extrae de los servidores web mediante una solicitud HTTP. La única información para configurarlo es el nombre del archivo de red de <span class="uicontrol"> contenido </span>. El nombre del archivo es el nombre base del archivo que se proporciona. Utilice sólo nombres de archivo con una extensión de nombre de archivo. 
            <!--Depending on the feed, the file name is a template for multiple files where the feed might generate multiple files in the following format: basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml. --> </p> <p>Una vez introducido el nombre de archivo base y guardada correctamente la fuente, la dirección URL del archivo de red de contenido se muestra en el panel Verificación del asistente. La dirección URL se activa después de que la fuente se haya procesado correctamente. El proveedor puede obtener los datos de la fuente desde esta dirección URL. </p> </li> 
          </ul> </li> 
        <li id="li_4DF56FA607A7479296CDA042A63C5A2C"> <p> <b>¿Conservar fichas?</b> </p> <p>Mantener caracteres de tabulación en la fuente. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Verificación </p> </td> 
      <td colname="col3"> <p>Al acceder al panel <span class="wintitle"> Verificación </span> , la fuente se guarda en ese momento. Sin embargo, los archivos de fuente reales no se guardan hasta más tarde. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_7420C415987448A796DD979CF5FA2EB6"> 
        <li id="li_AF02E8609B7B4F20A01AF4E010308E15"> <span class="uicontrol"> Vista de datos </span> <p>Permite hacer clic en el vínculo para comprobar el resultado de la fuente mediante una vista de datos que se muestra en el formulario de tabla. La vista de datos también puede ayudarle a solucionar los problemas al mostrarle qué campos meta se seleccionan y cómo cualquier criterio de búsqueda especificado del panel Criterios de <span class="wintitle"> búsqueda </span> del asistente afecta la salida de la fuente. La vista de datos se genera de forma dinámica, por lo que está disponible en todo momento. </p> </li> 
        <li id="li_32CEB8885C184354BFA1773BA66DB7A7"> <span class="uicontrol"> Archivos de fuente </span> <p>Después de que los servidores de búsqueda y comercialización del sitio generen los archivos de fuente, puede utilizar la lista desplegable <span class="uicontrol"> Archivos de fuente </span> para ver los archivos de los servidores. Aparece una nueva ficha del navegador o una nueva ventana del navegador con el contenido de la fuente. Este método es útil para ayudarle a solucionar problemas de fuentes con problemas de formato. Tenga en cuenta que no ve los archivos desde el destino final ni desde los propios proveedores. </p> <p> Si la fuente es nueva, la lista desplegable estará vacía hasta que genere archivos de fuente. </p> </li> 
        <li id="li_8D1B876B0EC2455C8654EC573EC53FA9"> <span class="uicontrol"> Vínculo de red de contenido </span> <p>Si ha seleccionado <span class="uicontrol"> Red de contenido alojado </span> como método de carga en el panel Envío de <span class="wintitle"> archivos </span> del asistente, la URL se mostrará aquí. Si todavía no ha generado ningún archivo de fuente, la dirección URL no será válida hasta que la fuente se genere correctamente. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Centro de comercialización de Google**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Panel </p> </th> 
      <th colname="col2" class="entry"> <p>Nombre del panel Asistente </p> </th> 
      <th colname="col3" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nombre de la fuente </p> </td> 
      <td colname="col3"> <p>Especifica el nombre de la fuente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Mapas de campo </p> </td> 
      <td colname="col3"> <p>Le permite asignar campos de fuente específicos del proveedor a los campos de metadatos de búsqueda y comercialización del sitio. Este paso de asignación en el asistente es importante porque permite a las fuentes correlacionar la información entre los campos del índice y los campos de los datos de las fuentes. En la mayoría de los casos, excepto en el caso de las fuentes <span class="wintitle"> genéricas </span>, las correlaciones se guardan en una plantilla de búsqueda generada dinámicamente. </p> <p>Cada fila de la tabla Mapas de campo representa una asignación de campo. En la columna <span class="wintitle"> Agregar o quitar </span> de la tabla, haga clic en <span class="uicontrol"> + </span> para agregar una nueva fila de asignación de campos; haga clic en <span class="uicontrol"> - </span> para eliminar la fila de asignación de campos seleccionada de la tabla. Para asociar un campo de fuente con un campo de metadatos de búsqueda o comercialización del sitio, utilice las listas desplegables correspondientes para elegir los campos deseados. </p> <p> <b>Uso avanzado</b> </p> <p>Puede crear sus propios campos personalizados. En la lista desplegable <span class="wintitle"> Campos de fuente </span> , haga clic en <span class="uicontrol"> Personalizar </span>. En el campo de texto asociado, introduzca un nombre de etiqueta personalizado para ese campo. Esta opción personalizada resulta útil si una fuente necesita campos especiales específicos del proveedor. </p> <p>También puede crear un campo de metadatos personalizado. En la lista desplegable <span class="wintitle"> Campos de metadatos </span> , haga clic en <span class="uicontrol"> Personalizar </span>. En el campo de texto asociado, introduzca un valor de campo de metadatos personalizado. El valor se inserta en la plantilla pregenerada y también se puede utilizar para insertar etiquetas de plantilla de búsqueda personalizadas. </p> <p>Consulte <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Buscar etiquetas de plantilla </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>Criterios de búsqueda </p> </td> 
      <td colname="col3"> <p>Cuando se generan los archivos de fuente, se utiliza una consulta de búsqueda para filtrar los datos. Los filtros que se utilizan para la consulta de búsqueda se definen en este panel. </p> 
        <ul id="ul_8179321A58BB4C72B0CDB2B2BEC58FE4"> 
        <li id="li_9F8008A2398A4667B106BC49C94E5E3E"> <span class="uicontrol"> Meta-Field </span> <p>Define qué campo de metadatos desea filtrar. </p> <p> <b>Uso avanzado</b> </p> <p>Dado que el sistema de filtrado es una consulta de búsqueda estándar, puede seleccionar <span class="uicontrol"> Formulario libre </span> en la lista desplegable para introducir los parámetros de búsqueda CGI y sus valores. Se requiere el escape de URL. Se omite el argumento de búsqueda <span class="codeph"> sp_q </span> . Puede crear varias filas de cuadros de texto de forma libre. Entre cada fila, los argumentos se delimitan automáticamente con &amp;. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Buscar parámetros CGI </a>. </p> </li> 
        <li id="li_50C9CE59E9E5418895F8C1A070560063"> <span class="uicontrol"> Criterios </span> <p>Define la operación de filtrado. La operación de filtrado seleccionada en la lista desplegable aplica el valor constante introducido en la tercera columna. </p> </li> 
        <li id="li_9F86D0F5010046A4A9F93DBA5FB158B3"> <span class="uicontrol"> Valor </span> <p>Valor constante. </p> </li> 
        <li id="li_1051AFD5AEA447D0AF5FAB305E1D1E64"> <span class="uicontrol"> Acción </span> <p>Agrega una nueva fila de asignación de campos o elimina la fila resaltada actualmente. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Envío de archivo </p> </td> 
      <td colname="col3"> <p>Permite configurar la programación para enviar los archivos de fuente y establecer el método que desea utilizar para cargar los archivos. </p> 
        <ul id="ul_A6A3C333AADD4438B835BF3E16E2AEFF"> 
        <li id="li_FCC4DAF198E149278B5CFB870CB6218C"> <span class="uicontrol"> Programa </span> <p>Define la frecuencia máxima con la que se envía una fuente. Al seleccionar <span class="uicontrol"> Nunca </span> se desactiva la fuente. Otros valores definen el período que espera la fuente antes de volver a enviarla. La decisión de cuándo enviar la fuente se toma en cada índice. En otras palabras, al final del índice, se comprueba una fuente para ver si ha caducado y debe actualizarla y enviarla el proveedor. Además, se utiliza como método para evitar que una cuenta se envíe en exceso a un proveedor. Algunos proveedores tienen directivas contra fuentes de fuentes de datos que se cargan con demasiada frecuencia. Asegúrese de comprobar la directiva del proveedor de fuentes sobre la frecuencia de los envíos. </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_2D9ECAFB8E8544D39B486F7BC3DCE589"> <span class="uicontrol"> Cargar método </span> <p>La mayoría de las fuentes tiene dos formas de distribuir los archivos: FTP y red de contenido alojado. </p> <p>El método de carga recomendado para enviar la fuente de datos es <span class="uicontrol"> FTP </span>. Google Merchant Center aloja un servidor FTP con este fin. Consulte la Ayuda de Google Merchant Center para obtener información sobre la configuración de una cuenta FTP de Google para esta fuente de búsqueda de productos de Google. </p> 
          <ul id="ul_BC0D8B541068407883CAC948496DBD0A"> 
          <li id="li_DB28CA23C94A4AF09E1A0EB06DF8F40C"> <span class="uicontrol"> FTP </span> <p>Los servidores de búsqueda y comercialización del sitio utilizan FTP pasivo. </p> <p>FTP es la única manera de insertar un archivo en otro servidor. </p> <p> <span class="uicontrol"> Servidor FTP </span> : especifica el nombre del servidor FTP. En este caso, es 
            <userinput>
              cargas.google.com 
            </userinput>. No incluya el protocolo ni preceda a "ftp://". </p> <p> <span class="uicontrol"> Nombre de usuario de FTP </span> : especifica el nombre de la cuenta de FTP. </p> <p> <span class="uicontrol"> Contraseña de FTP </span> : especifica la contraseña de la cuenta de FTP. </p> <p> <span class="uicontrol"> Nombre de archivo FTP </span> : especifica el nombre del archivo que se va a transmitir. Este nombre es una plantilla si la fuente genera varios archivos, lo que generalmente incrementa un número al final del nombre pero antes de la extensión. Por ejemplo: basename.xml, basename1.xml, basename2.xml, ... , basename-Nth.xml </p> <p> <span class="uicontrol"> Directorio FTP </span> : si se requiere una ruta de directorio específica, debe escribirla aquí. No incluya el nombre de archivo en la ruta. </p> </li> 
          <li id="li_5990927146434DAF89273F4636D21437"> <span class="uicontrol"> Red de contenido alojado </span> <p>La red de contenido es el medio de proporcionar archivos desde los servidores Web de búsqueda/comercialización del sitio. El destinatario de la fuente la extrae de los servidores web mediante una solicitud HTTP. </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>Verificación </p> </td> 
      <td colname="col3"> <p>Al acceder al panel <span class="wintitle"> Verificación </span> , la fuente se guarda en ese momento. Sin embargo, los archivos de fuente reales no se guardan hasta más tarde. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_4A94355A8DF840A3BAF6BD5E9F11C27F"> 
        <li id="li_825697CB36B34C4AB5959B15EDDB55F1"> <span class="uicontrol"> Vista de datos </span> <p>Permite hacer clic en el vínculo para comprobar el resultado de la fuente mediante una vista de datos que se muestra en el formulario de tabla. La vista de datos también puede ayudarle a solucionar los problemas al mostrarle qué campos meta se seleccionan y cómo cualquier criterio de búsqueda especificado del panel Criterios de <span class="wintitle"> búsqueda </span> del asistente afecta la salida de la fuente. La vista de datos se genera de forma dinámica, por lo que está disponible en todo momento. </p> </li> 
        <li id="li_91B8B5F5F9DE4A13863CD62F74AA6206"> <span class="uicontrol"> Archivos de fuente </span> <p>Después de que los servidores de búsqueda y comercialización del sitio generen los archivos de fuente, puede utilizar la lista desplegable <span class="uicontrol"> Archivos de fuente </span> para ver los archivos de los servidores. Aparece una nueva ficha del navegador o una nueva ventana del navegador con el contenido de la fuente. Este método es útil para ayudarle a solucionar problemas de fuentes con problemas de formato. Tenga en cuenta que no ve los archivos desde el destino final ni desde los propios proveedores. </p> <p> Si la fuente es nueva, la lista desplegable estará vacía hasta que genere archivos de fuente. </p> </li> 
        <li id="li_4A5EC089628E43029A38F8919888FF0A"> <span class="uicontrol"> Vínculo de red de contenido </span> <p>Si ha seleccionado <span class="uicontrol"> Red de contenido alojado </span> como método de carga en el panel Envío de <span class="wintitle"> archivos </span> del asistente, la URL se mostrará aquí. Si todavía no ha generado ningún archivo de fuente, la dirección URL no será válida hasta que la fuente se genere correctamente. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Mapas de sitios de Google**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Panel </p> </th> 
      <th colname="col2" class="entry"> <p>Nombre del panel Asistente </p> </th> 
      <th colname="col3" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nombre de la fuente </p> </td> 
      <td colname="col3"> <p>Especifica el nombre de la fuente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Mapas de campo </p> </td> 
      <td colname="col3"> <p>Le permite asignar campos de fuente específicos del proveedor a los campos de metadatos de búsqueda y comercialización del sitio. Este paso de asignación en el asistente es importante porque permite a las fuentes correlacionar la información entre los campos del índice y los campos de los datos de las fuentes. En la mayoría de los casos, excepto en el caso de las fuentes <span class="wintitle"> genéricas </span>, las correlaciones se guardan en una plantilla de búsqueda generada dinámicamente. </p> <p>Cada fila de la tabla Mapas de campo representa una asignación de campo. En la columna Agregar o quitar de la tabla, haga clic en <span class="uicontrol"> + </span> para agregar una nueva fila de asignación de campos; haga clic en <span class="uicontrol"> - </span> para eliminar la fila de asignación de campos seleccionada de la tabla. Para asociar un campo de fuente con un campo de metadatos, utilice las listas desplegables correspondientes para elegir los campos deseados. </p> <p> <b>Uso avanzado</b> </p> <p>Puede crear sus propios campos personalizados. En la lista desplegable <span class="wintitle"> Campos de fuente </span> , haga clic en <span class="uicontrol"> Personalizar </span>. En el campo de texto asociado, introduzca un nombre de etiqueta personalizado para ese campo. Esta opción personalizada resulta útil si una fuente necesita campos especiales específicos del proveedor. </p> <p>También puede crear un campo de metadatos personalizado. En la lista desplegable <span class="wintitle"> Campos de metadatos </span> , haga clic en <span class="uicontrol"> Personalizar </span>. En el campo de texto asociado, introduzca un valor de campo de metadatos personalizado. El valor se inserta en la plantilla pregenerada y también se puede utilizar para insertar etiquetas de plantilla de búsqueda personalizadas. </p> <p>Consulte <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Buscar etiquetas de plantilla </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>Criterios de búsqueda </p> </td> 
      <td colname="col3"> <p>Cuando se generan los archivos de fuente, se utiliza una consulta de búsqueda para filtrar los datos. Los filtros que se utilizan para la consulta de búsqueda se definen en este panel. </p> 
        <ul id="ul_994585E89A044BD3A89A99D30F277432"> 
        <li id="li_61FA9246B9824E3C8124958C8EBFF0DA"> <span class="uicontrol"> Meta-Field </span> <p>Define qué campo de metadatos desea filtrar. </p> <p> <b>Uso avanzado</b> </p> <p>Dado que el sistema de filtrado es una consulta de búsqueda estándar, puede seleccionar <span class="uicontrol"> Formulario libre </span> en la lista desplegable para introducir los parámetros de búsqueda CGI y sus valores. Se requiere el escape de URL. Se omite el argumento de búsqueda <span class="codeph"> sp_q </span> . Puede crear varias filas de cuadros de texto de forma libre. Entre cada fila, los argumentos se delimitan automáticamente con &amp;. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Buscar parámetros CGI </a>. </p> </li> 
        <li id="li_A5D00883738845C8B8F612A7521F160F"> <span class="uicontrol"> Criterios </span> <p>Define la operación de filtrado. La operación de filtrado seleccionada en la lista desplegable aplica el valor constante introducido en la tercera columna. </p> </li> 
        <li id="li_5A312C2984454C2CB518CA453AD9F6D2"> <span class="uicontrol"> Valor </span> <p>Valor constante. </p> </li> 
        <li id="li_666AAE1BC7A2432E91953B08EC7394DC"> <span class="uicontrol"> Acción </span> <p>Agrega una nueva fila de asignación de campos o elimina la fila resaltada actualmente. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Envío de archivo </p> </td> 
      <td colname="col3"> <p>Permite configurar la programación para enviar los archivos de fuente y establecer el método que desea utilizar para cargar los archivos. </p> 
        <ul id="ul_49B3255BE669424B925BBAEE4C9B385F"> 
        <li id="li_939828C774D440EBB0769F6D5B0BBA23"> <span class="uicontrol"> Programa </span> <p>Define la frecuencia máxima con la que se envía una fuente. Al seleccionar <span class="uicontrol"> Nunca </span> se desactiva la fuente. Otros valores definen el período que espera la fuente antes de volver a enviarla. La decisión de cuándo enviar la fuente se toma en cada índice. En otras palabras, al final del índice, se comprueba una fuente para ver si ha caducado y debe actualizarla y enviarla el proveedor. Además, se utiliza como método para evitar que una cuenta se envíe en exceso a un proveedor. Algunos proveedores tienen directivas contra fuentes de fuentes de datos que se cargan con demasiada frecuencia. Asegúrese de comprobar la directiva del proveedor de fuentes sobre la frecuencia de los envíos. </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_07B5BCF7936241A7915C4898B231184B"> <span class="uicontrol"> Cargar método </span> <p>La mayoría de las fuentes tiene dos formas de distribuir los archivos: FTP y red de contenido alojado. </p> 
          <ul id="ul_74FA98A82754469BA5FADCC63FC364F7"> 
          <li id="li_02940B712D6444A8B65C0A51834187E6"> <span class="uicontrol"> FTP </span> <p>Los servidores de búsqueda y comercialización del sitio utilizan FTP pasivo. </p> <p>FTP es la única manera de insertar un archivo en otro servidor. </p> <p> <span class="uicontrol"> Servidor FTP </span> : especifica el nombre del servidor FTP. No incluya el protocolo ni preceda a "ftp://". </p> <p> <span class="uicontrol"> Nombre de usuario de FTP </span> : especifica el nombre de la cuenta de FTP. </p> <p> <span class="uicontrol"> Contraseña de FTP </span> : especifica la contraseña de la cuenta de FTP. </p> <p> <span class="uicontrol"> Nombre de archivo FTP </span> : especifica el nombre del archivo que se va a transmitir. Este nombre es una plantilla si la fuente genera varios archivos, lo que generalmente incrementa un número al final del nombre pero antes de la extensión. Por ejemplo: basename.xml, basename1.xml, basename2.xml, ... , basename-Nth.xml </p> <p> <span class="uicontrol"> Directorio FTP </span> : si se requiere una ruta de directorio específica, debe escribirla aquí. No incluya el nombre de archivo en la ruta. </p> </li> 
          <li id="li_EAE504436CD84452BA04BE51855A2BEF"> <span class="uicontrol"> Red de contenido alojado </span> <p>La red de contenido es la manera de proporcionar archivos desde los servidores Web de búsqueda/comercialización del sitio. El destinatario de la fuente la extrae de los servidores web mediante una solicitud HTTP. </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> <p>Tenga en cuenta que cualquier método de carga requiere que especifique la URL que Google utiliza para recuperar el mapa del sitio, en el campo URL del <span class="wintitle"> mapa del sitio principal </span> . Aquí también se determina el nombre del archivo de mapa del sitio. Si el mapa del sitio es grande, es posible que existan varios archivos y la convención de nombres sea adjuntar un número de índice al final del archivo, comenzando por el número 1. El primer archivo o archivo de índice no tiene índice, como en <span class="codeph"> sitemap.xml </span>, <span class="codeph"> sitemap1.xml </span>, <span class="codeph"> sitemap2.xml </span> ... <span class="codeph"> sitemap12.xml </span>. </p> <p>Si elige <span class="uicontrol"> Red de contenido alojado </span> como método de carga, la dirección URL de los archivos tiene los mismos nombres de archivo, pero la dirección URL tiene la ruta y el nombre de host del servicio de alojamiento. Por lo tanto, las solicitudes para el mapa del sitio se redirigen a la red de contenido alojado. También debería poder extraer los archivos de la misma ubicación. </p> <p>Una vez creados y enviados los archivos de fuente al destino intermedio, Google se hace ping y les informa de que la fuente de mapa del sitio está lista. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>Verificación </p> </td> 
      <td colname="col3"> <p>Al acceder al panel <span class="wintitle"> Verificación </span> , la fuente se guarda en ese momento. Sin embargo, los archivos de fuente reales no se guardan hasta más tarde. </p> <p>The <span class="wintitle"> Verification </span> panel lets you do the following: </p> 
        <ul id="ul_A1D889A84972419599FC83F39EA2676A"> 
        <li id="li_C8ED077B6DD1461E85A4914C1CFDBE88"> <span class="uicontrol"> Vista de datos </span> <p>Permite hacer clic en el vínculo para comprobar el resultado de la fuente mediante una vista de datos que se muestra en el formulario de tabla. La vista de datos también puede ayudarle a solucionar los problemas al mostrarle qué campos meta se seleccionan y cómo cualquier criterio de búsqueda especificado del panel Criterios de <span class="wintitle"> búsqueda </span> del asistente afecta la salida de la fuente. La vista de datos se genera de forma dinámica, por lo que está disponible en todo momento. </p> </li> 
        <li id="li_DACEE40703AF40EFBCD90D43825CE9C1"> <span class="uicontrol"> Archivos de fuente </span> <p>Una vez generados los archivos de fuente, puede utilizar la lista desplegable <span class="uicontrol"> Archivos de fuente </span> para ver los archivos de los servidores. Aparece una nueva ficha del navegador o una nueva ventana del navegador con el contenido de la fuente. Este método es útil para ayudarle a solucionar problemas de fuentes con problemas de formato. Tenga en cuenta que no ve los archivos del destino final ni de los propios proveedores. </p> <p> Si la fuente es nueva, la lista desplegable estará vacía hasta que genere archivos de fuente. </p> </li> 
        <li id="li_1C530354B4F34EC79D92CEFEB5B39ED7"> <span class="uicontrol"> Vínculo de red de contenido </span> <p>Si ha seleccionado <span class="uicontrol"> Red de contenido alojado </span> como método de carga en el panel Envío de <span class="wintitle"> archivos </span> del asistente, la URL se mostrará aquí. Si todavía no ha generado ningún archivo de fuente, la dirección URL no será válida hasta que la fuente se genere correctamente. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cuando complete los pasos del asistente, haga clic en **[!UICONTROL Close]**.

## Edición de una fuente {#task_B855D28CD99B4FA58E2D4D4FD6DC9CEB}

Puede editar la configuración de una fuente existente.

<!-- 

t_editing_a_feed.xml

 -->

>[!NOTE]
>
>Cuando se edita una fuente, no se puede cambiar el tipo. Si necesita cambiar el tipo de fuente, elimine la fuente existente y, a continuación, agregue una fuente nueva con el tipo que desee.

Consulte [Eliminación de una fuente](../c-about-settings-menu/c-about-searching-menu.md#task_7E39A140E69D43C6B61FB42E81051269).

**Para editar una fuente**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Realice uno de los siguientes pasos:

* En la [!DNL Feeds] página, en la [!DNL Name] columna de la tabla, haga clic en la lista desplegable situada junto al nombre de una fuente y, a continuación, haga clic en **[!UICONTROL Edit feed]**.

* En la [!DNL Feeds] página, debajo de la [!DNL Name] columna, haga clic en el nombre de una fuente que desee cambiar.

1. En el asistente de la fuente, defina las opciones que desee para cada panel del asistente.

   Consulte las tablas de opciones en **Adición de una fuente**.
1. Al final del asistente, en el [!DNL Verification] panel, haga clic en **[!UICONTROL Close]**.

## Eliminación de una fuente {#task_7E39A140E69D43C6B61FB42E81051269}

Puede eliminar una fuente que ya no necesite ni use.

<!-- 

t_deleting_a_feed.xml

 -->

**Para eliminar una fuente**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. En la [!DNL Feeds Menu] pantalla, en la [!DNL Actions] columna, haga clic en **[!UICONTROL Delete]** para el nombre de la fuente que desee eliminar.
1. En el cuadro de diálogo [!DNL Delete feed] , haga clic en **[!UICONTROL Yes]** para confirmar la eliminación.

## Visualización de archivos de fuente {#task_1E413C7650DE466EA68925F72E086884}

Puede ir al último panel del asistente de fuentes para acceder rápidamente a la vista de datos de la fuente o para descargar los archivos de fuentes actuales del servidor. Esta funcionalidad es útil si desea verificar y examinar la salida de la fuente.

<!-- 

t_viewing_feed_files.xml

 -->

**Para ver los archivos de fuente**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. En la [!DNL Feeds] página, en la [!DNL Name] columna de la tabla, haga clic en la lista desplegable situada junto al nombre de una fuente y, a continuación, haga clic en **[!UICONTROL View Feed Files]**.
1. En el [!DNL Verification] panel del asistente de la fuente, haga clic en **[!UICONTROL Show Data View]**.
1. Haga clic **[!UICONTROL Close]**.

## Prueba de una fuente sin carga de archivos {#task_F1F390F72E0A4886B6CD4CD86EDB4C8C}

Puede probar una fuente sin cargar archivos en el destino final.

<!-- 

t_testing_a_feed_with_no_file_upload.xml

 -->

**Prueba de una fuente sin carga de archivos**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. En la [!DNL Feeds] página, en la [!DNL Name] columna de la tabla, haga clic en la lista desplegable situada junto al nombre de una fuente y, a continuación, haga clic en **[!UICONTROL Test Feed (No file upload)]**.
1. En la [!DNL Feeds] página, la [!DNL Feed Status] columna se actualiza durante y después de la prueba.

## Generación y carga de una fuente {#task_C9A57827C7674035B62A22D310DDAA0C}

Puede generar y enviar archivos de fuente manualmente al destino final, independientemente de la programación que haya definido en el panel [!DNL File Submission] del asistente de fuentes.

<!-- 

t_generating_and_uploading_a_feed.xml

 -->

Consulte también [Creación de una fuente](../c-about-settings-menu/c-about-searching-menu.md#task_63179C1FC359497483CD6CE13FD1C250).

**Para generar y cargar una fuente**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. En la [!DNL Feeds] página, en la [!DNL Name] columna de la tabla, haga clic en la lista desplegable situada junto al nombre de una fuente y, a continuación, haga clic en **[!UICONTROL Generate and Upload Feed]**.
1. En la [!DNL Feeds] página, la columna [!DNL Feed Status] se actualiza durante y después de la generación y carga de fuentes de datos.
