---
description: Utilice el menú Rastreo para definir las máscaras de fecha y URL, las contraseñas, los tipos de contenido, las conexiones, las definiciones de formulario y los puntos de entrada de URL.
seo-description: Utilice el menú Rastreo para definir las máscaras de fecha y URL, las contraseñas, los tipos de contenido, las conexiones, las definiciones de formulario y los puntos de entrada de URL.
seo-title: Acerca del menú Rastreo
solution: Target
subtopic: Crawling
title: Acerca del menú Rastreo
topic: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '11033'
ht-degree: 0%

---


# Acerca del menú Rastreo{#about-the-crawling-menu}

Utilice el menú Rastreo para definir las máscaras de fecha y URL, las contraseñas, los tipos de contenido, las conexiones, las definiciones de formulario y los puntos de entrada de URL.

## Acerca de los puntos de entrada de URL {#concept_5D857E3B5C124E85BC0B5AE77A509573}

La mayoría de los sitios Web tienen un punto de entrada o página de inicio principal que un cliente visita inicialmente. Este punto de entrada principal es la dirección URL desde la cual el robot de búsqueda comienza el rastreo de índice. Sin embargo, si el sitio web tiene varios dominios o subdominios, o si partes del sitio no están vinculadas desde el punto de entrada principal, puede utilizar puntos de entrada de URL para agregar más puntos de entrada.

Todas las páginas del sitio web debajo de cada punto de entrada de URL especificado se indexan. Puede combinar puntos de entrada de URL con máscaras para controlar exactamente qué partes de un sitio Web desea indexar. Debe volver a generar el índice del sitio web antes de que los efectos de la configuración de puntos de entrada de URL sean visibles para los clientes.

El punto de entrada principal suele ser la dirección URL del sitio Web que desea indexar y buscar. Puede configurar este punto de entrada principal en Configuración de cuenta.

Consulte [Configuración de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Después de especificar el punto de entrada de la URL principal, puede especificar, opcionalmente, puntos de entrada adicionales que desee rastrear en orden. La mayoría de las veces especificará puntos de entrada adicionales para las páginas Web que no están vinculadas desde las páginas debajo del punto de entrada principal. Especifique puntos de entrada adicionales cuando el sitio web abarque más de un dominio, como en el siguiente ejemplo:

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

Usted califica cada punto de entrada con una o más de las siguientes palabras clave separadas por espacios en la tabla a continuación. Estas palabras clave afectan la manera en que se indexa la página.

**Importante**: Asegúrese de separar una palabra clave determinada del punto de entrada y entre sí por un espacio; una coma no es un separador válido.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Palabra clave </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Si no desea indexar el texto en la página de puntos de entrada, pero sí desea seguir los vínculos de la página, agregue <code>
       noindex 
     </code> después del punto de entrada. </p> <p>Separe la palabra clave del punto de entrada con un espacio como en el ejemplo siguiente: </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>Esta palabra clave equivale a una etiqueta meta de robots con <code>
       content="noindex" 
     </code>) entre el <code>
       &lt;head&gt; 
     </code>... 
     <code>
       &lt;/head&gt; 
     </code> de la página de puntos de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>noseguir </p> </td> 
   <td colname="col2"> <p> Si desea indexar el texto en la página de puntos de entrada pero no desea seguir ninguno de los vínculos de la página, agregue <code>
       nofollow 
     </code> después del punto de entrada. </p> <p>Separe la palabra clave del punto de entrada con un espacio como en el ejemplo siguiente: </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>Esta palabra clave equivale a una etiqueta meta de robots con <code>
       content="nofollow" 
     </code> entre el <code>
       &lt;head&gt; 
     </code>... 
     <code>
       &lt;/head&gt; 
     </code> de una página de punto de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>formulario </p> </td> 
   <td colname="col2"> <p> Cuando el punto de entrada es una página de inicio de sesión, generalmente <code>
       form 
     </code> se utiliza para que el robot de búsqueda pueda enviar el formulario de inicio de sesión y recibir las cookies correspondientes antes de rastrear el sitio Web. Cuando se utiliza la palabra clave "formulario", la página de punto de entrada no se indiza y el robot de búsqueda no marca la página de punto de entrada como rastreada. Utilícelo <code>
       nofollow 
     </code> si no desea que el robot de búsqueda siga los vínculos de la página. </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte también [Acerca de los tipos](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)de contenido.

Consulte también [Acerca del conector](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)de índice.

## Añadir varios puntos de entrada de URL que desea indizar {#task_2338A47387D74CFDAC4D4EF4A367ED45}

Si el sitio web tiene varios dominios o subdominios y desea rastrearlos, puede utilizar los puntos de entrada de URL para agregar más direcciones URL.

Para establecer el punto de entrada de la URL principal del sitio web, utilice Configuración de cuenta.

Consulte [Configuración de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

**Para agregar varios puntos de entrada de URL que desee indizar**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**.
1. En la [!DNL URL Entrypoints] página, en el [!DNL Entrypoints] campo, escriba una dirección URL por línea.
1. (Opcional) En la **[!UICONTROL Add Index Connector Configurations]** lista desplegable, seleccione un conector de índice que desee agregar como punto de entrada para la indexación.

   La lista desplegable solo está disponible si previamente ha agregado una o más definiciones de conector de índice.

   ![](assets/url_entrypoints_index_connector.png)

   Consulte [Añadir una definición](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)de conector de índice.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las máscaras URL {#concept_8039DFC53FF3410AA494D602F71BA164}

Las máscaras URL son patrones que determinan qué documentos del sitio Web indexan o no los índices del robot de búsqueda.

Asegúrese de volver a generar el índice del sitio para que los resultados de las máscaras URL sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

A continuación se indican dos tipos de máscaras URL que puede utilizar:

* Incluir máscaras URL
* Excluir máscaras URL

Las máscaras URL de inclusión indican al robot de búsqueda que indexe los documentos que coincidan con el patrón de la máscara.

Las máscaras de exclusión de URL indican al robot de búsqueda que indexe los documentos coincidentes.

A medida que el robot de búsqueda viaja de un vínculo a otro a través del sitio web, encuentra direcciones URL y busca máscaras que coincidan con esas direcciones URL. La primera coincidencia determina si se debe incluir o excluir esa dirección URL del índice. Si ninguna máscara coincide con una dirección URL encontrada, esa dirección URL se descarta del índice.

Las máscaras URL de inclusión para las direcciones URL de los puntos de entrada se generan automáticamente. Este comportamiento garantiza que todos los documentos encontrados en el sitio web se indiquen. También elimina convenientemente los enlaces que &quot;dejan&quot; tu sitio web. Por ejemplo, si una página indizada se vincula a https://www.yahoo.com, el robot de búsqueda no indexará esa dirección URL porque no coincide con la máscara de inclusión generada automáticamente por la dirección URL del punto de entrada.

Cada máscara de dirección URL que especifique debe estar en una línea independiente.

La máscara puede especificar cualquiera de las siguientes opciones:

* Una ruta completa como en `https://www.mydomain.com/products.html`.
* Una ruta parcial como en `https://www.mydomain.com/products`.
* Dirección URL que utiliza comodines como en `https://www.mydomain.com/*.html`.
* Una expresión normal (para usuarios avanzados).

   Para convertir una máscara en una expresión normal, inserte la palabra clave `regexp` entre el tipo de máscara ( `exclude` o `include`) y la máscara de dirección URL.

A continuación se muestra un ejemplo sencillo de máscara de exclusión URL:

```
exclude https://www.mydomain.com/photos
```

Dado que este ejemplo es una máscara de URL de exclusión, no se indexará ningún documento que coincida con el patrón. El patrón coincide con cualquier elemento encontrado, tanto los archivos como las carpetas, de modo que `https://www.mydomain.com/photos.html` y `https://www.mydomain.com/photos/index.html`, que coinciden con la URL de exclusión, no se indizan. Para que solo coincidan los archivos de la `/photos/` carpeta, la máscara URL debe contener una barra diagonal final, como en el ejemplo siguiente:

```
exclude https://www.mydomain.com/photos/
```

El siguiente ejemplo de máscara de exclusión utiliza comodines. Indica al robot de búsqueda que pase por alto los archivos con la extensión &quot;.pdf&quot;. El robot de búsqueda no agrega estos archivos al índice.

```
exclude *.pdf
```

A continuación se muestra una simple máscara de URL de inclusión:

```
include https://www.mydomain.com/news/
```

Solo se indexan los documentos que están vinculados mediante una serie de vínculos desde un punto de entrada de URL o que se utilizan como puntos de entrada de URL. La enumeración única de la dirección URL de un documento como una máscara de URL de inclusión no indexa un documento no vinculado. Para agregar documentos no vinculados al índice, puede utilizar la función Puntos de entrada de URL.

Consulte [Acerca de los puntos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

Incluir máscaras y excluir máscaras puede funcionar conjuntamente. Puede excluir una gran parte del sitio web de la indexación mediante la creación de una máscara de URL de exclusión e incluir una o más de las páginas excluidas con una máscara de URL de inclusión. Por ejemplo, supongamos que la dirección URL del punto de entrada es la siguiente:

```
https://www.mydomain.com/photos/
```

El robot de búsqueda rastrea e indexa todas las páginas debajo `/photos/summer/`, `/photos/spring/` y `/photos/fall/` (suponiendo que hay vínculos a al menos una página en cada directorio desde la `photos` carpeta). Este comportamiento se debe a que las rutas de vínculo permiten al robot de búsqueda encontrar los documentos en las carpetas `/summer/`, `/spring/`y `/fall/`, y las direcciones URL de las carpetas coinciden con la máscara de inclusión que genera automáticamente la dirección URL del punto de entrada.

Puede elegir excluir todas las páginas de la `/fall/` carpeta con una máscara de URL de exclusión, como en el ejemplo siguiente:

```
exclude https://www.mydomain.com/photos/fall/
```

O bien, incluya selectivamente solo `/photos/fall/redleaves4.html` como parte del índice con la siguiente máscara URL:

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Para que los dos ejemplos de máscara anteriores funcionen correctamente, la máscara de inclusión aparece en primer lugar, como se muestra a continuación:

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

Dado que el robot de búsqueda sigue las direcciones en el orden en que aparecen, primero incluye `/photos/fall/redleaves4.html`y luego excluye el resto de los archivos de la `/fall` carpeta.

Si las instrucciones se especifican de la forma contraria a la siguiente:

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

A continuación, no `/photos/fall/redleaves4.html` se incluye, aunque la máscara especifique que se incluye.

Una máscara URL que aparece primero siempre tiene prioridad sobre una máscara URL que aparece más adelante en la configuración de la máscara. Además, si el robot de búsqueda encuentra una página que coincide con una máscara URL de inclusión y una máscara URL de exclusión, la máscara que aparece primero siempre tiene prioridad.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

## Acerca del uso de palabras clave con máscaras URL {#section_7609A7A6D79B482ABCA8900886541AAB}

Puede calificar cada máscara de inclusión con una o más palabras clave separadas por espacio, lo que afecta la manera en que se indexan las páginas coincidentes.

Una coma no es válida como separador entre la máscara y la palabra clave; solo puede utilizar espacios.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Palabra clave </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Si no desea indexar el texto en las páginas que coinciden con la máscara de URL, pero desea seguir los vínculos de páginas coincidentes, agregue <code>
       noindex 
     </code> después de la máscara de URL de inclusión. Asegúrese de separar la palabra clave de la máscara con un espacio como en el ejemplo siguiente: </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>El ejemplo anterior especifica que el robot de búsqueda sigue todos los vínculos de archivos con la extensión, pero deshabilita la indexación de todo el texto contenido en esos archivos. <code>
       .swf 
     </code> </p> <p>La <code>
       noindex 
     </code> palabra clave equivale a una etiqueta meta de robot con <code>
       content="noindex" 
     </code> entre las <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> etiquetas de las páginas coincidentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>noseguir </p> </td> 
   <td colname="col2"> <p> Si desea indexar el texto en las páginas que coinciden con la máscara de dirección URL, pero no desea seguir los vínculos de la página coincidentes, agregue <code>
       nofollow 
     </code> después de la máscara de dirección URL de inclusión. Asegúrese de separar la palabra clave de la máscara con un espacio como en el ejemplo siguiente: </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>La <code>
       nofollow 
     </code> palabra clave equivale a una etiqueta meta de robot con <code>
       content="nofollow" 
     </code> entre las <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> etiquetas de las páginas coincidentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>Se utiliza para incluir y excluir máscaras. </p> <p>Cualquier máscara de URL precedida de <code>
       regexp 
     </code> se trata como una expresión normal. Si el robot de búsqueda encuentra documentos que coinciden con una máscara de URL de expresión normal de exclusión, esos documentos no se indizan. Si el robot de búsqueda encuentra documentos que coinciden con una máscara de URL de expresión normal y la incluye, esos documentos se indexan. Por ejemplo, supongamos que tiene la siguiente máscara URL: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>El robot de búsqueda excluye los archivos coincidentes, como 
     <code>
       https://www.mydomain.com/products/page1.html 
     </code> </p> <p>Si tenía la siguiente máscara de exclusión de URL de expresión normal: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>El robot de búsqueda no incluye ninguna dirección URL que contenga un parámetro CGI como <code>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </code>. </p> <p>Si tiene lo siguiente, incluya la máscara de URL de expresión normal: </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>El robot de búsqueda sigue todos los vínculos de archivos con la extensión ".swf". La <code>
       noindex 
     </code> palabra clave también especifica que el texto de los archivos coincidentes no se indiza. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expresiones regulares </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Añadir máscaras URL para indexar o no partes del sitio web {#task_E1AFC17C746048B8843013D979E082C1}

Puede utilizar [!DNL URL Masks] para definir qué partes del sitio Web desea o no desea rastrear e indexar.

Utilice el campo Probar máscaras URL para comprobar si un documento se incluye o no después de indexar.

Asegúrese de volver a generar el índice del sitio para que los resultados de las máscaras URL sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

**Adición de máscaras URL para indexar o no partes del sitio web**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**.
1. (Opcional) En la [!DNL URL Masks] página, en el **[!UICONTROL Test URL Masks]** campo, introduzca una máscara de URL de prueba en el sitio web y, a continuación, haga clic en **[!UICONTROL Test]**.
1. En el [!DNL URL Masks] campo, escriba `include` (para agregar un sitio web que desee rastrear e indexar) o `exclude` (para bloquear un sitio web para que no se pueda rastrear ni indizar), seguido de la dirección de máscara URL.

   Introduzca una dirección de máscara URL por línea. Ejemplo:

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las máscaras de fecha {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

Puede utilizar Máscaras de fecha para incluir o excluir archivos de los resultados de búsqueda según la edad del archivo.

Asegúrese de volver a generar el índice del sitio para que los resultados de las máscaras URL sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

A continuación se indican dos tipos de máscaras de fecha que puede utilizar:

* Incluir máscaras de fecha (&quot;días de inclusión&quot; e &quot;fecha de inclusión&quot;)

   Incluya los archivos de índice de máscaras de fecha con fecha anterior a la fecha especificada.
* Excluir máscaras de fecha (&quot;días de exclusión&quot; y &quot;fecha de exclusión&quot;)

   Excluir los archivos de índice de máscaras de fecha con fecha anterior a la fecha especificada.

De forma predeterminada, la fecha del archivo se determina a partir de la información de la etiqueta meta. Si no se encuentra ninguna etiqueta Meta, la fecha de un archivo se determina a partir del encabezado HTTP que se recibe del servidor cuando el robot de búsqueda descarga un archivo.

Cada máscara de fecha que especifique debe estar en una línea separada.

La máscara puede especificar cualquiera de las siguientes opciones:

* Una ruta completa como en `https://www.mydomain.com/products.html`
* Una ruta parcial como en `https://www.mydomain.com/products`
* Dirección URL que utiliza comodines `https://www.mydomain.com/*.html`
* Una expresión regular. Para convertir una máscara en una expresión normal, inserte la palabra clave `regexp` antes de la dirección URL.

Las máscaras de fecha de inclusión y exclusión pueden especificar una fecha de una de las dos formas siguientes. Las máscaras solo se aplican si los archivos coincidentes se crearon en la fecha especificada o antes de ella:

1. Varios días. Por ejemplo, supongamos que la máscara de fecha es la siguiente:

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   El número de días especificados se vuelve a contabilizar. Si el archivo tiene fecha en la fecha de llegada o antes, se aplica la máscara.

1. Fecha real con el formato AAAA-MM-DD. Por ejemplo, supongamos que la máscara de fecha es la siguiente:

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   Si el documento coincidente está fechado en la fecha especificada o antes, se aplica la máscara de fecha.

A continuación se muestra un ejemplo sencillo de máscara de fecha de exclusión:

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

Dado que se trata de una máscara de fecha de exclusión, cualquier archivo que coincida con el patrón no se indexará y tendrá 90 días de antigüedad o más. Cuando se excluye un documento, no se indiza ningún texto y no se siguen vínculos de ese archivo. El archivo se ignora de forma efectiva. En este ejemplo, los archivos y las carpetas pueden coincidir con el patrón de URL especificado. Observe que tanto `https://www.mydomain.com/docs/archive.html` como `https://www.mydomain.com/docs/archive/index.html` coinciden con el patrón y no se indexan si tienen 90 días o más. Para que solo coincidan los archivos de la `/docs/archive/` carpeta, la máscara de fecha debe contener una barra diagonal final, como se muestra a continuación:

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

Las máscaras de fecha también se pueden utilizar con comodines. La siguiente máscara de exclusión indica al robot de búsqueda que pase por alto los archivos con la extensión &quot;.pdf&quot; con fecha de 2011-02-15 o anterior. El robot de búsqueda no agrega ningún archivo coincidente al índice.

```
exclude-date 2011-02-15 *.pdf
```

Incluir máscara de fecha tiene un aspecto similar, solo se agregan al índice los archivos coincidentes. El siguiente ejemplo de máscara de fecha indica al robot de búsqueda que indexe el texto de cualquier archivo que tenga cero días o más en el `/docs/archive/manual/` área del sitio web.

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

Incluir máscaras y excluir máscaras puede funcionar conjuntamente. Por ejemplo, puede excluir una gran parte del sitio web de la indexación mediante la creación de una máscara de fecha de exclusión e incluir una o más de las páginas excluidas con una máscara de URL de inclusión. Si la dirección URL del punto de entrada es la siguiente:

```
https://www.mydomain.com/archive/
```

El robot de búsqueda rastrea e indexa todas las páginas debajo `/archive/summer/`, `/archive/spring/`y `/archive/fall/` (suponiendo que hay vínculos a al menos una página en cada carpeta desde la `archive` carpeta). Este comportamiento se debe a que las rutas de vínculo permiten al robot de búsqueda &quot;buscar&quot; los archivos de las carpetas `/summer/`, `/spring/`y `/fall/` y las direcciones URL de las carpetas coinciden con la máscara de inclusión generada automáticamente por la dirección URL del punto de entrada.

Consulte [Acerca de los puntos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

Consulte [Configuración de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Puede elegir excluir todas las páginas con más de 90 días de antigüedad en la `/fall/` carpeta con una máscara de fecha de exclusión, como se muestra a continuación:

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Solo puede incluir de forma selectiva `/archive/fall/index.html` (independientemente de su antigüedad (se iguala cualquier archivo de 0 días o más) como parte del índice con la siguiente máscara de fecha:

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

Para que los dos ejemplos de máscara anteriores funcionen correctamente, debe aplicar la lista de la máscara de inclusión primero como en el siguiente ejemplo:

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Dado que el robot de búsqueda sigue las direcciones en el orden en que se especifican, primero incluye `/archive/fall/index.html`y luego excluye el resto de los archivos de la `/fall` carpeta.

Si las instrucciones se especifican de la forma contraria a la siguiente:

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

A continuación no `/archive/fall/index.html` se incluye, aunque la máscara especifique que debe estar. Una máscara de fecha que aparece primero siempre tiene prioridad sobre una máscara de fecha que puede aparecer más adelante en la configuración de la máscara. Además, si el robot de búsqueda encuentra una página que coincide tanto con una máscara de fecha de inclusión como con una máscara de fecha de exclusión, la máscara que aparece primero siempre tiene prioridad.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

## Acerca del uso de palabras clave con máscaras de fecha {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

Puede calificar cada máscara de inclusión con una o más palabras clave separadas por espacio, lo que afecta la manera en que se indexan las páginas coincidentes.

Una coma no es válida como separador entre la máscara y la palabra clave; solo puede utilizar espacios.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Palabra clave </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Si no desea indexar el texto en las páginas con fecha en la fecha especificada por la máscara de inclusión o antes de ella, agregue <code>
       noindex 
     </code> después de la máscara de fecha de inclusión como se muestra a continuación: </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>Asegúrese de separar la palabra clave de la máscara con un espacio. </p> <p>El ejemplo anterior especifica que el robot de búsqueda sigue todos los vínculos de archivos con la extensión ".swf" que tienen 10 días o más. Sin embargo, deshabilita la indexación de todo el texto contenido en esos archivos. </p> <p>Es posible que desee asegurarse de que el texto de los archivos antiguos no está indizado pero siga todos los vínculos de esos archivos. En estos casos, utilice una máscara de fecha de inclusión con la palabra clave "noindex" en lugar de utilizar una máscara de fecha de exclusión. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>noseguir </p> </td> 
   <td colname="col2"> <p> Si desea indexar el texto en las páginas con fecha en o antes de la fecha especificada por la máscara de inclusión, pero no desea seguir los vínculos de la página coincidente, agregue <code>
       nofollow 
     </code> después de la máscara de fecha de inclusión como se muestra a continuación: </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Asegúrese de separar la palabra clave de la máscara con un espacio. </p> <p>La <code>
       nofollow 
     </code> palabra clave es equivalente a una etiqueta meta de robot con <code>
       content="nofollow" 
     </code> entre la <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> etiqueta de las páginas coincidentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server-date </p> </td> 
   <td colname="col2"> <p>Se utiliza para incluir y excluir máscaras. </p> <p>El robot de búsqueda generalmente descarga y analiza cada archivo antes de comprobar las máscaras de fecha. Este comportamiento se produce porque algunos tipos de archivo pueden especificar una fecha dentro del propio archivo. Por ejemplo, un documento HTML puede incluir metaetiquetas que definan la fecha del archivo. </p> <p>Si va a excluir muchos archivos en función de su fecha y no desea cargar innecesariamente los servidores, puede usar <code>
       server-date 
     </code> después de la dirección URL en la máscara de fecha. </p> <p>Esta palabra clave indica al robot de búsqueda que confíe en la fecha del archivo que devuelve el servidor en lugar de analizar cada archivo. Por ejemplo, la siguiente máscara de fecha de exclusión omite las páginas que coinciden con la dirección URL si los documentos son 90 días o más, según la fecha devuelta por el servidor en los encabezados HTTP: </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> Si la fecha devuelta por el servidor es 90 días o más, <code>
       server-date 
     </code> especifica que los documentos excluidos no se descargarán del servidor. El resultado significa un tiempo de indexación más rápido para los documentos y una carga reducida en los servidores. Si no <code>
       server-date 
     </code> se especifica, el robot de búsqueda omite la fecha devuelta por el servidor en los encabezados HTTP. En su lugar, se descarga y comprueba cada archivo para ver si se ha especificado la fecha. Si no se especifica ninguna fecha en el archivo, el robot de búsqueda utiliza la fecha que devuelve el servidor. </p> <p>No debe utilizar <code>
       server-date 
     </code> si los archivos contienen comandos que anulan la fecha del servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> Se utiliza para incluir y excluir máscaras. </p> <p>Cualquier máscara de fecha precedida por <code>
       regexp 
     </code> se trata como una expresión normal. </p> <p>Si el robot de búsqueda encuentra archivos que coinciden con una máscara de fecha de expresión normal de exclusión, no los indexará. </p> <p>Si el robot de búsqueda encuentra archivos que coinciden y incluyen una máscara de fecha de expresión normal, indexará esos documentos. </p> <p>Por ejemplo, supongamos que tiene la siguiente máscara de fecha: </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>La máscara indica al robot de búsqueda que excluya los archivos coincidentes que tengan 180 días o más. Es decir, los archivos que contienen la palabra "archivo" en su dirección URL. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expresiones regulares </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Añadir máscaras de fecha para indexar o no partes del sitio web {#task_0010543C55F648D2B5DEFEFAD60FAF04}

Puede utilizar Máscaras de fecha para incluir o excluir archivos de los resultados de búsqueda de clientes en función de la edad de los archivos.

Utilice los campos **[!UICONTROL Test Date]** y **[!UICONTROL Test URL]** para comprobar si un archivo se incluye o no después de indexarlo.

Asegúrese de volver a generar el índice del sitio para que los resultados de las máscaras URL sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

**Adición de máscaras de fecha para indexar o no partes del sitio web**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Date Masks]**.
1. (Opcional) En la [!DNL Date Masks] página, en el **[!UICONTROL Test Date]** campo, introduzca una fecha con el formato AAAA-MM-DD (por ejemplo, `2011-07-25`); en el **[!UICONTROL Test URL]** campo, introduzca una máscara URL del sitio web y, a continuación, haga clic en **[!UICONTROL Test]**.
1. En el [!DNL Date Masks] campo, introduzca una dirección de máscara de fecha por línea.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las contraseñas {#concept_3EDBD731725D46B891F834D4472774DC}

Para acceder a partes del sitio web protegidas con autenticación básica HTTP, puede agregar una o más contraseñas.

Antes de que los clientes vean los efectos de la configuración de contraseña, debe volver a generar el índice del sitio.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

En la [!DNL Passwords] página, escriba cada contraseña en una sola línea. La contraseña consiste en una dirección URL o territorio, un nombre de usuario y una contraseña, como en el siguiente ejemplo:

```
https://www.mydomain.com/ myname mypassword
```

En lugar de usar una ruta de URL, como la anterior, también puede especificar un territorio.

Para determinar el dominio correcto que se debe utilizar, abra una página web protegida por contraseña con un navegador y vea el cuadro de diálogo &quot;Introducir contraseña de red&quot;.

![](assets/realms.gif)

El nombre del territorio, en este caso, es &quot;Mi territorio del sitio&quot;.

Con el nombre del dominio anterior, la contraseña podría tener el siguiente aspecto:

```
My Site Realm myusername mypassword
```

Si el sitio Web tiene varios dominios, puede crear varias contraseñas introduciendo un nombre de usuario y una contraseña para cada dominio en una línea separada, como en el siguiente ejemplo:

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

Puede combinar contraseñas que contengan direcciones URL o dominios para que la lista de contraseñas tenga el siguiente aspecto:

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

En la lista anterior, se utiliza la primera contraseña que contiene un dominio o una dirección URL que coincide con la solicitud de autenticación del servidor. Incluso si el archivo de `https://www.mysite.com/path1/path2/index.html` se encuentra en `Realm3`, por ejemplo, `name2` y `password2` se utiliza porque la contraseña definida con la dirección URL se muestra por encima de la definida con el dominio.

## Añadir contraseñas para acceder a áreas del sitio web que requieren autenticación {#task_DED19D476FF04B48BB6456D5ECB8628A}

Puede utilizar contraseñas para acceder a las áreas del sitio web protegidas por contraseña con fines de rastreo e indexación.

Antes de que los efectos de la contraseña sean visibles para los clientes, asegúrese de volver a generar el índice del sitio

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

**Para agregar contraseñas para acceder a áreas del sitio web que requieren autenticación**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Passwords]**.
1. En la [!DNL Passwords] página, en el **[!UICONTROL Passwords]** campo, introduzca un territorio o una dirección URL, su nombre de usuario y contraseña asociados, separados por un espacio.

   Ejemplo de contraseña de territorio y contraseña de URL en líneas separadas:

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   Solo agregue una contraseña por línea.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de los tipos de contenido {#concept_6FEA1355C0374500B4C53090C34A8A07}

Puede utilizar [!DNL Content Types] para seleccionar qué tipos de archivos desea rastrear e indexar para esta cuenta.

Los tipos de contenido que puede elegir rastrear e indexar incluyen documentos PDF, documentos de texto, películas de Flash de Adobe, archivos de aplicaciones de Microsoft Office como Word, Excel y Powerpoint, y texto en archivos MP3. El texto que se encuentra dentro de los tipos de contenido seleccionados se busca junto con el resto del texto del sitio web.

Antes de que los clientes vean los efectos de la configuración de tipos de contenido, debe volver a generar el índice del sitio.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

## Acerca de la indexación de archivos de música MP3 {#section_AD2E28BEEE3E46629E2B05C34A963673}

Si selecciona la opción **[!UICONTROL Text in MP3 Music Files]** en la [!DNL Content Types] página, se rastrea y se indexa un archivo MP3 de una de las dos maneras siguientes. La primera y más común es desde una etiqueta href delimitadora en un archivo HTML, como se muestra a continuación:

```
<a href="MP3-file-URL"></a>
```

La segunda forma es introducir la URL del archivo MP3 como punto de entrada de URL.

Consulte [Acerca de los puntos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

Un archivo MP3 está reconocido por su tipo MIME &quot;audio/mpeg&quot;.

Tenga en cuenta que los tamaños de archivo de música MP3 pueden ser bastante grandes, aunque normalmente contienen sólo una pequeña cantidad de texto. Por ejemplo, los archivos MP3 pueden almacenar de forma opcional el nombre del álbum, el nombre del artista, el título de la canción, el género de la canción, el año de lanzamiento y un comentario. Esta información se almacena al final del archivo en lo que se denomina TAG. Los archivos MP3 que contienen información de TAG se indizan de la siguiente manera:

* El título de la canción se trata como el título de una página HTML.
* El comentario se trata como una descripción definida para una página HTML.
* El género se trata como una palabra clave definida para una página HTML.
* El nombre del artista, el nombre del álbum y el año de publicación se tratan como el cuerpo de una página HTML.

Tenga en cuenta que cada archivo MP3 rastreado e indexado en el sitio web cuenta como una página.

Si su sitio web contiene muchos archivos MP3 de gran tamaño, puede superar el límite de bytes de indexación de su cuenta. Si esto sucede, puede anular la selección **[!UICONTROL Text in MP3 Music Files]** en la [!DNL Content Types] página para evitar la indexación de todos los archivos MP3 del sitio web.

Si solo desea evitar la indexación de determinados archivos MP3 en su sitio web, puede realizar una de las siguientes acciones:

* Rodee las etiquetas delimitadoras que se vinculan a los archivos MP3 con `<nofollow>` y `</nofollow>` etiquetas. El robot de búsqueda no sigue los vínculos entre esas etiquetas.

* Añada las direcciones URL de los archivos MP3 como máscaras de exclusión.

   Consulte [Acerca de las máscaras](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

## Selección de tipos de contenido para rastrear e indexar {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

Puede utilizar [!DNL Content Types] para seleccionar qué tipos de archivos desea rastrear e indexar para esta cuenta.

Los tipos de contenido que puede elegir rastrear e indexar incluyen documentos PDF, documentos de texto, películas de Flash de Adobe, archivos de aplicaciones de Microsoft Office como Word, Excel y Powerpoint, y texto en archivos MP3. El texto que se encuentra dentro de los tipos de contenido seleccionados se busca junto con el resto del texto del sitio web.

Antes de que los clientes vean los efectos de la configuración de tipos de contenido, debe volver a generar el índice del sitio.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

Para rastrear e indexar archivos MP3 chinos, japoneses o coreanos, complete los pasos a continuación. A continuación, en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**, especifique el conjunto de caracteres utilizado para codificar los archivos MP3.

Consulte [Acerca de las inyecciones](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

**Seleccionar tipos de contenido para rastrear e indexar**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.
1. En la [!DNL Content Types] página, compruebe los tipos de archivo que desea rastrear e indexar en el sitio web.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las conexiones {#concept_E2F3B7E7521147479E5948A94BB3A40B}

Puede utilizar Conexiones para agregar hasta diez conexiones HTTP que el robot de búsqueda utiliza para indexar el sitio Web.

Aumentar el número de conexiones puede reducir significativamente la cantidad de tiempo que se tarda en completar un rastreo y un índice. Sin embargo, tenga en cuenta que cada conexión adicional aumenta la carga en el servidor.

## Añadir conexiones para aumentar la velocidad de indexación {#task_3E9B83E43C1842A19066355A15C4A6FB}

Puede reducir la cantidad de tiempo que tarda en indexar el sitio web mediante Conexiones para aumentar el número de conexiones HTTP simultáneas que utiliza el explorador. Puede agregar hasta diez conexiones.

Tenga en cuenta que cada conexión adicional aumenta la carga que se coloca en el servidor.

**Agregar conexiones para aumentar la velocidad de indexación**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Connections]**.
1. En la [!DNL Parallel Indexing Connections] página, en el **[!UICONTROL Number of Connections]** campo, introduzca el número de conexiones (1-10) que desea agregar.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del envío del formulario {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

Puede utilizar el envío de formulario para ayudarle a reconocer y procesar formularios en el sitio web.

Durante el rastreo y la indexación del sitio web, cada formulario encontrado se compara con las definiciones de formulario que ha agregado. Si un formulario coincide con una definición de formulario, se envía para indexación. Si un formulario coincide con más de una definición, el formulario se envía una vez por cada definición coincidente.

## Añadir definiciones de formulario para indexar formularios en el sitio web {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

Se puede utilizar [!DNL Form Submission] para ayudar a procesar formularios reconocidos en el sitio web con fines de indexación.

Asegúrese de volver a generar el índice del sitio para que los resultados de los cambios sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

**Adición de definiciones de formularios para indexar formularios en el sitio Web**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. En la [!DNL Form Submission] página, haga clic en **[!UICONTROL Add New Form]**.
1. En la [!DNL Add Form Definition] página, establezca las opciones [!DNL Form Recognition] y [!DNL Form Submission] .

   Las cinco opciones de la [!DNL Form Recognition] sección de la [!DNL Form Definition] página se utilizan para identificar los formularios de las páginas Web que se pueden procesar.

   Las tres opciones de la [!DNL Form Submission] sección se utilizan para especificar los parámetros y valores que se envían con un formulario al servidor web.

   Introduzca un parámetro de reconocimiento o envío por línea. Cada parámetro debe incluir un nombre y un valor.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <b>Reconocimiento de formularios</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de dirección URL de página </p> </td> 
      <td colname="col2"> <p>Identifique la página web o las páginas que contienen el formulario. Para identificar un formulario que aparece en una sola página, introduzca la dirección URL de esa página como en el ejemplo siguiente: </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>Para identificar los formularios que aparecen en varias páginas, especifique una máscara URL que utilice caracteres comodín para describir las páginas. Para identificar los formularios encontrados en cualquier página ASP en <code> https://www.mydomain.com/register/ </code>, por ejemplo, debe especificar lo siguiente: </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>También puede utilizar una expresión normal para identificar varias páginas. Especifique la <code>
        regexp 
      </code> palabra clave antes de la máscara de dirección URL, como en el ejemplo siguiente: </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de dirección URL de acción </p> </td> 
      <td colname="col2"> <p>Identifica el atributo de acción de la <code>
        &lt;form&gt; 
      </code> etiqueta . </p> <p>Al igual que la máscara de dirección URL de la página, la máscara de dirección URL de acción puede adoptar la forma de una sola dirección URL, una URL con caracteres comodín o una expresión normal. </p> <p>La máscara URL puede ser cualquiera de las siguientes: 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> Una ruta completa como la siguiente: <code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> Una ruta parcial como en el siguiente ejemplo: <code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> Dirección URL que utiliza comodines como se muestra a continuación: <code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> Una expresión regular como la siguiente: <code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>Si no desea indexar el texto en las páginas identificadas por una máscara de dirección URL o por una máscara de dirección URL de acción, o si no desea que se sigan vínculos en esas páginas, puede utilizar las palabras clave <code>
        noindex 
      </code> y <code>
        nofollow 
      </code> . Puede agregar estas palabras clave a sus máscaras mediante máscaras URL o puntos de entrada. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> Acerca de los puntos de entrada de URL </a>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> Acerca de las máscaras URL </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de nombre de formulario </p> </td> 
      <td colname="col2"> <p>Identifica los formularios si las <code>
        &lt;form&gt; 
      </code> etiquetas de las páginas web contienen un atributo de nombre. </p> <p>Puede utilizar un nombre simple ( <code>
        login_form 
      </code>), un nombre con un comodín ( <code>
        form* 
      </code>) o una expresión normal ( <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>Normalmente, este campo se puede dejar vacío porque los formularios normalmente no tienen un atributo de nombre. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de ID de formulario </p> </td> 
      <td colname="col2"> <p>Identifica los formularios si las <code>
        &lt;form&gt; 
      </code> etiquetas de las páginas web contienen un atributo de identificación. </p> <p>Puede utilizar un nombre simple ( <code>
        login_form 
      </code>), un nombre con un comodín ( <code>
        form* 
      </code>) o una expresión normal ( <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>Normalmente, este campo se puede dejar vacío porque los formularios normalmente no tienen un atributo de nombre. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetros </p> </td> 
      <td colname="col2"> <p>Identifique los formularios que contienen o no contienen un parámetro con nombre o un parámetro con nombre con un valor específico. </p> <p>Por ejemplo, para identificar un formulario que contiene un parámetro de correo electrónico preestablecido en rick_brough@mydomain.com, un parámetro de contraseña, pero no un parámetro de nombre, debe especificar la siguiente configuración de parámetro, una por línea: </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Envío de formulario</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Anular URL de acción </p> </td> 
      <td colname="col2"> <p>Especifique cuándo el destinatario del envío del formulario es diferente del especificado en el atributo de acción del formulario. </p> <p>Por ejemplo, puede utilizar esta opción cuando el formulario se envía mediante una función de JavaScript que construye un valor de URL diferente del que se encuentra en el formulario. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Override (método) </p> </td> 
      <td colname="col2"> <p>Especifique cuándo el destinatario del envío del formulario es diferente del que se utiliza en el atributo de acción del formulario y cuándo el JavaScript que envía ha cambiado el método. </p> <p>Los valores predeterminados para todos los parámetros de formulario ( <code>
        &lt;input&gt; 
      </code> etiquetas, incluidos los campos ocultos), el valor predeterminado <code>
        &lt;option&gt; 
      </code> de una <code>
        &lt;select&gt; 
      </code> etiqueta y el texto predeterminado entre <code>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </code> etiquetas) se leen en la página web. Sin embargo, cualquier parámetro que aparezca en la sección Envío del <span class="wintitle"> formulario </span> , en el campo <span class="uicontrol"> Parámetros </span> , se reemplazará por los valores predeterminados del formulario. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetros </p> </td> 
      <td colname="col2"> <p>Puede añadir un prefijo a los parámetros de envío de formulario con la <code>
        not 
      </code> palabra clave. </p> <p>Al anteponer un parámetro con <code>
        not 
      </code>, no se envía como parte del envío del formulario. Este comportamiento resulta útil para las casillas de verificación que se deben enviar sin seleccionar. </p> <p>Por ejemplo, supongamos que desea enviar los siguientes parámetros: </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> El parámetro de correo electrónico con el valor 
      <code>
        nobody@mydomain.com 
      </code> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> El parámetro password con el valor 
      <code>
        tryme 
      </code> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> El parámetro mychecktal como no está seleccionado. </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>Todos los demás <code>
        &lt;form&gt; 
      </code> parámetros como sus valores predeterminados </p> </li> 
      </ul> </p> <p>El parámetro de envío de formulario tendría el siguiente aspecto: </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>El atributo de método de la <code>
        &lt;form&gt; 
      </code> etiqueta en la página web se utiliza para decidir si los datos se envían al servidor mediante el método GET o el método POST. </p> <p>Si la <code>
        &lt;form&gt; 
      </code> etiqueta no contiene un atributo de método, el formulario se envía mediante el método de GET. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Add]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una definición de formulario {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

Puede editar una definición de formulario existente si ha cambiado un formulario en el sitio Web o si sólo necesita cambiar la definición.

Tenga en cuenta que no hay ninguna [!DNL History] característica en la [!DNL Form Submission] página para revertir los cambios que realice en la definición del formulario.

Asegúrese de volver a generar el índice del sitio para que los resultados de los cambios sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

**Para editar una definición de formulario**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. En la [!DNL Form Submission] página, haga clic **[!UICONTROL Edit]** a la derecha de la definición de formulario que desee actualizar.
1. En la [!DNL Edit Form Definition] página, establezca las opciones [!DNL Form Recognition] y [!DNL Form Submission] .

   Consulte la tabla de opciones en [Añadir definiciones de formularios para indexar formularios en el sitio Web](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una definición de formulario {#task_C350FC0CDE344F2786215D544C048B5E}

Puede eliminar una definición de formulario existente si el formulario ya no existe en el sitio Web o si ya no desea procesar e indexar un formulario concreto.

Tenga en cuenta que no hay ninguna [!DNL History] característica en la [!DNL Form Submission] página para revertir los cambios que realice en la definición del formulario.

Asegúrese de volver a generar el índice del sitio para que los resultados de los cambios sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)escalonado.

**Eliminar una definición de formulario**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. En la [!DNL Form Submission] página, haga clic **[!UICONTROL Delete]** a la derecha de la definición de formulario que desee eliminar.

   Asegúrese de elegir la definición de formulario correcta que desea eliminar. No hay ningún cuadro de diálogo de confirmación de eliminación cuando hace clic **[!UICONTROL Delete]** en el paso siguiente.
1. En la [!DNL Delete Form Definition] página, haga clic en **[!UICONTROL Delete]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del conector de índice {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

Se utiliza [!DNL Index Connector] para definir fuentes de entrada adicionales para indexar páginas XML o cualquier tipo de fuente.

Puede utilizar un origen de entrada de fuente de datos para acceder al contenido almacenado en un formulario distinto del que se suele descubrir en un sitio web mediante uno de los métodos de rastreo disponibles. Cada documento rastreado e indexado corresponde directamente a una página de contenido del sitio web. Sin embargo, una fuente de datos proviene de un documento XML o de un archivo de texto delimitado por comas o tabuladores, y contiene la información de contenido que se va a indexar.

Un origen de datos XML consta de estatutos o registros XML que contienen información que corresponde a documentos individuales. Estos documentos individuales se agregan al índice. Una fuente de datos de texto contiene registros individuales delimitados por líneas que corresponden a documentos individuales. Estos documentos individuales también se agregan al índice. En cualquier caso, una configuración de conector de índice describe cómo interpretar la fuente. Cada configuración describe dónde reside el archivo y cómo los servidores acceden a él. La configuración también describe la información de &quot;asignación&quot;. Es decir, cómo se utilizan los elementos de cada registro para rellenar los campos de metadatos en el índice resultante.

Después de agregar una definición de conector de índice a la [!DNL Staged Index Connector Definitions] página, puede cambiar cualquier configuración, *excepto* los valores Nombre o Tipo.

La [!DNL Index Connector] página muestra la siguiente información:

* Nombre de los conectores de índice definidos que ha configurado y agregado.
* Uno de los siguientes tipos de fuentes de datos para cada conector que ha agregado:

   * **Texto** : archivos sencillos &quot;planos&quot;, delimitados por comas, delimitados por tabuladores u otros formatos delimitados de forma consistente.
   * **Fuente** : fuentes XML.
   * **XML** : colecciones de documentos XML.

* Indica si el conector está activado o no para el siguiente rastreo e indización realizado.
* La dirección del origen de datos.

Consulte también [Acerca del conector de índice](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)

## Cómo funciona el proceso de indexación para las configuraciones de texto y fuente en el conector de índice {#section_E059A33D61EE4DB0972A37B8A35E9E16}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Paso  </p> </th> 
   <th colname="col2" class="entry"> <p>Proceso </p> </th> 
   <th colname="col3" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Descargue la fuente de datos. </p> </td> 
   <td colname="col3"> <p>Para las configuraciones de texto y fuente, es una descarga de archivo sencilla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Desglose el origen de datos descargado en pseudodocumentos individuales. </p> </td> 
   <td colname="col3"> <p>Para <span class="uicontrol"> Texto </span>, cada nueva línea de texto delimitada por líneas corresponde a un documento individual y se analiza utilizando el delimitador especificado, como una coma o una tabulación. </p> <p>Para <span class="uicontrol"> Feed </span>, los datos de cada documento se extraen usando un patrón de expresión regular en el siguiente formulario: </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>Mediante <span class="uicontrol"> Asignar </span> en la página <span class="wintitle"> Conector de índice Añadir </span> , cree una copia en caché de los datos y, a continuación, cree una lista de vínculos para el buscador. Los datos se almacenan en una caché local y se rellenan con los campos configurados. </p> <p>Los datos analizados se escriben en la caché local. </p> <p>Esta caché se lee más tarde para crear los documentos HTML simples que necesita el rastreador. Por ejemplo, </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>El elemento <span class="codeph"> &lt;title&gt; </span> solo se genera cuando existe una asignación al campo de metadatos Título. Del mismo modo, el elemento <span class="codeph"> &lt;body&gt; </span> solo se genera cuando existe una asignación al campo de metadatos Body. </p> <p> <b>Importante</b>: No se admite la asignación de valores a la etiqueta meta de URL predefinida. </p> <p>Para todas las demás asignaciones, se generan <span class="codeph"> &lt;meta&gt; </span> etiquetas para cada campo que tenga datos encontrados en el documento original. </p> <p>Los campos de cada documento se agregan a la caché. Para cada documento que se escribe en la caché, también se genera un vínculo como en los siguientes ejemplos: </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>La asignación de la configuración debe tener un campo identificado como Clave principal. Esta asignación forma la clave que se utiliza cuando se recuperan datos de la caché. </p> <p>El buscador reconoce el <span class="codeph"> índice de URL: </span> prefijo de esquema, que luego puede acceder a los datos almacenados en la caché local. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Arrastre el conjunto de documentos en caché. </p> </td> 
   <td colname="col3"> <p>El <span class="codeph"> índice: </span> los vínculos se agregan a la lista pendiente del rastreador y se procesan en la secuencia de rastreo normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Procese cada documento. </p> </td> 
   <td colname="col3"> <p>El valor clave de cada vínculo corresponde a una entrada de la caché, por lo que al rastrear cada vínculo se obtienen los datos de ese documento de la caché. Luego se "integra" en una imagen HTML que se procesa y se agrega al índice. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cómo funciona el proceso de indexación para las configuraciones XML en el conector de índice {#section_7F1551EA51854C5C99F284CE260526EB}

El proceso de indexación para la configuración XML es similar al proceso para las configuraciones de texto y fuente con los siguientes cambios y excepciones menores.

Dado que los documentos para los rastreos XML ya están separados en archivos individuales, los pasos 1 y 2 de la tabla anterior no se aplican directamente. Si especifica una dirección URL en los campos **[!UICONTROL Host Address]** y **[!UICONTROL File Path]** de la [!DNL Index Connector Add] página, se descargará y se procesará como un documento HTML normal. Se espera que el documento de descarga contenga una colección de `<a href="{url}"...` vínculos, cada uno de los cuales apunta a un documento XML que se procesa. Estos vínculos se convierten al siguiente formulario:

```
<a href="index:<ic_config_name>?url="{url}">
```

Por ejemplo, si la configuración de Adobe devolvió los vínculos siguientes:

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

En la tabla anterior, el paso 3 no se aplica y el paso 4 se completa en el momento del rastreo y la indexación.

También puede mezclar sus documentos XML con otros documentos que se descubrieron de forma natural a través del proceso de rastreo. En estos casos, se pueden usar reglas de reescritura ( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**) para cambiar las direcciones URL de los documentos XML y dirigirlos al conector de índice.

Consulte [Acerca de la Lista de rastreo Recuperar reglas](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)URL.

Por ejemplo, se supone que tiene la siguiente regla de reescritura:

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

Esta regla traduce cualquier dirección URL que termine con `.xml` en un vínculo Conector de índice. El buscador reconoce y vuelve a escribir el esquema de `index:` URL. El proceso de descarga se redirige a través del servidor Apache Index Connector en el servidor primario. Cada documento descargado se examina utilizando el mismo patrón de expresión regular que se utiliza con las fuentes. En este caso, sin embargo, el documento HTML fabricado no se guarda en la caché. En su lugar, se entrega directamente al buscador para el procesamiento del índice.

## Cómo configurar varios conectores de índice {#section_C2B14C0F06354A57AEF6238FF3814E5D}

Puede definir varias configuraciones de conector de índice para cualquier cuenta. Las configuraciones se agregan automáticamente a la lista desplegable en **[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]** , como se muestra en la siguiente ilustración:

![](assets/url_entrypoints_index_connector.png)

Al seleccionar una configuración en la lista desplegable, se agrega el valor al final de la lista de los puntos de entrada de URL.

>[!NOTE]
>
>Aunque las configuraciones del conector de índice desactivadas se agregan a la lista desplegable, no puede seleccionarlas. Si selecciona la misma configuración del conector de índice por segunda vez, se agrega al final de la lista y se elimina la instancia anterior.

Para especificar un punto de entrada de conector de índice para un rastreo incremental, puede agregar entradas con el siguiente formato:

```
index:<indexconnector_configuration_name>
```

El buscador procesa cada entrada agregada si se encuentra en la página Conectores de índice y está activada.

Nota: Dado que la dirección URL de cada documento se crea utilizando el nombre de configuración del conector de índice y la clave principal del documento, asegúrese de utilizar el mismo nombre de configuración del conector de índice al realizar actualizaciones incrementales. Al hacerlo, se pueden [!DNL Adobe Search&Promote] actualizar correctamente los documentos indexados anteriormente.

Consulte también [Acerca de los puntos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

**Uso de mapas de configuración al agregar un conector de índice**

Cuando se agrega un conector de índice, se puede utilizar la función **[!UICONTROL Setup Maps]** para descargar una muestra del origen de datos. Los datos se examinan para determinar la idoneidad de la indexación.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Si ha seleccionado el tipo Conector de índice... </p> </th> 
   <th colname="col2" class="entry"> <p>La función de mapas de configuración... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Texto </p> </td> 
   <td colname="col2"> <p>Determina el valor del delimitador probando las fichas primero y luego las barras verticales ( <span class="codeph"> | </span>), y finalmente comas ( <span class="codeph"> , </span>). Si ya especificó un valor delimitador antes de hacer clic en <span class="uicontrol"> Configurar mapas </span>, se utilizará ese valor. </p> <p>El mejor ajuste resulta en que los campos de mapa se rellenen con suposiciones en los valores de etiqueta y campo correspondientes. Además, se muestra un muestreo de los datos analizados. Asegúrese de seleccionar <span class="uicontrol"> Encabezados en Primera fila </span> si sabe que el archivo incluye una fila de encabezado. La función de configuración utiliza esta información para identificar mejor las entradas de mapa resultantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fuente </p> </td> 
   <td colname="col2"> <p>Descarga el origen de datos y realiza un análisis XML sencillo. </p> <p>Los identificadores XPath resultantes se muestran en las filas Tag de la tabla Map y valores similares en Fields. Estas filas sólo identifican los datos disponibles y no generan las definiciones XPath más complicadas. Sin embargo, sigue siendo útil porque describe los datos XML e identifica los valores de Itemtag. </p> <p> <p>Nota:  La función de mapas de configuración descarga el origen XML completo para realizar su análisis. Si el archivo es grande, esta operación podría agotarse. </p> </p> <p>Cuando se realiza correctamente, esta función identifica todos los elementos XPath posibles, muchos de los cuales no son deseables de usar. Asegúrese de examinar las definiciones de mapa resultantes y eliminar las que no necesita o desea. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>Descarga la dirección URL de un documento individual representativo, no la lista de vínculo principal. Este documento único se analiza utilizando el mismo mecanismo que se utiliza con las fuentes y se muestran los resultados. </p> <p>Antes de hacer clic en <span class="uicontrol"> Añadir </span> para guardar la configuración, asegúrese de volver a cambiar la dirección URL al documento de lista del vínculo principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Importante**: Es posible que la función de mapas de configuración no funcione para grandes conjuntos de datos XML porque el analizador de archivos intenta leer todo el archivo en la memoria. Como resultado, podría experimentar una condición de memoria insuficiente. Sin embargo, cuando se procesa el mismo documento en el momento de la indexación, no se lee en la memoria. En cambio, los documentos grandes se procesan &quot;sobre la marcha&quot; y no se leen en la memoria en primer lugar.

**Uso de la Previsualización al agregar un conector de índice**

En el momento de agregar un conector de índice, puede utilizar la función **[!UICONTROL Preview]** para validar los datos, como si lo estuviera guardando. Ejecuta una prueba con la configuración, pero sin guardar la configuración en la cuenta. La prueba accede al origen de datos configurado. Sin embargo, escribe la caché de descarga en una ubicación temporal; no entra en conflicto con la carpeta de caché principal que utiliza el buscador de indexación.

Previsualización sólo procesa un valor predeterminado de cinco documentos, como se controla con Acct:IndexConnector-Previsualización-Max-Documentos. Los documentos previsualizados se muestran en el formulario de origen, a medida que se presentan en el buscador de indexación. La visualización es similar a una función &quot;Origen de Vista&quot; en un explorador Web. Puede desplazarse por los documentos del conjunto de previsualizaciones mediante los vínculos de navegación estándar.

Previsualización no admite configuraciones XML porque estos documentos se procesan directamente y no se descargan en la memoria caché.

## Añadir una definición de conector de índice {#task_96779B651A654E1F871F55D6DBBC8886}

Cada configuración de conector de índice define un origen de datos y asignaciones para relacionar los elementos de datos definidos para ese origen con los campos de metadatos del índice.

Antes de que los clientes vean los efectos de la nueva definición habilitada, vuelva a generar el índice del sitio.

**Adición de una definición de conector de índice**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la [!DNL Stage Index Connector Definitions] página, haga clic en **[!UICONTROL Add New Index Connector]**.
1. En la [!DNL Index Connector Add] página, establezca las opciones de conector que desee. Las opciones disponibles dependen del **[!UICONTROL Type]** que haya seleccionado.

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
      <td colname="col2"> <p>Nombre exclusivo de la configuración del conector de índice. Puede utilizar caracteres alfanuméricos. También se permiten los caracteres "_" y "-". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo  </p> </td> 
      <td colname="col2"> <p>La fuente de los datos. El tipo de fuente de datos que seleccione afecta a las opciones resultantes que están disponibles en la página Añadir <span class="wintitle"> conector de índice </span> . Puede elegir entre las opciones siguientes: </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Texto </span> <p>Archivos de texto planos sencillos, delimitados por comas, delimitados por tabuladores u otros formatos delimitados de forma consistente. Cada nueva línea de texto delimitada por líneas corresponde a un documento individual y se analiza utilizando el delimitador especificado. </p> <p>Puede asignar cada valor, o columna, a un campo de metadatos, al que se hace referencia mediante el número de columna, comenzando en 1 (uno). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Fuente </span> <p>Descarga un documento XML principal que contiene varias "filas" de información. </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>Descarga un documento XML principal que contiene vínculos ( <code>
        &lt;a&gt; 
      </code>) a documentos XML individuales. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fuente de datos: Texto</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Habilitado </p> </td> 
      <td colname="col2"> <p>Activa la configuración "on" para rastrear e indexar. O bien, puede desactivar la configuración para evitar el rastreo y la indexación. </p> <p> <b>Nota</b>: Las configuraciones del conector de índice desactivadas se omiten si se encuentran en una lista de punto de entrada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dirección del host </p> </td> 
      <td colname="col2"> <p>Especifica la dirección del host del servidor donde se ubican los datos. </p> <p>Si lo desea, puede especificar una ruta URI completa (identificador uniforme de recursos) al documento de origen de datos como en los siguientes ejemplos: </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p>o </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>El URI se desglosa en las entradas correspondientes para los campos Dirección del host, Ruta de archivo, Protocolo y, opcionalmente, Nombre de usuario y Contraseña. </p> <p>Especifica la dirección IP o la dirección URL del sistema host donde se encuentra el archivo de origen de datos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al archivo de texto plano simple, delimitado por comas, delimitado por tabuladores u otro archivo de formato delimitado por tabuladores. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta incremental del archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al archivo de texto plano simple, delimitado por comas, delimitado por tabuladores u otro archivo de formato delimitado por tabuladores. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones de aumento de índice. Si no se especifica ningún archivo, se utiliza el archivo que aparece en Ruta de archivo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo vertical </p> </td> 
      <td colname="col2"> <p>Especifica la ruta de acceso al archivo de texto plano simple, delimitado por comas, delimitado por tabuladores u otro archivo de formato delimitado de forma consistente que se utilizará durante una actualización vertical. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones de actualización vertical. </p> <p> <b>Nota</b>: Esta función no está habilitada de forma predeterminada. Póngase en contacto con la asistencia técnica para activar la función para su uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Elimina la ruta del archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al archivo de texto plano simple, que contiene un valor de identificador de documento único por línea. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones de aumento de índice. Los valores encontrados en este archivo se utilizan para generar solicitudes de "eliminación" para eliminar documentos indexados anteriormente. Los valores de este archivo deben corresponder a los valores encontrados en los archivos de ruta de archivo completa o incremental, en la columna identificada como clave <span class="uicontrol"> principal </span>. </p> <p> <b>Nota</b>: Esta función no está habilitada de forma predeterminada. Póngase en contacto con la asistencia técnica para activar la función para su uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica el protocolo que se utiliza para acceder al archivo. Puede elegir entre las opciones siguientes: </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTP. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTPS. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>Debe especificar las credenciales de autenticación correctas para acceder al servidor FTP. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>Debe especificar las credenciales de autenticación correctas para acceder al servidor SFTP. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Archivo </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tiempo de espera </p> </td> 
      <td colname="col2"> <p>Especifica el tiempo de espera, en segundos, para las conexiones FTP, SFTP, HTTP o HTTPS. Este valor debe estar entre 30 y 300. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Reintentos </p> </td> 
      <td colname="col2"> <p>Especifica el número máximo de reintentos para conexiones fallidas FTP, SFTP, HTTP o HTTPS. Este valor debe estar entre 0 y 10. </p> <p>Un valor de cero (0) impedirá los intentos de reintento. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Codificación </p> </td> 
      <td colname="col2"> <p>Especifica el sistema de codificación de caracteres que se utiliza en el archivo de origen de datos especificado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Delimitador </p> </td> 
      <td colname="col2"> <p>Especifica el carácter que desea utilizar para delimitar cada campo del archivo de origen de datos especificado. </p> <p>El carácter de coma ( <span class="codeph"> , </span>) es un ejemplo de delimitador. La coma actúa como delimitador de campo que ayuda a separar los campos de datos en el archivo de origen de datos especificado. </p> <p>¿Seleccionar <span class="uicontrol"> ficha? </span> para utilizar el carácter de tabulación horizontal como delimitador. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Encabezados en primera fila </p> </td> 
      <td colname="col2"> <p>Indica que la primera fila del archivo de origen de datos contiene sólo información de encabezado, no datos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número mínimo de documentos para indexar </p> </td> 
      <td colname="col2"> <p>Si se establece en un valor positivo, esto especifica el número mínimo de registros esperados en el archivo descargado. Si se reciben menos registros, se anula la operación de índice. </p> <p> <b>Nota</b>: Esta función no está habilitada de forma predeterminada. Póngase en contacto con la asistencia técnica para activar la función para su uso. </p> <p> <b>Nota</b>: Esta función solo se utiliza durante las operaciones de índice completas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Especifica las asignaciones de columna a metadatos mediante números de columna. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Columna </span> <p> Especifica un número de columna, siendo la primera columna 1 (una). Para agregar nuevas filas de asignación para cada columna, en <span class="wintitle"> Acción </span>, haga clic en <span class="uicontrol"> + </span>. </p> <p>No es necesario hacer referencia a cada columna en el origen de datos. En su lugar, puede omitir valores. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Campo </span> <p>Define el valor del atributo name que se utiliza para cada etiqueta &lt;meta&gt; generada. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Metadatos? </span> <p>Hace que <span class="uicontrol"> Campo </span> se convierta en una lista desplegable desde la que puede seleccionar campos de metadatos definidos para la cuenta actual. </p> <p>El valor <span class="uicontrol"> Campo </span> puede ser un campo de metadatos no definido, si lo desea. Un campo de metadatos no definido a veces resulta útil para crear contenido utilizado por <span class="wintitle"> Filtrado de secuencias de comandos </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Acerca del filtrado de secuencias de comandos </a>. </p> <p>Cuando Conector de índice procesa documentos XML con varias visitas en cualquier campo de mapa, los valores múltiples se concatenan en un solo valor en el documento en caché resultante. De forma predeterminada, estos valores se combinan con un delimitador de coma. Sin embargo, supongamos que el valor <span class="wintitle"> Campo </span> es un campo de metadatos definido. Además, ese campo tiene el conjunto de atributos <span class="wintitle"> Listas de permitidos </span> . En este caso, el valor Delimitadores de Lista del campo, que es el primer delimitador definido, se utiliza en la concatenación. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> ¿Clave principal? </span> <p>Sólo se identifica una definición del mapa como clave principal. Este campo se convierte en la referencia única que se presenta cuando se agrega este documento al índice. Este valor se utiliza en la dirección URL del documento en el índice. </p> <p>Los valores de <span class="uicontrol"> Clave principal </span> deben ser únicos en todos los documentos representados por la configuración del conector de índice; se omitirán los duplicados encontrados. Si los documentos de origen no contienen un solo valor único para su uso como clave <span class="uicontrol"> principal </span>, pero dos o más campos juntos <i>pueden</i> formar un identificador único, puede definir la clave principal <span class="uicontrol"> combinando varios valores </span> de columna <span class="uicontrol"> </span> con una barra vertical ("|") delimitando los valores. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> ¿Eliminar HTML? </span> <p>Cuando se selecciona esta opción, se eliminan todas las etiquetas HTML que se encuentren en los datos de este campo. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Acción </span> <p>Permite agregar filas al mapa o quitar filas del mapa. El orden de las filas no es importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fuente de datos: Fuente</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Habilitado </p> </td> 
      <td colname="col2"> <p>Activa la configuración "on" para rastrear e indexar. O bien, puede desactivar la configuración para evitar el rastreo y la indexación. </p> <p> <b>Nota</b>: Las configuraciones del conector de índice desactivadas se omiten si se encuentran en una lista de punto de entrada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dirección del host </p> </td> 
      <td colname="col2"> <p>Especifica la dirección IP o la dirección URL del sistema host donde se encuentra el archivo de origen de datos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al documento XML principal que contiene varias "filas" de información. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta incremental del archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al documento XML incremental que contiene varias "filas" de información. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones de aumento de índice. Si no se especifica ningún archivo, se utiliza el archivo que aparece en Ruta de archivo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo vertical </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al documento XML que contiene varias "filas" dispersas de información que se utilizarán durante una actualización vertical. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones de actualización vertical. </p> <p> <b>Nota</b>: Esta función no está habilitada de forma predeterminada. Póngase en contacto con la asistencia técnica para activar la función para su uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Elimina la ruta del archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al archivo de texto plano simple, que contiene un valor de identificador de documento único por línea. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones de aumento de índice. Los valores encontrados en este archivo se utilizan para generar solicitudes de "eliminación" para eliminar documentos indexados anteriormente. Los valores de este archivo deben corresponder a los valores encontrados en los archivos de ruta de archivo completa o incremental, en la columna identificada como clave <span class="uicontrol"> principal </span>. </p> <p> <b>Nota</b>: Esta función no está habilitada de forma predeterminada. Póngase en contacto con la asistencia técnica para activar la función para su uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica el protocolo que se utiliza para acceder al archivo. Puede elegir entre las opciones siguientes: </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTP. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTPS. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>Debe especificar las credenciales de autenticación correctas para acceder al servidor FTP. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>Debe especificar las credenciales de autenticación correctas para acceder al servidor SFTP. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Archivo </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifica el elemento XML que puede utilizar para identificar líneas XML individuales en el archivo de origen de datos que especificó. </p> <p>Por ejemplo, en el siguiente fragmento de fuente de un documento XML de Adobe, el valor de Itemtag es <span class="codeph"> record </span>: </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt;&lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt;         &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt;         &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt;         &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número mínimo de documentos para indexar </p> </td> 
      <td colname="col2"> <p>Si se establece en un valor positivo, esto especifica el número mínimo de registros esperados en el archivo descargado. Si se reciben menos registros, se anula la operación de índice. </p> <p> <b>Nota</b>: Esta función no está habilitada de forma predeterminada. Póngase en contacto con la asistencia técnica para activar la función para su uso. </p> <p> <b>Nota</b>: Esta función solo se utiliza durante las operaciones de índice completas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Permite especificar asignaciones de elementos XML a metadatos mediante expresiones XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Etiqueta </span> <p>Especifica una representación XPath de los datos XML analizados. Utilizando el documento XML de Adobe de ejemplo anterior, en la opción Itemtag, se puede asignar con la siguiente sintaxis: </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La sintaxis anterior se traduce como: </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>El <span class="codeph"> atributo display url </span> del <span class="codeph"> elemento record </span> se asigna al campo de metadatos <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>El <span class="codeph"> atributo content </span> de cualquier <span class="codeph"> metaelemento </span> contenido dentro de un <span class="codeph"> elemento de metadatos </span> , que se encuentra dentro de un elemento <span class="codeph"> record </span> , cuyo atributo name es <span class="codeph"> title </span><span class="codeph"> </span>, se asigna al título del campo de metadatos. </p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>El <span class="codeph"> atributo content </span> de cualquier <span class="codeph"> meta </span> contenido dentro de un <span class="codeph"> elemento de metadatos </span> , que se encuentra dentro del elemento <span class="codeph"> record </span> , cuyo atributo name es <span class="codeph"> description </span><span class="codeph"> </span>, se asigna al campo de metadatos. </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>El <span class="codeph"> atributo content </span> de cualquier <span class="codeph"> meta </span> contenido dentro de un <span class="codeph"> elemento de metadatos </span> , que se encuentra dentro del elemento <span class="codeph"> record </span> , cuyo atributo name es <span class="codeph"> description </span><span class="codeph"> </span>, se asigna al cuerpo del campo de metadatos. </p> </li> 
      </ul> </p> <p>XPath es una notación relativamente complicada. Hay más información disponible en la siguiente ubicación: </p> <p>Consulte <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Campo </span> <p>Define el valor del atributo name que se utiliza para cada etiqueta <span class="codeph"> &lt;meta&gt; </span> generada. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Metadatos? </span> <p>Hace que <span class="uicontrol"> Campo </span> se convierta en una lista desplegable desde la que puede seleccionar campos de metadatos definidos para la cuenta actual. </p> <p>El valor <span class="uicontrol"> Campo </span> puede ser un campo de metadatos no definido, si lo desea. Un campo de metadatos no definido a veces resulta útil para crear contenido utilizado por <span class="wintitle"> Filtrado de secuencias de comandos </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Acerca del filtrado de secuencias de comandos </a>. </p> <p>Cuando Conector de índice procesa documentos XML con varias visitas en cualquier campo de mapa, los valores múltiples se concatenan en un solo valor en el documento en caché resultante. De forma predeterminada, estos valores se combinan con un delimitador de coma. Sin embargo, supongamos que el valor <span class="wintitle"> Campo </span> es un campo de metadatos definido. Además, ese campo tiene el conjunto de atributos <span class="wintitle"> Listas de permitidos </span> . En este caso, el valor Delimitadores de Lista del campo, que es el primer delimitador definido, se utiliza en la concatenación. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> ¿Clave principal? </span> <p>Sólo se identifica una definición del mapa como clave principal. Este campo se convierte en la referencia única que se presenta cuando se agrega este documento al índice. Este valor se utiliza en la dirección URL del documento en el índice. </p> <p>Los valores de <span class="uicontrol"> Clave principal </span> deben ser únicos en todos los documentos representados por la configuración del conector de índice; se omitirán los duplicados encontrados. Si los documentos de origen no contienen un solo valor único para su uso como clave <span class="uicontrol"> principal </span>, pero dos o más campos juntos <i>pueden</i> formar un identificador único, puede definir la clave principal <span class="uicontrol"> combinando varias definiciones </span> de <span class="uicontrol"> </span> etiqueta con una barra vertical ("|") delimitando los valores. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> ¿Eliminar HTML? </span> <p>Cuando se selecciona esta opción, se eliminan todas las etiquetas HTML que se encuentren en los datos de este campo. </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> ¿Se utiliza para eliminar? </span> <p>Solo se utiliza durante las operaciones de Índice incremental. Los registros que coinciden con este patrón XPath identifican los elementos que se deben eliminar. El valor de la clave <span class="uicontrol"> principal </span> para cada registro de este tipo se utiliza para construir solicitudes de "eliminación", como en Suprimir ruta de archivo. </p> <p> <b>Nota</b>: Esta función no está habilitada de forma predeterminada. Póngase en contacto con la asistencia técnica para activar la función para su uso. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Acción </span> <p>Permite agregar filas al mapa o quitar filas del mapa. El orden de las filas no es importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fuente de datos: XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Habilitado </p> </td> 
      <td colname="col2"> <p>Activa la configuración "on" para rastrear e indexar. O bien, puede desactivar la configuración para evitar el rastreo y la indexación. </p> <p> <b>Nota</b>: Las configuraciones del conector de índice desactivadas se omiten si se encuentran en una lista de punto de entrada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dirección del host </p> </td> 
      <td colname="col2"> <p>Especifica la dirección URL del sistema host donde se encuentra el archivo de origen de datos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al documento XML principal que contiene vínculos ( <code>
        &lt;a&gt; 
      </code>) a documentos XML individuales. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica el protocolo que se utiliza para acceder al archivo. Puede elegir entre las opciones siguientes: </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTP. </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTPS. </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>Debe especificar las credenciales de autenticación correctas para acceder al servidor FTP. </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>Debe especificar las credenciales de autenticación correctas para acceder al servidor SFTP. </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> Archivo </li> 
      </ul> </p> <p> <b>Nota</b>: La configuración del protocolo solo se utiliza cuando hay información especificada en los campos Dirección del host y/o Ruta del archivo. Los documentos XML individuales se descargan mediante HTTP o HTTPS, según sus especificaciones de URL. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifica el elemento XML que define una "fila" en el archivo de origen de datos que especificó. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Permite especificar asignaciones de columna a metadatos mediante números de columna. </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> Etiqueta </span> <p>Especifica una representación XPath de los datos XML analizados. Con el documento XML de Adobe de ejemplo anterior, en la opción Itemtag, puede asignarlo con la siguiente sintaxis: </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La sintaxis anterior se traduce como: </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>El <span class="codeph"> atributo display url </span> del <span class="codeph"> elemento record </span> se asigna al campo de metadatos <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>El <span class="codeph"> atributo content </span> de cualquier <span class="codeph"> metaelemento </span> contenido dentro de un <span class="codeph"> elemento de metadatos </span> , que se encuentra dentro de un elemento <span class="codeph"> record </span> , cuyo atributo name es <span class="codeph"> title </span><span class="codeph"> </span>, se asigna al título del campo de metadatos. </p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>El <span class="codeph"> atributo content </span> de cualquier <span class="codeph"> meta </span> contenido dentro de un <span class="codeph"> elemento de metadatos </span> , que se encuentra dentro del elemento <span class="codeph"> record </span> , cuyo atributo name es <span class="codeph"> description </span><span class="codeph"> </span>, se asigna al campo de metadatos. </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>El <span class="codeph"> atributo content </span> de cualquier <span class="codeph"> meta </span> contenido dentro de un <span class="codeph"> elemento de metadatos </span> , que se encuentra dentro del elemento <span class="codeph"> record </span> , cuyo atributo name es <span class="codeph"> description </span><span class="codeph"> </span>, se asigna al cuerpo del campo de metadatos. </p> </li> 
      </ul> </p> <p>XPath es una notación relativamente complicada. Hay más información disponible en la siguiente ubicación: </p> <p>Consulte <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> Campo </span> <p>Define el valor del atributo name que se utiliza para cada etiqueta &lt;meta&gt; generada. </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> Metadatos? </span> <p>Hace que <span class="uicontrol"> Campo </span> se convierta en una lista desplegable desde la que puede seleccionar campos de metadatos definidos para la cuenta actual. </p> <p>El valor <span class="uicontrol"> Campo </span> puede ser un campo de metadatos no definido, si lo desea. Un campo de metadatos no definido a veces resulta útil para crear contenido utilizado por <span class="wintitle"> Filtrado de secuencias de comandos </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Acerca del filtrado de secuencias de comandos </a>. </p> <p>Cuando Conector de índice procesa documentos XML con varias visitas en cualquier campo de mapa, los valores múltiples se concatenan en un solo valor en el documento en caché resultante. De forma predeterminada, estos valores se combinan con un delimitador de coma. Sin embargo, supongamos que el valor <span class="wintitle"> Campo </span> es un campo de metadatos definido. Además, ese campo tiene el conjunto de atributos <span class="wintitle"> Listas de permitidos </span> . En este caso, el valor Delimitadores de Lista del campo, que es el primer delimitador definido, se utiliza en la concatenación. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> ¿Clave principal? </span> <p>Sólo se identifica una definición del mapa como clave principal. Este campo se convierte en la referencia única que se presenta cuando se agrega este documento al índice. Este valor se utiliza en la dirección URL del documento en el índice. </p> <p>Los valores de <span class="uicontrol"> Clave principal </span> deben ser únicos en todos los documentos representados por la configuración del conector de índice; se omitirán los duplicados encontrados. Si los documentos de origen no contienen un solo valor único para su uso como clave <span class="uicontrol"> principal </span>, pero dos o más campos juntos <i>pueden</i> formar un identificador único, puede definir la clave principal <span class="uicontrol"> combinando varias definiciones </span> de <span class="uicontrol"> </span> etiqueta con una barra vertical ("|") delimitando los valores. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> ¿Eliminar HTML? </span> <p>Cuando se selecciona esta opción, se eliminan todas las etiquetas HTML que se encuentren en los datos de este campo. </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> Acción </span> <p>Permite agregar filas al mapa o quitar filas del mapa. El orden de las filas no es importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Haga clic en **[!UICONTROL Setup Maps]** para descargar una muestra de la fuente de datos. Los datos se examinan para determinar la idoneidad de la indexación. Esta función solo está disponible para tipos de fuente y texto.
1. (Opcional) Haga clic en **[!UICONTROL Preview]** para probar el funcionamiento real de la configuración. Esta función solo está disponible para tipos de fuente y texto.
1. Haga clic **[!UICONTROL Add]** para agregar la configuración a la [!DNL Index Connector Definitions] página y a la [!DNL Index Connector Configurations] lista desplegable de la [!DNL URL Entrypoints] página.

   Consulte [Acerca de los puntos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.
1. En la [!DNL Index Connector Definitions] página, haga clic en **[!UICONTROL rebuild your staged site index]**.
1. (Opcional) En la [!DNL Index Connector Definitions] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una definición de conector de índice {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

Puede editar un conector de índice existente que haya definido.

>[!NOTE]
>
>No todas las opciones están disponibles para cambiar, como Nombre del conector de índice o Tipo desde la lista [!DNL Type] desplegable.

**Para editar una definición de conector de índice**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la [!DNL Index Connector] página, debajo del encabezado de la [!DNL Actions] columna, haga clic en **[!UICONTROL Edit]** para obtener un nombre de definición del conector de índice cuya configuración desee cambiar.
1. En la [!DNL Index Connector Edit] página, configure las opciones que desee.

   Consulte la tabla de opciones en [Añadir una definición](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)de conector de índice.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) En la [!DNL Index Connector Definitions] página, haga clic en **[!UICONTROL rebuild your staged site index]**.
1. (Opcional) En la [!DNL Index Connector Definitions] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Visualización de la configuración de una definición de conector de índice {#task_D0B71A7426E54247BDB3468EC576D871}

Puede revisar la configuración de una definición de conector de índice existente.

Después de agregar una definición de conector de índice a la [!DNL Index Connector Definitions] página, no podrá cambiar su configuración de tipo. En su lugar, debe eliminar la definición y luego agregar una nueva.

**Vista de la configuración de una definición de conector de índice**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la [!DNL Index Connector] página, debajo del encabezado de la [!DNL Actions] columna, haga clic en **[!UICONTROL Edit]** para obtener un nombre de definición del conector de índice cuya configuración desee revisar o editar.

## Copia de una definición de conector de índice {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

Puede copiar una definición de conector de índice existente para utilizarla como base para un nuevo conector de índice que desee crear.

Al copiar una definición de conector de índice, la definición copiada se desactiva de forma predeterminada. Para habilitar o &quot;activar&quot; la definición, debe editarla desde la [!DNL Index Connector Edit] página y seleccionar **[!UICONTROL Enable]**.

Consulte [Edición de una definición](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9)de conector de índice.

**Para copiar una definición de conector de índice**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la [!DNL Index Connector] página, debajo del encabezado de la [!DNL Actions] columna, haga clic en **[!UICONTROL Copy]** para obtener un nombre de definición del conector de índice cuya configuración desee duplicado.
1. En la [!DNL Index Connector Copy] página, escriba el nuevo nombre de la definición.
1. Haga clic **[!UICONTROL Copy]**.
1. (Opcional) En la [!DNL Index Connector Definitions] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cambio de nombre de una definición de conector de índice {#task_5132118FC21B47D99881E0ED425225D7}

Puede cambiar el nombre de una definición de conector de índice existente.

Después de cambiar el nombre de la definición, marque **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Desea asegurarse de que el nombre de la nueva definición se refleja en la lista desplegable de la [!DNL URL Entrypoints] página.

Consulte [Añadir varios puntos de entrada de URL que desea indizar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

**Cambio del nombre de una definición de conector de índice**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la [!DNL Index Connector] página, debajo del encabezado de la [!DNL Actions] columna, haga clic en **[!UICONTROL Rename]** para obtener el nombre de definición del conector de índice que desee cambiar.
1. En la [!DNL Index Connector Rename] página, introduzca el nuevo nombre de la definición en el [!DNL Name] campo.
1. Haga clic **[!UICONTROL Rename]**.
1. Haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Si el nombre del conector de índice anterior está presente en la lista, elimínelo y añada la entrada con el nuevo nombre.

   Consulte [Añadir varios puntos de entrada de URL que desea indizar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45). 1. (Opcional) En la [!DNL Index Connector Definitions] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una definición de conector de índice {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

Puede eliminar una definición de conector de índice existente que ya no necesite ni use.

**Eliminar una definición de conector de índice**

1. En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la [!DNL Index Connector Definitions] página, debajo del encabezado de la [!DNL Actions] columna, haga clic en **[!UICONTROL Delete]** para el nombre de definición del conector de índice que desee eliminar.
1. En la [!DNL Index Connector Delete] página, haga clic en **[!UICONTROL Delete]**.
