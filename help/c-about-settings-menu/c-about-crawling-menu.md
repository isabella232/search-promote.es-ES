---
description: Utilice el menú Rastreo para establecer las máscaras de fecha y URL, contraseñas, tipos de contenido, conexiones, definiciones de formulario y puntos de entrada de URL.
solution: Target
subtopic: Crawling
title: Acerca del menú Rastreo
topic: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '11016'
ht-degree: 0%

---


# Acerca del menú Rastreo{#about-the-crawling-menu}

Utilice el menú Rastreo para establecer las máscaras de fecha y URL, contraseñas, tipos de contenido, conexiones, definiciones de formulario y puntos de entrada de URL.

## Acerca de los puntos de entrada de URL {#concept_5D857E3B5C124E85BC0B5AE77A509573}

La mayoría de los sitios web tienen un punto de entrada o una página de inicio principal al que accede un cliente inicialmente. Este punto de entrada principal es la dirección URL desde la que el robot de búsqueda comienza a rastrear el índice. Sin embargo, si el sitio web tiene varios dominios o subdominios, o si partes del sitio no están vinculadas desde el punto de entrada principal, puede utilizar puntos de entrada de URL para agregar más puntos de entrada.

Se indexan todas las páginas del sitio web debajo de cada punto de entrada de URL especificado. Puede combinar puntos de entrada de URL con máscaras para controlar exactamente qué partes de un sitio web desea indexar. Debe volver a generar el índice del sitio web antes de que los clientes puedan ver los efectos de la configuración de puntos de entrada de URL.

El punto de entrada principal suele ser la dirección URL del sitio web que desea indexar y buscar. Puede configurar este punto de entrada principal en Configuración de cuenta.

Consulte [Configuración de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Una vez especificado el punto de entrada de la URL principal, puede especificar, opcionalmente, puntos de entrada adicionales que desee rastrear en orden. La mayoría de las veces, especificará puntos de entrada adicionales para páginas web que no están vinculadas desde páginas bajo el punto de entrada principal. Especifique puntos de entrada adicionales cuando el sitio web abarque más de un dominio, como en el siguiente ejemplo:

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

Cada punto de entrada se clasifica con una o más de las siguientes palabras clave separadas por espacio en la siguiente tabla. Estas palabras clave afectan al modo en que se indexa la página.

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
   <td colname="col2"> <p> Si no desea indexar el texto en la página de punto de entrada, pero sí desea seguir los vínculos de la página, agregue 
     <code>
       noindex 
     </code> después del punto de entrada. </p> <p>Separe la palabra clave del punto de entrada con un espacio, como en el siguiente ejemplo: </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>Esta palabra clave es equivalente a una metaetiqueta de robots con 
     <code>
       content="noindex" 
     </code>) entre la variable 
     <code>
       &lt;head&gt; 
     </code>... 
     etiquetas <code>
       &lt;/head&gt; 
     </code> de la página de puntos de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>noseguir </p> </td> 
   <td colname="col2"> <p> Si desea indexar el texto en la página de punto de entrada pero no desea seguir ninguno de los vínculos de la página, agregue 
     <code>
       nofollow 
     </code> después del punto de entrada. </p> <p>Separe la palabra clave del punto de entrada con un espacio, como en el siguiente ejemplo: </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>Esta palabra clave es equivalente a una metaetiqueta de robots con 
     <code>
       content="nofollow" 
     </code> entre la variable 
     <code>
       &lt;head&gt; 
     </code>... 
     etiqueta <code>
       &lt;/head&gt; 
     </code> de una página de punto de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>formulario </p> </td> 
   <td colname="col2"> <p> Cuando el punto de entrada es una página de inicio de sesión, 
     <code>
       form 
     </code> generalmente se utiliza para que el robot de búsqueda pueda enviar el formulario de inicio de sesión y recibir las cookies adecuadas antes de rastrear el sitio web. Cuando se utiliza la palabra clave "formulario", la página de punto de entrada no se indexa y el robot de búsqueda no marca la página de punto de entrada como rastreada. Uso 
     <code>
       nofollow 
     </code> si no desea que el robot de búsqueda siga los vínculos de la página. </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte también [Acerca de los tipos de contenido](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

Consulte también [Acerca del conector de índice](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84).

## Añadir varios puntos de entrada de URL que desea indexar {#task_2338A47387D74CFDAC4D4EF4A367ED45}

Si el sitio web tiene varios dominios o subdominios y desea que se rastreen, puede utilizar puntos de entrada de URL para agregar más direcciones URL.

Para establecer el punto de entrada principal de la URL del sitio web, use Configuración de la cuenta.

Consulte [Configuración de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

**Para agregar varios puntos de entrada de URL que desee indexar**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**.
1. En la página [!DNL URL Entrypoints], en el campo [!DNL Entrypoints], introduzca una dirección URL por línea.
1. (Opcional) En la lista desplegable **[!UICONTROL Add Index Connector Configurations]**, seleccione un conector de índice que desee agregar como punto de entrada para la indexación.

   La lista desplegable solo está disponible si ha añadido anteriormente una o más definiciones del conector de índice.

   ![](assets/url_entrypoints_index_connector.png)

   Consulte [Adición de una definición de conector de índice](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las máscaras de URL {#concept_8039DFC53FF3410AA494D602F71BA164}

Las máscaras de URL son patrones que determinan cuál de los documentos del sitio web indexa o no los índices del robot de búsqueda.

Asegúrese de reconstruir el índice del sitio para que los resultados de las máscaras de URL sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

A continuación se indican dos tipos de máscaras URL que puede utilizar:

* Incluir máscaras de URL
* Excluir máscaras de URL

Las máscaras de URL de inclusión indican al robot de búsqueda que indexe cualquier documento que coincida con el patrón de la máscara.

Las máscaras de exclusión de URL indican al robot de búsqueda que indexe los documentos coincidentes.

A medida que el robot de búsqueda viaja de un vínculo a otro a través de su sitio web, encuentra direcciones URL y busca máscaras que coincidan con esas direcciones URL. La primera coincidencia determina si se debe incluir o excluir esa dirección URL del índice. Si ninguna máscara coincide con una dirección URL encontrada, esa dirección URL se descarta del índice.

Las máscaras de URL de inclusión para las direcciones URL de los puntos de entrada se generan automáticamente. Este comportamiento garantiza que todos los documentos encontrados en el sitio web se indiquen. También elimina convenientemente los enlaces que &quot;dejan&quot; tu sitio web. Por ejemplo, si una página indexada vincula a https://www.yahoo.com, el robot de búsqueda no indexa esa dirección URL porque no coincide con la máscara de inclusión generada automáticamente por la dirección URL del punto de entrada.

Cada máscara de URL que especifique debe estar en una línea independiente.

La máscara puede especificar cualquiera de las siguientes opciones:

* Una ruta completa como en `https://www.mydomain.com/products.html`.
* Una ruta parcial como en `https://www.mydomain.com/products`.
* Dirección URL que utiliza comodines como en `https://www.mydomain.com/*.html`.
* Expresión regular (para usuarios avanzados).

   Para que una máscara sea una expresión regular, inserte la palabra clave `regexp` entre el tipo de máscara ( `exclude` o `include`) y la máscara URL.

A continuación se muestra un ejemplo sencillo de máscara de URL de exclusión:

```
exclude https://www.mydomain.com/photos
```

Dado que este ejemplo es una máscara de URL de exclusión, cualquier documento que coincida con el patrón no está indexado. El patrón coincide con cualquier elemento encontrado, tanto archivos como carpetas, de modo que `https://www.mydomain.com/photos.html` y `https://www.mydomain.com/photos/index.html`, que coinciden con la dirección URL de exclusión, no se indizan. Para que coincida únicamente con los archivos de la carpeta `/photos/` , la máscara de URL debe contener una barra diagonal, como en el siguiente ejemplo:

```
exclude https://www.mydomain.com/photos/
```

El siguiente ejemplo de máscara de exclusión utiliza un comodín. Indica al robot de búsqueda que pase por alto los archivos con la extensión &quot;.pdf&quot;. El robot de búsqueda no agrega estos archivos al índice.

```
exclude *.pdf
```

A continuación se muestra una simple máscara de URL de inclusión:

```
include https://www.mydomain.com/news/
```

Solo se indexan los documentos vinculados mediante una serie de vínculos desde un punto de entrada URL o que se utilizan como puntos de entrada URL. La enumeración única de la dirección URL de un documento como una máscara de URL de inclusión no indexa un documento desvinculado. Para agregar documentos desvinculados al índice, puede utilizar la función Puntos de entrada de URL.

Consulte [Acerca de los puntos de entrada de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Incluir máscaras y excluir máscaras pueden funcionar juntas. Puede excluir una gran parte del sitio web de la indexación creando una máscara de URL de exclusión, pero incluyendo una o más de las páginas excluidas con una máscara de URL de inclusión. Por ejemplo, supongamos que la dirección URL del punto de entrada es la siguiente:

```
https://www.mydomain.com/photos/
```

El robot de búsqueda rastrea e indexa todas las páginas en `/photos/summer/`, `/photos/spring/` y `/photos/fall/` (suponiendo que haya vínculos a al menos una página en cada directorio desde la carpeta `photos`). Este comportamiento se produce porque las rutas de vínculo permiten al robot de búsqueda encontrar los documentos de las carpetas `/summer/`, `/spring/` y `/fall/`, y que las direcciones URL de las carpetas coinciden con la máscara de inclusión que genera automáticamente la dirección URL del punto de entrada.

Puede elegir excluir todas las páginas de la carpeta `/fall/` con una máscara de URL de exclusión como en el siguiente ejemplo:

```
exclude https://www.mydomain.com/photos/fall/
```

O bien, incluya selectivamente solo `/photos/fall/redleaves4.html` como parte del índice con la siguiente máscara de URL:

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Para que los dos ejemplos de máscara anteriores funcionen según lo previsto, la máscara de inclusión se enumera primero, como en el siguiente ejemplo:

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

Dado que el robot de búsqueda sigue las indicaciones en el orden en que aparecen en la lista, el robot de búsqueda primero incluye `/photos/fall/redleaves4.html` y luego excluye el resto de los archivos de la carpeta `/fall`.

Si las instrucciones se especifican de la forma opuesta a la siguiente:

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Luego `/photos/fall/redleaves4.html` no se incluye, aunque la máscara especifique que se incluye.

Una máscara de URL que aparece primero siempre tiene prioridad sobre una máscara de URL que aparece más adelante en la configuración de la máscara. Además, si el robot de búsqueda encuentra una página que coincide con una máscara de inclusión de URL y una máscara de exclusión de URL, la máscara que aparece primero siempre tiene prioridad.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## Acerca del uso de palabras clave con máscaras de URL {#section_7609A7A6D79B482ABCA8900886541AAB}

Puede clasificar cada máscara de inclusión con una o más palabras clave separadas por espacio, lo que afecta a cómo se indexan las páginas coincidentes.

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
   <td colname="col2"> <p> Si no desea indexar el texto en las páginas que coinciden con la máscara de dirección URL, pero desea seguir los vínculos de páginas coincidentes, agregue 
     <code>
       noindex 
     </code> después de la máscara de inclusión de URL. Asegúrese de separar la palabra clave de la máscara con un espacio, como en el siguiente ejemplo: </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>El ejemplo anterior especifica que el robot de búsqueda sigue todos los vínculos de archivos con la variable 
     <code>
       .swf 
     </code> , pero deshabilita la indexación de todo el texto contenido en esos archivos. </p> <p>La variable 
     La palabra clave <code>
       noindex 
     </code> es equivalente a una metaetiqueta de robot con 
     <code>
       content="noindex" 
     </code> entre la variable 
     <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> etiquetas de páginas coincidentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>noseguir </p> </td> 
   <td colname="col2"> <p> Si desea indexar el texto en las páginas que coinciden con la máscara de dirección URL, pero no desea seguir los vínculos de la página coincidente, agregue 
     <code>
       nofollow 
     </code> después de la máscara de inclusión de URL. Asegúrese de separar la palabra clave de la máscara con un espacio, como en el siguiente ejemplo: </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>La variable 
     La palabra clave <code>
       nofollow 
     </code> es equivalente a una metaetiqueta de robot con 
     <code>
       content="nofollow" 
     </code> entre la variable 
     <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> etiquetas de páginas coincidentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>Se utiliza para incluir y excluir máscaras. </p> <p>Cualquier máscara de dirección URL precedida por 
     <code>
       regexp 
     </code> se trata como una expresión regular. Si el robot de búsqueda encuentra documentos que coinciden con una máscara de URL de expresión regular de exclusión, esos documentos no se indexan. Si el robot de búsqueda encuentra documentos que coinciden con una máscara URL de expresión regular de inclusión, esos documentos se indexan. Por ejemplo, supongamos que tiene la siguiente máscara de dirección URL: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>El robot de búsqueda excluye los archivos coincidentes, como 
     <code>
       https://www.mydomain.com/products/page1.html 
     </code> </p> <p>Si tenía la siguiente máscara de URL de expresión regular de exclusión: </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>El robot de búsqueda no incluye ninguna dirección URL que contenga un parámetro CGI como 
     <code>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </code>. </p> <p>Si tenía lo siguiente, incluir máscara de URL de expresión regular: </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>El robot de búsqueda sigue todos los vínculos de archivos con la extensión ".swf". La variable 
     La palabra clave <code>
       noindex 
     </code> también especifica que el texto de los archivos coincidentes no está indexado. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expresiones regulares </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Añadir máscaras de URL para indexar o no indexar partes del sitio web {#task_E1AFC17C746048B8843013D979E082C1}

Puede utilizar [!DNL URL Masks] para definir qué partes del sitio web desea o no desea rastrear e indexar.

Utilice el campo Probar máscaras de URL para comprobar si un documento está o no incluido después de indexar.

Asegúrese de reconstruir el índice del sitio para que los resultados de las máscaras de URL sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para agregar máscaras de URL para indexar o no indexar partes del sitio web**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**.
1. (Opcional) En la página [!DNL URL Masks], en el campo **[!UICONTROL Test URL Masks]**, introduzca una máscara de URL de prueba en el sitio web y haga clic en **[!UICONTROL Test]**.
1. En el campo [!DNL URL Masks], escriba `include` (para agregar un sitio web que desee rastrear e indexar), o escriba `exclude` (para bloquear un sitio web y evitar que se rastree e indexe), seguido de la dirección de máscara de URL.

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

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las máscaras de fecha {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

Puede utilizar Máscaras de fecha para incluir o excluir archivos de los resultados de búsqueda en función de la edad del archivo.

Asegúrese de reconstruir el índice del sitio para que los resultados de las máscaras de URL sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Las siguientes son dos tipos de máscaras de fecha que puede utilizar:

* Incluir máscaras de fecha (&quot;días de inclusión&quot; y &quot;fecha de inclusión&quot;)

   Incluir archivos de índice de máscaras de fecha con fecha anterior o anterior a la fecha especificada.
* Excluir máscaras de fecha (&quot;exclude-days&quot; y &quot;exclude-date&quot;)

   La exclusión de fechas enmascara los archivos de índice con fecha anterior o posterior a la fecha especificada.

De forma predeterminada, la fecha del archivo se determina a partir de la información de la metaetiqueta. Si no se encuentra ninguna Meta tag, la fecha de un archivo se determina a partir del encabezado HTTP que se recibe del servidor cuando el robot de búsqueda descarga un archivo.

Cada máscara de fecha que especifique debe estar en una línea independiente.

La máscara puede especificar cualquiera de las siguientes opciones:

* Una ruta completa como en `https://www.mydomain.com/products.html`
* Una ruta parcial como en `https://www.mydomain.com/products`
* Una dirección URL que utiliza comodines `https://www.mydomain.com/*.html`
* Expresión regular. Para que una máscara sea una expresión regular, inserte la palabra clave `regexp` antes de la dirección URL.

Las máscaras de fechas de inclusión y exclusión pueden especificar una fecha de una de las dos maneras siguientes. Las máscaras solo se aplican si los archivos coincidentes se crearon en la fecha especificada o antes de esta:

1. Un número de días. Por ejemplo, supongamos que la máscara de fecha es la siguiente:

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   El número de días especificados se vuelve a contabilizar. Si el archivo tiene fecha en la fecha o antes de la fecha de llegada, se aplica la máscara.

1. Una fecha real con el formato AAAA-MM-DD. Por ejemplo, supongamos que la máscara de fecha es la siguiente:

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   Si el documento coincidente tiene fecha en la fecha especificada o antes de ella, se aplica la máscara de fecha.

A continuación se muestra un ejemplo sencillo de máscara de fecha de exclusión:

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

Como se trata de una máscara de fecha de exclusión, cualquier archivo que coincida con el patrón no se indexa y tiene 90 días o más. Al excluir un documento, no se indexa ningún texto y no se siguen vínculos de ese archivo. El archivo se ignora de forma efectiva. En este ejemplo, tanto los archivos como las carpetas pueden coincidir con el patrón de URL especificado. Observe que tanto `https://www.mydomain.com/docs/archive.html` como `https://www.mydomain.com/docs/archive/index.html` coinciden con el patrón y no se indexan si tienen 90 días o más. Para que coincida únicamente con los archivos de la carpeta `/docs/archive/` , la máscara de fecha debe contener una barra diagonal como se muestra a continuación:

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

Las máscaras de fecha también se pueden utilizar con comodines. La siguiente máscara de exclusión indica al robot de búsqueda que pase por alto los archivos con la extensión &quot;.pdf&quot; que tengan fecha o fecha anterior al 2011-02-15. El robot de búsqueda no agrega ningún archivo coincidente a su índice.

```
exclude-date 2011-02-15 *.pdf
```

La máscara de fecha de inclusión tiene un aspecto similar, solo se añaden al índice los archivos coincidentes. El siguiente ejemplo de máscara de fecha de inclusión indica al robot de búsqueda que indexe el texto de cualquier archivo que tenga cero días o más en el área `/docs/archive/manual/` del sitio web.

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

Incluir máscaras y excluir máscaras pueden funcionar juntas. Por ejemplo, puede excluir una gran parte del sitio web de la indexación creando una máscara de fecha de exclusión, pero incluyendo una o más de las páginas excluidas con una máscara de URL de inclusión. Si la dirección URL del punto de entrada es la siguiente:

```
https://www.mydomain.com/archive/
```

El robot de búsqueda rastrea e indexa todas las páginas en `/archive/summer/`, `/archive/spring/` y `/archive/fall/` (suponiendo que haya vínculos a al menos una página en cada carpeta de la carpeta `archive`). Este comportamiento se produce porque las rutas de vínculo permiten al robot de búsqueda &quot;encontrar&quot; los archivos de las carpetas `/summer/`, `/spring/` y `/fall/` y que las direcciones URL de las carpetas coinciden con la máscara de inclusión generada automáticamente por la dirección URL del punto de entrada.

Consulte [Acerca de los puntos de entrada de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Consulte [Configuración de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Puede elegir excluir todas las páginas con más de 90 días de antigüedad en la carpeta `/fall/` con una máscara de fecha de exclusión, como se muestra a continuación:

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Puede incluir selectivamente solo `/archive/fall/index.html` (independientemente de su antigüedad; se hace coincidir cualquier archivo de 0 días o más) como parte del índice con la siguiente máscara de fecha:

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

Para que los dos ejemplos de máscara anteriores funcionen según lo previsto, debe incluir primero la máscara de inclusión como en el siguiente:

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Dado que el robot de búsqueda sigue las indicaciones en el orden en que se especifican, el robot de búsqueda primero incluye `/archive/fall/index.html` y luego excluye el resto de los archivos de la carpeta `/fall`.

Si las instrucciones se especifican de la forma opuesta a la siguiente:

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

A continuación, no se incluye `/archive/fall/index.html` aunque la máscara especifique que debe estarlo. Una máscara de fecha que aparece primero siempre tiene prioridad sobre una máscara de fecha que podría aparecer más adelante en la configuración de la máscara. Además, si el robot de búsqueda encuentra una página que coincide tanto con una máscara de fecha de inclusión como con una máscara de fecha de exclusión, la máscara que aparece primero siempre tiene prioridad.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## Acerca del uso de palabras clave con máscaras de fecha {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

Puede clasificar cada máscara de inclusión con una o más palabras clave separadas por espacio, lo que afecta a cómo se indexan las páginas coincidentes.

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
   <td colname="col2"> <p> Si no desea indexar el texto en las páginas con fecha o antes de la fecha especificada por la máscara de inclusión, agregue 
     <code>
       noindex 
     </code> después de la máscara de fecha de inclusión, como se muestra a continuación: </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>Asegúrese de separar la palabra clave de la máscara con un espacio. </p> <p>El ejemplo anterior especifica que el robot de búsqueda sigue todos los vínculos de archivos con la extensión ".swf" que tengan 10 días o más. Sin embargo, deshabilita la indexación de todo el texto contenido en esos archivos. </p> <p>Es posible que desee asegurarse de que el texto de los archivos más antiguos no esté indexado, pero siga todos los vínculos de esos archivos. En estos casos, utilice una máscara de fecha de inclusión con la palabra clave "noindex" en lugar de utilizar una máscara de fecha de exclusión. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>noseguir </p> </td> 
   <td colname="col2"> <p> Si desea indexar el texto en las páginas con fecha o antes de la fecha especificada por la máscara de inclusión, pero no desea seguir los vínculos de la página coincidente, agregue 
     <code>
       nofollow 
     </code> después de la máscara de fecha de inclusión, como se muestra a continuación: </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Asegúrese de separar la palabra clave de la máscara con un espacio. </p> <p>La variable 
     La palabra clave <code>
       nofollow 
     </code> es equivalente a una metaetiqueta de robot con 
     <code>
       content="nofollow" 
     </code> entre la variable 
     <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> etiqueta de páginas coincidentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server-date </p> </td> 
   <td colname="col2"> <p>Se utiliza para incluir y excluir máscaras. </p> <p>El robot de búsqueda generalmente descarga y analiza cada archivo antes de comprobar las máscaras de fecha. Este comportamiento se produce porque algunos tipos de archivo pueden especificar una fecha dentro del propio archivo. Por ejemplo, un documento HTML puede incluir metaetiquetas que establecen la fecha del archivo. </p> <p>Si va a excluir muchos archivos en función de su fecha y no desea cargar innecesariamente los servidores, puede usar 
     <code>
       server-date 
     </code> después de la dirección URL en la máscara de fecha. </p> <p>Esta palabra clave indica al robot de búsqueda que confíe en la fecha del archivo que devuelve el servidor en lugar de analizar cada archivo. Por ejemplo, la siguiente máscara de fecha de exclusión ignora las páginas que coinciden con la dirección URL si los documentos tienen 90 días o más, según la fecha que devuelva el servidor en los encabezados HTTP: </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> Si la fecha devuelta por el servidor ha transcurrido 90 días o más, 
     <code>
       server-date 
     </code> especifica que los documentos excluidos no se descargan del servidor. El resultado significa un tiempo de indexación más rápido para los documentos y una carga reducida colocada en los servidores. If 
     <code>
       server-date 
     </code> no se especifica, el robot de búsqueda ignora la fecha que devuelve el servidor en los encabezados HTTP. En su lugar, se descarga y comprueba cada archivo para ver si se especifica la fecha. Si no se especifica ninguna fecha en el archivo, el robot de búsqueda utiliza la fecha que devuelve el servidor. </p> <p>No debe usar 
     <code>
       server-date 
     </code> si los archivos contienen comandos que anulan la fecha del servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> Se utiliza para incluir y excluir máscaras. </p> <p>Cualquier máscara de fecha precedida por 
     <code>
       regexp 
     </code> se trata como una expresión regular. </p> <p>Si el robot de búsqueda encuentra archivos que coinciden con una máscara de fecha de expresión regular de exclusión, no los indexa. </p> <p>Si el robot de búsqueda encuentra archivos que coinciden con una máscara de fecha de expresión regular de inclusión, indexa esos documentos. </p> <p>Por ejemplo, supongamos que tiene la siguiente máscara de fecha: </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>La máscara indica al robot de búsqueda que excluya los archivos coincidentes que tengan 180 días o más. Es decir, archivos que contienen la palabra "archive" en su URL. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expresiones regulares </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Agregar máscaras de fecha para indexar o no indexar partes del sitio web {#task_0010543C55F648D2B5DEFEFAD60FAF04}

Puede utilizar Máscaras de fecha para incluir o excluir archivos de los resultados de búsqueda de clientes en función de la edad de los archivos.

Utilice los campos **[!UICONTROL Test Date]** y **[!UICONTROL Test URL]** para comprobar si un archivo se incluye o no después del índice.

Asegúrese de reconstruir el índice del sitio para que los resultados de las máscaras de URL sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para agregar máscaras de fecha para indexar o no partes del sitio web**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Date Masks]**.
1. (Opcional) En la página [!DNL Date Masks], en el campo **[!UICONTROL Test Date]**, introduzca una fecha con el formato AAAA-MM-DD (por ejemplo, `2011-07-25`); en el campo **[!UICONTROL Test URL]**, introduzca una máscara de URL del sitio web y haga clic en **[!UICONTROL Test]**.
1. En el campo [!DNL Date Masks], introduzca una dirección de máscara de fecha por línea.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las contraseñas {#concept_3EDBD731725D46B891F834D4472774DC}

Para acceder a partes del sitio web protegidas con autenticación básica HTTP, puede agregar una o más contraseñas.

Para que los clientes puedan ver los efectos de la configuración de la contraseña, debe volver a generar el índice del sitio.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

En la página [!DNL Passwords], escriba cada contraseña en una sola línea. La contraseña consiste en una dirección URL o dominio, un nombre de usuario y una contraseña, como en el siguiente ejemplo:

```
https://www.mydomain.com/ myname mypassword
```

En lugar de usar una ruta de URL, como en el ejemplo anterior, también puede especificar un dominio.

Para determinar el dominio correcto a utilizar, abra una página web protegida por contraseña con un navegador y mire el cuadro de diálogo &quot;Introducir contraseña de red&quot;.

![](assets/realms.gif)

El nombre de territorio, en este caso, es &quot;Mi territorio del sitio&quot;.

Con el nombre de dominio anterior, la contraseña puede tener el siguiente aspecto:

```
My Site Realm myusername mypassword
```

Si el sitio web tiene varios dominios, puede crear varias contraseñas introduciendo un nombre de usuario y una contraseña para cada dominio en una línea independiente, como en el siguiente ejemplo:

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

Puede combinar contraseñas que contengan direcciones URL o reinos para que la lista de contraseñas se parezca a la siguiente:

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

En la lista anterior, se utiliza la primera contraseña que contiene un dominio o una dirección URL que coincide con la solicitud de autenticación del servidor. Incluso si el archivo en `https://www.mysite.com/path1/path2/index.html` está en `Realm3`, por ejemplo, `name2` y `password2` se utilizan porque la contraseña definida con la dirección URL se muestra por encima de la definida con el dominio.

## Adición de contraseñas para acceder a áreas del sitio web que requieren autenticación {#task_DED19D476FF04B48BB6456D5ECB8628A}

Puede utilizar Contraseñas para acceder a áreas del sitio web protegidas con contraseña con fines de rastreo e indexación.

Antes de que los efectos de la contraseña sean visibles para los clientes, asegúrese de reconstruir el índice del sitio

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Para agregar contraseñas para acceder a áreas del sitio web que requieran autenticación**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Passwords]**.
1. En la página [!DNL Passwords], en el campo **[!UICONTROL Passwords]**, introduzca un dominio o una dirección URL, y su nombre de usuario y contraseña asociados, separados por un espacio.

   Ejemplo de contraseña de dominio y contraseña de URL en líneas independientes:

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   Solo añada una contraseña por línea.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de los tipos de contenido {#concept_6FEA1355C0374500B4C53090C34A8A07}

Puede utilizar [!DNL Content Types] para seleccionar qué tipos de archivos desea rastrear e indexar para esta cuenta.

Los tipos de contenido que puede elegir rastrear e indexar incluyen documentos PDF, documentos de texto, películas de Flash de Adobe, archivos de aplicaciones de Microsoft Office como Word, Excel y Powerpoint, y texto en archivos MP3. El texto que se encuentra dentro de los tipos de contenido seleccionados se busca junto con el resto del texto del sitio web.

Para que los clientes puedan ver los efectos de la configuración de Tipos de contenido, debe volver a generar el índice del sitio.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## Acerca de la indexación de archivos de música MP3 {#section_AD2E28BEEE3E46629E2B05C34A963673}

Si selecciona la opción **[!UICONTROL Text in MP3 Music Files]** en la página [!DNL Content Types] , se rastrea un archivo MP3 y se indexa de una de las dos maneras siguientes. La primera y más común forma de hacerlo es desde una etiqueta href delimitadora en un archivo HTML como se muestra a continuación:

```
<a href="MP3-file-URL"></a>
```

La segunda forma es introducir la URL del archivo MP3 como punto de entrada de URL.

Consulte [Acerca de los puntos de entrada de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Un archivo MP3 se reconoce por su tipo MIME &quot;audio/mpeg&quot;.

Tenga en cuenta que los tamaños de archivo de música MP3 pueden ser bastante grandes, aunque normalmente contienen sólo una pequeña cantidad de texto. Por ejemplo, los archivos MP3 pueden, opcionalmente, almacenar cosas como el nombre del álbum, el nombre del artista, el título de la canción, el género de la canción, el año de lanzamiento y un comentario. Esta información se almacena al final del archivo en lo que se denomina TAG. Los archivos MP3 que contienen información de TAG se indexan de la siguiente manera:

* El título de la canción se trata como el título de una página HTML.
* El comentario se trata como una descripción definida para una página HTML.
* El género se trata como una palabra clave definida para una página HTML.
* El nombre del artista, el nombre del álbum y el año de lanzamiento se tratan como el cuerpo de una página HTML.

Tenga en cuenta que cada archivo MP3 que se rastrea e indexa en su sitio web cuenta como una página.

Si su sitio web contiene muchos archivos MP3 de gran tamaño, puede que exceda el límite de bytes de indexación de su cuenta. Si esto sucede, puede anular la selección **[!UICONTROL Text in MP3 Music Files]** en la página [!DNL Content Types] para evitar la indexación de todos los archivos MP3 del sitio web.

Si solo desea evitar la indexación de ciertos archivos MP3 en su sitio web, puede realizar una de las siguientes acciones:

* Rodee las etiquetas de anclaje que se vinculan a los archivos MP3 con etiquetas `<nofollow>` y `</nofollow>`. El robot de búsqueda no sigue los vínculos entre esas etiquetas.

* Añada las direcciones URL de los archivos MP3 como máscaras de exclusión.

   Consulte [Acerca de las máscaras de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

## Selección de tipos de contenido para rastrear e indexar {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

Puede utilizar [!DNL Content Types] para seleccionar qué tipos de archivos desea rastrear e indexar para esta cuenta.

Los tipos de contenido que puede elegir rastrear e indexar incluyen documentos PDF, documentos de texto, películas de Flash de Adobe, archivos de aplicaciones de Microsoft Office como Word, Excel y Powerpoint, y texto en archivos MP3. El texto que se encuentra dentro de los tipos de contenido seleccionados se busca junto con el resto del texto del sitio web.

Para que los clientes puedan ver los efectos de la configuración de Tipos de contenido, debe volver a generar el índice del sitio.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Para rastrear e indexar archivos MP3 chinos, japoneses o coreanos, complete los pasos a continuación. A continuación, en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**, especifique el conjunto de caracteres que se utiliza para codificar los archivos MP3.

Consulte [Acerca de las inyecciones](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

**Seleccionar tipos de contenido para rastrear e indexar**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.
1. En la página [!DNL Content Types], compruebe los tipos de archivo que desea rastrear e indexar en el sitio web.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las conexiones {#concept_E2F3B7E7521147479E5948A94BB3A40B}

Puede utilizar Conexiones para agregar hasta diez conexiones HTTP que el robot de búsqueda utiliza para indexar su sitio web.

Aumentar el número de conexiones puede reducir significativamente la cantidad de tiempo que se tarda en completar un rastreo y un índice. Sin embargo, tenga en cuenta que cada conexión adicional aumenta la carga en el servidor.

## Añadir conexiones para aumentar la velocidad de indexación {#task_3E9B83E43C1842A19066355A15C4A6FB}

Puede reducir la cantidad de tiempo que se tarda en indexar el sitio web mediante Conexiones para aumentar el número de conexiones HTTP simultáneas que utiliza el rastreador. Se pueden agregar hasta diez conexiones.

Tenga en cuenta que cada conexión adicional aumenta la carga que se coloca en el servidor.

**Para agregar conexiones para aumentar la velocidad de indexación**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Connections]**.
1. En la página [!DNL Parallel Indexing Connections], en el campo **[!UICONTROL Number of Connections]**, introduzca el número de conexiones (1-10) que desea agregar.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del envío de formulario {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

Puede utilizar el envío de formulario para ayudarle a reconocer y procesar los formularios en su sitio web.

Durante el rastreo y la indexación del sitio web, cada formulario encontrado se compara con las definiciones de formulario agregadas. Si un formulario coincide con una definición del formulario, se envía para su indexación. Si un formulario coincide con más de una definición, el formulario se envía una vez para cada definición coincidente.

## Adición de definiciones de formulario para la indexación de formularios en el sitio web {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

Puede utilizar [!DNL Form Submission] para ayudar a procesar los formularios que se reconocen en el sitio web con fines de indexación.

Asegúrese de reconstruir el índice del sitio para que los resultados de los cambios sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Adición de definiciones de formulario para la indexación de formularios en el sitio web**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. En la página [!DNL Form Submission], haga clic en **[!UICONTROL Add New Form]**.
1. En la página [!DNL Add Form Definition], configure las opciones [!DNL Form Recognition] y [!DNL Form Submission] .

   Las cinco opciones de la sección [!DNL Form Recognition] de la página [!DNL Form Definition] se utilizan para identificar los formularios de las páginas web que se pueden procesar.

   Las tres opciones de la sección [!DNL Form Submission] se utilizan para especificar los parámetros y valores que se envían con un formulario al servidor web.

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
      <td colname="col1"> <p>Máscara de dirección URL de la página </p> </td> 
      <td colname="col2"> <p>Identifique la página web o páginas que contienen el formulario. Para identificar un formulario que aparece en una sola página, introduzca la dirección URL de esa página, como en el siguiente ejemplo: </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>Para identificar los formularios que aparecen en varias páginas, especifique una máscara de dirección URL que utilice caracteres comodín para describir las páginas. Para identificar los formularios encontrados en cualquier página ASP en <code> https://www.mydomain.com/register/ </code>, por ejemplo, debe especificar lo siguiente: </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>También puede utilizar una expresión regular para identificar varias páginas. Especifique la variable 
      Palabra clave <code>
        regexp 
      </code> antes de la máscara de URL, como en el siguiente ejemplo: </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de URL de acción </p> </td> 
      <td colname="col2"> <p>Identifica el atributo de acción de la variable 
      etiqueta <code>
        &lt;form&gt; 
      </code>. </p> <p>Al igual que la máscara de dirección URL de la página, la máscara de dirección URL de acción puede adoptar la forma de una sola dirección URL, una dirección URL con caracteres comodín o una expresión regular. </p> <p>La máscara de URL puede ser cualquiera de las siguientes: 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> Una ruta completa como la siguiente: <code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> Una ruta parcial como la siguiente: <code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> Una URL que utiliza comodines como en el siguiente ejemplo: <code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> Una expresión regular como la siguiente: <code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>Si no desea indexar el texto en páginas identificadas por una máscara de URL o por una máscara de URL de acción, o si no desea que se sigan vínculos en esas páginas, puede usar la variable 
      <code>
        noindex 
      </code> y 
      <code>
        nofollow 
      </code> palabras clave. Puede agregar estas palabras clave a sus máscaras usando máscaras de URL o puntos de entrada. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> Acerca de los puntos de entrada de URL </a>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> Acerca de las máscaras de URL </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de nombre de formulario </p> </td> 
      <td colname="col2"> <p>Identifica los formularios si la variable 
      Las etiquetas <code>
        &lt;form&gt; 
      </code> de las páginas web contienen un atributo name. </p> <p>Puede utilizar un nombre simple ( 
      <code>
        login_form 
      </code>), un nombre con un comodín ( 
      <code>
        form* 
      </code>) o una expresión regular ( 
      <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>Normalmente, este campo se puede dejar vacío porque los formularios no suelen tener un atributo de nombre. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Máscara de ID de formulario </p> </td> 
      <td colname="col2"> <p>Identifica los formularios si la variable 
      Las etiquetas <code>
        &lt;form&gt; 
      </code> de las páginas web contienen un atributo id. </p> <p>Puede utilizar un nombre simple ( 
      <code>
        login_form 
      </code>), un nombre con un comodín ( 
      <code>
        form* 
      </code>) o una expresión regular ( 
      <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>Normalmente, este campo se puede dejar vacío porque los formularios no suelen tener un atributo de nombre. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetros </p> </td> 
      <td colname="col2"> <p>Identifique los formularios que contienen o no contienen un parámetro con nombre o un parámetro con nombre con un valor específico. </p> <p>Por ejemplo, para identificar un formulario que contenga un parámetro de correo electrónico preestablecido en rick_brough@mydomain.com, un parámetro de contraseña, pero no un parámetro de nombre, debe especificar la siguiente configuración de parámetro, una por línea: </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Envío de formulario</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Anular URL de acción </p> </td> 
      <td colname="col2"> <p>Especifique cuándo el destino del envío del formulario es diferente del especificado en el atributo de acción del formulario. </p> <p>Por ejemplo, puede utilizar esta opción cuando el formulario se envíe mediante una función de JavaScript que construya un valor de URL diferente del que se encuentra en el formulario. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Override (método) </p> </td> 
      <td colname="col2"> <p>Especifique cuándo el destino del envío del formulario es diferente del que se utiliza en el atributo de acción del formulario y cuándo el JavaScript de envío ha cambiado el método. </p> <p>Los valores predeterminados de todos los parámetros de formulario ( 
      etiquetas <code>
        &lt;input&gt; 
      </code>, incluidos los campos ocultos), el valor predeterminado 
      <code>
        &lt;option&gt; 
      </code> desde un 
      <code>
        &lt;select&gt; 
      </code> y el texto predeterminado entre 
      <code>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </code> ) se leen desde la página web. Sin embargo, cualquier parámetro que aparezca en la sección <span class="wintitle"> Envío de formulario </span> del campo <span class="uicontrol"> Parámetros </span> se reemplaza por los valores predeterminados del formulario. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetros </p> </td> 
      <td colname="col2"> <p>Los parámetros de envío de formulario se pueden prefijar con la variable 
      <code>
        not 
      </code> palabra clave. </p> <p>Cuando crea un prefijo de un parámetro con 
      <code>
        not 
      </code>, no se envía como parte del envío del formulario. Este comportamiento resulta útil para las casillas de verificación que deben enviarse sin seleccionar. </p> <p>Por ejemplo, supongamos que desea enviar los siguientes parámetros: </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> El parámetro de correo electrónico con el valor 
      <code>
        nobody@mydomain.com 
      </code> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> El parámetro de contraseña con el valor 
      <code>
        tryme 
      </code> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> El parámetro mycheck no está seleccionado. </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>El resto 
      <code>
        &lt;form&gt; 
      </code> como valores predeterminados </p> </li> 
      </ul> </p> <p>El parámetro de envío de formulario tendría el siguiente aspecto: </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>El atributo de método de la variable 
      La etiqueta <code>
        &lt;form&gt; 
      </code> de la página web se usa para decidir si los datos se envían al servidor mediante el método de GET o el método de POST. </p> <p>Si la variable 
      La etiqueta <code>
        &lt;form&gt; 
      </code> no contiene un atributo de método; el formulario se envía mediante el método de GET. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Add]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una definición de formulario {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

Puede editar una definición de formulario existente si ha cambiado un formulario del sitio web o si solo necesita cambiar la definición.

Tenga en cuenta que no hay ninguna función [!DNL History] en la página [!DNL Form Submission] para revertir los cambios realizados en la definición del formulario.

Asegúrese de reconstruir el índice del sitio para que los resultados de los cambios sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Edición de una definición de formulario**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. En la página [!DNL Form Submission], haga clic en **[!UICONTROL Edit]** a la derecha de la definición del formulario que desea actualizar.
1. En la página [!DNL Edit Form Definition], configure las opciones [!DNL Form Recognition] y [!DNL Form Submission] .

   Consulte la tabla de opciones en [Adición de definiciones de formulario para la indexación de formularios en el sitio web](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una definición de formulario {#task_C350FC0CDE344F2786215D544C048B5E}

Puede eliminar una definición de formulario existente si el formulario ya no existe en el sitio web o si ya no desea procesar e indexar un formulario concreto.

Tenga en cuenta que no hay ninguna función [!DNL History] en la página [!DNL Form Submission] para revertir los cambios realizados en la definición del formulario.

Asegúrese de reconstruir el índice del sitio para que los resultados de los cambios sean visibles para los clientes.

Consulte [Configuración de un índice incremental de un sitio web provisional](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Eliminación de una definición de formulario**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. En la página [!DNL Form Submission], haga clic en **[!UICONTROL Delete]** a la derecha de la definición del formulario que desea quitar.

   Asegúrese de elegir la definición de formulario correcta que desee eliminar. No hay ningún cuadro de diálogo de confirmación de eliminación cuando hace clic en **[!UICONTROL Delete]** en el paso siguiente.
1. En la página [!DNL Delete Form Definition], haga clic en **[!UICONTROL Delete]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del conector de índice {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

Utilice [!DNL Index Connector] para definir fuentes de entrada adicionales para indexar páginas XML o cualquier tipo de fuente.

Se puede utilizar un origen de entrada de fuente de datos para acceder a contenido almacenado en un formulario diferente al que se suele descubrir en un sitio web mediante uno de los métodos de rastreo disponibles. Cada documento que se rastrea e indexa directamente corresponde a una página de contenido del sitio web. Sin embargo, una fuente de datos proviene de un documento XML o de un archivo de texto delimitado por comas o tabulaciones, y contiene la información de contenido que se va a indexar.

Un origen de datos XML consta de tablas o registros XML que contienen información que corresponde a documentos individuales. Estos documentos individuales se añaden al índice. Una fuente de datos de texto contiene registros individuales delimitados por líneas nuevas que corresponden a documentos individuales. Estos documentos individuales también se añaden al índice. En cualquier caso, una configuración de conector de índice describe cómo interpretar la fuente. Cada configuración describe dónde reside el archivo y cómo acceden a él los servidores. La configuración también describe la información de &quot;asignación&quot;. Es decir, cómo se utilizan los elementos de cada registro para rellenar los campos de metadatos en el índice resultante.

Después de agregar una definición de conector de índice a la página [!DNL Staged Index Connector Definitions], puede cambiar cualquier configuración, *excepto* para los valores Nombre o Tipo.

La página [!DNL Index Connector] muestra la siguiente información:

* El nombre de los conectores de índice definidos que ha configurado y agregado.
* Uno de los siguientes tipos de fuentes de datos para cada conector que ha agregado:

   * **Texto** : archivos &quot;planos&quot; simples, delimitados por comas, delimitados por tabulaciones u otros formatos delimitados de forma consistente.
   * **Fuente** : fuentes XML.
   * **XML** : colecciones de documentos XML.

* Indica si el conector está habilitado o no para el siguiente rastreo e indexación realizado.
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
   <td colname="col2"> <p>Desglose la fuente de datos descargada en seudodocumentos individuales. </p> </td> 
   <td colname="col3"> <p>Para <span class="uicontrol"> Texto </span>, cada línea de texto delimitada por líneas nuevas corresponde a un documento individual y se analiza utilizando el delimitador especificado, como una coma o una tabulación. </p> <p>Para <span class="uicontrol"> Fuente </span>, los datos de cada documento se extraen utilizando un patrón de expresión regular en el siguiente formulario: </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>Con <span class="uicontrol"> Asignar </span> en la página <span class="wintitle"> Conector de índice Agregar </span>, cree una copia en caché de los datos y, a continuación, cree una lista de vínculos para el buscador. Los datos se almacenan en una caché local y se rellenan con los campos configurados. </p> <p>Los datos analizados se escriben en la caché local. </p> <p>Esta caché se lee más tarde para crear los documentos HTML simples que necesita el rastreador. Por ejemplo, </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>El elemento <span class="codeph"> &lt;title&gt; </span> solo se genera cuando existe una asignación al campo de metadatos Título . Del mismo modo, el elemento <span class="codeph"> &lt;body&gt; </span> solo se genera cuando existe una asignación al campo de metadatos Body . </p> <p> <b>Importante</b>: No se admite la asignación de valores a la metaetiqueta de URL predefinida. </p> <p>Para todas las demás asignaciones, se generan etiquetas <span class="codeph"> &lt;meta&gt; </span> para cada campo que tenga datos encontrados en el documento original. </p> <p>Los campos de cada documento se añaden a la caché. Para cada documento que se escribe en la caché, también se genera un vínculo como en los ejemplos siguientes: </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>La asignación de la configuración debe tener un campo identificado como Clave principal. Esta asignación forma la clave que se utiliza cuando se recuperan datos de la caché. </p> <p>El rastreador reconoce el índice de la dirección URL <span class="codeph">: </span> prefijo de esquema, que puede acceder a los datos almacenados en caché localmente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Rastrear el conjunto de documentos en caché. </p> </td> 
   <td colname="col3"> <p>El índice <span class="codeph">: Los </span> vínculos se agregan a la lista pendiente del rastreador y se procesan en la secuencia de rastreo normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Procese cada documento. </p> </td> 
   <td colname="col3"> <p>El valor de clave de cada vínculo corresponde a una entrada de la caché, por lo que al rastrear cada vínculo, los datos de ese documento se recuperan de la caché. A continuación, se "integra" en una imagen HTML que se procesa y se añade al índice. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cómo funciona el proceso de indexación para las configuraciones XML en el conector de índice {#section_7F1551EA51854C5C99F284CE260526EB}

El proceso de indexación para la configuración XML es similar al proceso para las configuraciones de texto y fuente con los siguientes cambios y excepciones menores.

Debido a que los documentos para los rastreos XML ya están separados en archivos individuales, los pasos 1 y 2 de la tabla anterior no se aplican directamente. Si especifica una dirección URL en los campos **[!UICONTROL Host Address]** y **[!UICONTROL File Path]** de la página [!DNL Index Connector Add], se descarga y procesa como documento HTML normal. Se espera que el documento de descarga contenga una colección de vínculos `<a href="{url}"...`, cada uno de los cuales apunta a un documento XML que se procesa. Estos vínculos se convierten al siguiente formulario:

```
<a href="index:<ic_config_name>?url="{url}">
```

Por ejemplo, si la configuración de Adobe devolvía los siguientes vínculos:

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

En la tabla anterior, el paso 3 no se aplica y el paso 4 se completa en el momento del rastreo y la indexación.

De lo contrario, puede combinar los documentos XML con otros documentos que se hayan descubierto de forma natural a través del proceso de rastreo. En estos casos, puede utilizar reglas de reescritura ( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**) para cambiar las direcciones URL de los documentos XML y dirigirlos al conector de índice.

Consulte [Acerca de las reglas de recuperación de listas arrastradas](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA).

Por ejemplo, se supone que tiene la siguiente regla de reescritura:

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

Esta regla traduce cualquier URL que termine con `.xml` en un vínculo de conector de índice. El rastreador reconoce y reescribe el esquema de URL `index:`. El proceso de descarga se redirige a través del servidor Apache del conector de índice en el servidor principal. Cada documento descargado se examina utilizando el mismo patrón de expresión regular que se utiliza con las fuentes. Sin embargo, en este caso, el documento HTML fabricado no se guarda en la caché. En su lugar, se entrega directamente al rastreador para el procesamiento de índices.

## Configuración de varios conectores de índice {#section_C2B14C0F06354A57AEF6238FF3814E5D}

Puede definir varias configuraciones de conector de índice para cualquier cuenta. Las configuraciones se añaden automáticamente a la lista desplegable en **[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]** como se muestra en la siguiente ilustración:

![](assets/url_entrypoints_index_connector.png)

Al seleccionar una configuración en la lista desplegable, se agrega el valor al final de la lista de puntos de entrada de URL.

>[!NOTE]
>
>Mientras que las configuraciones de conector de índice desactivadas se añaden a la lista desplegable, no se pueden seleccionar. Si selecciona la misma configuración del conector de índice por segunda vez, se añade al final de la lista y se elimina la instancia anterior.

Para especificar un punto de entrada del conector de índice para un rastreo incremental, puede agregar entradas con el siguiente formato:

```
index:<indexconnector_configuration_name>
```

El rastreador procesa cada entrada añadida si se encuentra en la página Conectores de índice y está habilitada.

Nota: Dado que la URL de cada documento se construye utilizando el nombre de configuración del conector de índice y la clave principal del documento, asegúrese de utilizar el mismo nombre de configuración del conector de índice al realizar actualizaciones incrementales. Al hacerlo, [!DNL Adobe Search&Promote] permite actualizar correctamente los documentos indexados anteriormente.

Consulte también [Acerca de los puntos de entrada de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

**El uso de mapas de configuración al añadir un conector de índice**

En el momento de agregar un conector de índice, puede utilizar la función **[!UICONTROL Setup Maps]** para descargar una muestra de la fuente de datos. Los datos se examinan para determinar la idoneidad de la indexación.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Si elige el tipo de conector de índice... </p> </th> 
   <th colname="col2" class="entry"> <p>La función de mapas de configuración... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Texto </p> </td> 
   <td colname="col2"> <p>Determina el valor del delimitador probando primero las pestañas y luego las barras verticales ( <span class="codeph"> | </span>) y finalmente comas ( <span class="codeph"> , </span>). Si ya especificó un valor de delimitador antes de hacer clic en <span class="uicontrol"> Mapas de configuración </span>, se utilizará ese valor en su lugar. </p> <p>El esquema que mejor se adapta permitirá rellenar los campos de mapa con suposiciones en los valores de campo y etiqueta adecuados. Además, se muestra un muestreo de los datos analizados. Asegúrese de seleccionar <span class="uicontrol"> Encabezados en la primera fila </span> si sabe que el archivo incluye una fila de encabezado. La función de configuración utiliza esta información para identificar mejor las entradas de mapa resultantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fuente </p> </td> 
   <td colname="col2"> <p>Descarga el origen de datos y realiza un análisis XML sencillo. </p> <p>Los identificadores XPath resultantes se muestran en las filas Tag de la tabla Map y valores similares en Fields. Estas filas solo identifican los datos disponibles y no generan las definiciones XPath más complicadas. Sin embargo, sigue siendo útil porque describe los datos XML e identifica los valores de Itemtag. </p> <p> <p>Nota:  La función de mapas de configuración descarga el origen XML completo para realizar su análisis. Si el archivo es grande, esta operación podría agotarse. </p> </p> <p>Cuando se realiza correctamente, esta función identifica todos los elementos XPath posibles, muchos de los cuales no son deseables de usar. Asegúrese de examinar las definiciones de Mapa resultantes y eliminar las que no necesite o desee. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>Descarga la dirección URL de un documento individual representativo, no la lista de vínculos principal. Este documento único se analiza utilizando el mismo mecanismo que se utiliza con las fuentes y se muestran los resultados. </p> <p>Antes de hacer clic en <span class="uicontrol"> Agregar </span> para guardar la configuración, asegúrese de volver a cambiar la dirección URL al documento de la lista de vínculos principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Importante**: Es posible que la función de mapas de configuración no funcione para grandes conjuntos de datos XML porque su analizador de archivos intenta leer todo el archivo en la memoria. Como resultado, podría experimentar una condición de falta de memoria. Sin embargo, cuando el mismo documento se procesa en el momento de la indexación, no se lee en la memoria. En su lugar, los documentos grandes se procesan &quot;sobre la marcha&quot; y no se leen en la memoria por completo primero.

**El uso de Vista previa al añadir un conector de índice**

En el momento de agregar un conector de índice, puede utilizar la función **[!UICONTROL Preview]** para validar los datos, como si lo estuviera guardando. Ejecuta una prueba con la configuración, pero sin guardar la configuración en la cuenta. La prueba accede al origen de datos configurado. Sin embargo, escribe la caché de descarga en una ubicación temporal; no entra en conflicto con la carpeta de caché principal que utiliza el rastreador de indexación.

La vista previa solo procesa un valor predeterminado de cinco documentos, tal como está controlado por Acct:IndexConnector-Preview-Max-Documents. Los documentos mostrados en la vista previa se muestran en el formulario de origen, a medida que se presentan al rastreador de indexación. La visualización es similar a la función &quot;Ver fuente&quot; de un explorador web. Puede navegar por los documentos del conjunto de vista previa utilizando vínculos de navegación estándar.

La vista previa no admite configuraciones XML porque estos documentos se procesan directamente y no se descargan en la caché.

## Adición de una definición de conector de índice {#task_96779B651A654E1F871F55D6DBBC8886}

Cada configuración de conector de índice define un origen de datos y asignaciones para relacionar los elementos de datos definidos para ese origen con los campos de metadatos del índice.

Antes de que los efectos de la definición nueva y habilitada sean visibles para los clientes, reconstruya el índice del sitio.

**Adición de una definición de conector de índice**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la página [!DNL Stage Index Connector Definitions], haga clic en **[!UICONTROL Add New Index Connector]**.
1. En la página [!DNL Index Connector Add], configure las opciones de conector que desee. Las opciones disponibles dependen del **[!UICONTROL Type]** que haya seleccionado.

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
      <td colname="col2"> <p>La fuente de los datos. El tipo de fuente de datos que seleccione afecta a las opciones resultantes que están disponibles en la página <span class="wintitle"> Agregar </span> Conector de índice. Puede elegir entre las siguientes opciones: </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Texto </span> <p>Archivos de texto plano simples, delimitados por comas, delimitados por tabulaciones u otros formatos delimitados de forma consistente. Cada línea de texto delimitada por líneas nuevas corresponde a un documento individual y se analiza utilizando el delimitador especificado. </p> <p>Puede asignar cada valor, o columna, a un campo de metadatos, al que se hace referencia en el número de columna, a partir del 1 (uno). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Fuente </span> <p>Descarga un documento XML principal que contiene varias "filas" de información. </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>Descarga un documento XML principal que contiene vínculos ( 
      <code>
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
      <td colname="col2"> <p>Activa la configuración para rastrear e indexar. O bien, puede desactivar la configuración para evitar el rastreo y la indexación. </p> <p> <b>Nota</b>: Las configuraciones del conector de índice desactivadas se omiten si se encuentran en una lista de puntos de entrada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dirección del host </p> </td> 
      <td colname="col2"> <p>Especifica la dirección del host del servidor donde se encuentran los datos. </p> <p>Si lo desea, puede especificar una ruta URI completa (Uniform Resource Identifier) al documento de origen de datos como en los ejemplos siguientes: </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p>o </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>El URI se desglosa en las entradas adecuadas para los campos Dirección de host, Ruta de archivo, Protocolo y, opcionalmente, Nombre de usuario y Contraseña. </p> <p>Especifica la dirección IP o la dirección URL del sistema host en el que se encuentra el archivo de origen de datos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al archivo de texto plano simple, delimitado por comas, delimitado por tabulaciones u otro archivo de formato delimitado por tabulaciones. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo incremental </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al archivo de texto plano simple, delimitado por comas, delimitado por tabulaciones u otro archivo de formato delimitado por tabulaciones. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones del Índice incremental. Si no se especifica ningún archivo, se utilizará el archivo que aparece en Ruta de archivo . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo vertical </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al archivo de texto plano simple, delimitado por comas, delimitado por tabulaciones u otro archivo de formato delimitado por tabulaciones que se utilizará durante una actualización vertical. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones de actualización vertical. </p> <p> <b>Nota</b>: Esta función no está activada de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Elimina la ruta del archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al archivo de texto plano simple, que contiene un valor de identificador de documento único por línea. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones del Índice incremental. Los valores que se encuentran en este archivo se utilizan para construir solicitudes de "eliminación" para eliminar documentos indexados anteriormente. Los valores de este archivo deben corresponder a los valores encontrados en los archivos de ruta de archivo completa o incremental, en la columna identificada como <span class="uicontrol"> Clave principal </span>. </p> <p> <b>Nota</b>: Esta función no está activada de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica el protocolo que se utiliza para acceder al archivo. Puede elegir entre las siguientes opciones: </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTP. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTPS. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>Debe introducir las credenciales de autenticación adecuadas para acceder al servidor FTP. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>Debe introducir las credenciales de autenticación adecuadas para acceder al servidor SFTP. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Archivo </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tiempo de espera </p> </td> 
      <td colname="col2"> <p>Especifica el tiempo de espera, en segundos, para las conexiones FTP, SFTP, HTTP o HTTPS. Este valor debe estar entre 30 y 300. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Reintentos </p> </td> 
      <td colname="col2"> <p>Especifica el número máximo de reintentos de conexiones FTP, SFTP, HTTP o HTTPS fallidas. Este valor debe estar entre 0 y 10. </p> <p>Un valor de cero (0) impedirá los intentos de reintento. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Codificación </p> </td> 
      <td colname="col2"> <p>Especifica el sistema de codificación de caracteres que se utiliza en el archivo de origen de datos especificado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Delimitador </p> </td> 
      <td colname="col2"> <p>Especifica el carácter que desea utilizar para delinear cada campo del archivo de origen de datos especificado. </p> <p>El carácter de coma ( <span class="codeph"> , </span>) es un ejemplo de delimitador. La coma actúa como delimitador de campo que ayuda a separar los campos de datos en el archivo de origen de datos especificado. </p> <p>Seleccione la pestaña <span class="uicontrol">? </span> para utilizar el carácter de tabulación horizontal como delimitador. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Encabezados en primera fila </p> </td> 
      <td colname="col2"> <p>Indica que la primera fila del archivo de origen de datos contiene solo información de encabezado, no datos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Número mínimo de documentos para la indexación </p> </td> 
      <td colname="col2"> <p>Si se establece en un valor positivo, especifica el número mínimo de registros esperados en el archivo descargado. Si se reciben menos registros, se anula la operación de índice. </p> <p> <b>Nota</b>: Esta función no está activada de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso. </p> <p> <b>Nota</b>: Esta función solo se utiliza durante las operaciones de índice completas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Especifica las asignaciones de columna a metadatos, utilizando números de columna. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Columna </span> <p> Especifica un número de columna, siendo la primera columna 1 (una). Para agregar nuevas filas de asignación para cada columna, en <span class="wintitle"> Acción </span>, haga clic en <span class="uicontrol"> + </span>. </p> <p>No es necesario hacer referencia a cada columna en el origen de datos. En su lugar, puede elegir omitir valores. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Campo </span> <p>Define el valor del atributo name que se utiliza para cada etiqueta &lt;meta&gt; generada. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Metadatos? </span> <p>Hace que <span class="uicontrol"> Field </span> se convierta en una lista desplegable desde la cual puede seleccionar campos de metadatos definidos para la cuenta actual. </p> <p>El valor <span class="uicontrol"> Field </span> puede ser un campo de metadatos no definido, si lo desea. Un campo de metadatos no definido a veces resulta útil para crear contenido utilizado por el <span class="wintitle"> script de filtrado </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Acerca del filtrado de secuencias de comandos </a>. </p> <p>Cuando el conector de índice procesa documentos XML con varias visitas en cualquier campo de mapa, los varios valores se concatenan en un solo valor en el documento en caché resultante. De forma predeterminada, estos valores se combinan con un delimitador de coma. Sin embargo, supongamos que el valor <span class="wintitle"> Field </span> correspondiente es un campo de metadatos definido. Además, ese campo tiene establecido el atributo <span class="wintitle"> Lista de permitidos </span> . En este caso, el valor de los delimitadores de lista del campo, que es el primer delimitador definido, se utiliza en la concatenación. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Clave principal  </span> <p>Solo se identifica una definición de mapa como clave principal. Este campo se convierte en la referencia única que se presenta cuando este documento se agrega al índice. Este valor se utiliza en la dirección URL del documento en el índice. </p> <p>Los valores <span class="uicontrol"> Clave principal </span> deben ser únicos en todos los documentos representados por la configuración del conector de índice; cualquier duplicado encontrado se omitirá. Si los documentos de origen no contienen un solo valor único para su uso como <span class="uicontrol"> Clave principal </span>, pero dos o más campos juntos <i>pueden</i> formar un identificador único, puede definir la <span class="uicontrol"> Clave principal </span> combinando varios valores de columna <span class="uicontrol"> con una barra vertical ("|") que delimite los valores.</span> </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> ¿Borrar HTML?  </span> <p>Cuando se selecciona esta opción, se elimina cualquier etiqueta HTML que se encuentre en los datos de este campo. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Acción </span> <p>Permite agregar filas al mapa o eliminarlas del mapa. El orden de las filas no es importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fuente de datos: Fuente</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Habilitado </p> </td> 
      <td colname="col2"> <p>Activa la configuración para rastrear e indexar. O bien, puede desactivar la configuración para evitar el rastreo y la indexación. </p> <p> <b>Nota</b>: Las configuraciones del conector de índice desactivadas se omiten si se encuentran en una lista de puntos de entrada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dirección del host </p> </td> 
      <td colname="col2"> <p>Especifica la dirección IP o la dirección URL del sistema host en el que se encuentra el archivo de origen de datos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al documento XML principal que contiene varias "filas" de información. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo incremental </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al documento XML incremental que contiene varias "filas" de información. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones del Índice incremental. Si no se especifica ningún archivo, se utilizará el archivo que aparece en Ruta de archivo . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo vertical </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al documento XML que contiene varias "filas" dispersas de información que se utilizarán durante una actualización vertical. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones de actualización vertical. </p> <p> <b>Nota</b>: Esta función no está activada de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Elimina la ruta del archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al archivo de texto plano simple, que contiene un valor de identificador de documento único por línea. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> <p>Este archivo, si se especifica, se descarga y procesa durante las operaciones del Índice incremental. Los valores que se encuentran en este archivo se utilizan para construir solicitudes de "eliminación" para eliminar documentos indexados anteriormente. Los valores de este archivo deben corresponder a los valores encontrados en los archivos de ruta de archivo completa o incremental, en la columna identificada como <span class="uicontrol"> Clave principal </span>. </p> <p> <b>Nota</b>: Esta función no está activada de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica el protocolo que se utiliza para acceder al archivo. Puede elegir entre las siguientes opciones: </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTP. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTPS. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>Debe introducir las credenciales de autenticación adecuadas para acceder al servidor FTP. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>Debe introducir las credenciales de autenticación adecuadas para acceder al servidor SFTP. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Archivo </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifica el elemento XML que puede utilizar para identificar líneas XML individuales en el archivo de origen de datos especificado. </p> <p>Por ejemplo, en el siguiente fragmento Feed de un documento XML de Adobe, el valor Itemtag es <span class="codeph"> registro </span>: </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col1"> <p>Número mínimo de documentos para la indexación </p> </td> 
      <td colname="col2"> <p>Si se establece en un valor positivo, especifica el número mínimo de registros esperados en el archivo descargado. Si se reciben menos registros, se anula la operación de índice. </p> <p> <b>Nota</b>: Esta función no está activada de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso. </p> <p> <b>Nota</b>: Esta función solo se utiliza durante las operaciones de índice completas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Permite especificar asignaciones de elementos XML a metadatos mediante expresiones XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Etiqueta </span> <p>Especifica una representación XPath de los datos XML analizados. Utilizando el documento XML de Adobe de ejemplo anterior, en la opción Itemtag , se puede asignar utilizando la siguiente sintaxis: </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La sintaxis anterior se traduce como: </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>El atributo <span class="codeph"> display url </span> del elemento <span class="codeph"> record </span> se asigna al campo de metadatos <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>El atributo <span class="codeph"> contenido </span> de cualquier elemento <span class="codeph"> meta </span> contenido dentro de un elemento <span class="codeph"> metadatos </span>, que se encuentra dentro de un elemento <span class="codeph"> registro </span>, cuyo atributo name es <span class="codeph"> título </span>, se asigna al título </span> del campo de metadatos&gt;.<span class="codeph"> </span></p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>El atributo <span class="codeph"> contenido </span> de cualquier elemento <span class="codeph"> meta </span> que se encuentre dentro de un elemento <span class="codeph"> metadatos </span> que se encuentra dentro del elemento <span class="codeph"> registro </span>, cuyo atributo name es <span class="codeph"> descripción </span>, se asigna al campo de metadatos <span class="codeph"> desc </span>. </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>El atributo <span class="codeph"> contenido </span> de cualquier elemento <span class="codeph"> meta </span> contenido dentro de un elemento <span class="codeph"> metadatos </span>, que se encuentra dentro del elemento <span class="codeph"> registro </span>, cuyo atributo name es <span class="codeph"> descripción </span>, se asigna al campo de metadatos <span class="codeph"> cuerpo </span>&gt;. </p> </li> 
      </ul> </p> <p>XPath es una notación relativamente complicada. Encontrará más información en la siguiente ubicación: </p> <p>Consulte <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Campo </span> <p>Define el valor del atributo name que se utiliza para cada etiqueta <span class="codeph"> &lt;meta&gt; </span> generada. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Metadatos? </span> <p>Hace que <span class="uicontrol"> Field </span> se convierta en una lista desplegable desde la cual puede seleccionar campos de metadatos definidos para la cuenta actual. </p> <p>El valor <span class="uicontrol"> Field </span> puede ser un campo de metadatos no definido, si lo desea. Un campo de metadatos no definido a veces resulta útil para crear contenido utilizado por el <span class="wintitle"> script de filtrado </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Acerca del filtrado de secuencias de comandos </a>. </p> <p>Cuando el conector de índice procesa documentos XML con varias visitas en cualquier campo de mapa, los varios valores se concatenan en un solo valor en el documento en caché resultante. De forma predeterminada, estos valores se combinan con un delimitador de coma. Sin embargo, supongamos que el valor <span class="wintitle"> Field </span> correspondiente es un campo de metadatos definido. Además, ese campo tiene establecido el atributo <span class="wintitle"> Lista de permitidos </span> . En este caso, el valor de los delimitadores de lista del campo, que es el primer delimitador definido, se utiliza en la concatenación. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Clave principal  </span> <p>Solo se identifica una definición de mapa como clave principal. Este campo se convierte en la referencia única que se presenta cuando este documento se agrega al índice. Este valor se utiliza en la dirección URL del documento en el índice. </p> <p>Los valores <span class="uicontrol"> Clave principal </span> deben ser únicos en todos los documentos representados por la configuración del conector de índice; cualquier duplicado encontrado se omitirá. Si los documentos de origen no contienen un solo valor único para su uso como <span class="uicontrol"> Clave principal </span>, pero dos o más campos juntos <i>pueden</i> formar un identificador único, puede definir la <span class="uicontrol"> Clave principal </span> combinando varias definiciones de etiqueta </span> con una barra vertical ("|") que delimite los valores.<span class="uicontrol"> </span></p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> ¿Borrar HTML?  </span> <p>Cuando se selecciona esta opción, se eliminan todas las etiquetas HTML que se encuentren en los datos de este campo. </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> ¿Se utiliza para la eliminación?  </span> <p>Solo se utiliza durante las operaciones de Índice incremental. Los registros que coinciden con este patrón XPath identifican los elementos que se van a eliminar. El valor <span class="uicontrol"> Clave principal </span> de cada registro de este tipo se utiliza para construir solicitudes de "eliminación", como con la Ruta de acceso del archivo de eliminación. </p> <p> <b>Nota</b>: Esta función no está activada de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Acción </span> <p>Permite agregar filas al mapa o eliminarlas del mapa. El orden de las filas no es importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fuente de datos: XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Habilitado </p> </td> 
      <td colname="col2"> <p>Activa la configuración para rastrear e indexar. O bien, puede desactivar la configuración para evitar el rastreo y la indexación. </p> <p> <b>Nota</b>: Las configuraciones del conector de índice desactivadas se omiten si se encuentran en una lista de puntos de entrada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dirección del host </p> </td> 
      <td colname="col2"> <p>Especifica la dirección URL del sistema host en el que se encuentra el archivo de origen de datos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al documento XML principal que contiene los vínculos ( 
      <code>
        &lt;a&gt; 
      </code>) a documentos XML individuales. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocolo </p> </td> 
      <td colname="col2"> <p>Especifica el protocolo que se utiliza para acceder al archivo. Puede elegir entre las siguientes opciones: </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTP. </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>Si es necesario, puede introducir las credenciales de autenticación adecuadas para acceder al servidor HTTPS. </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>Debe introducir las credenciales de autenticación adecuadas para acceder al servidor FTP. </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>Debe introducir las credenciales de autenticación adecuadas para acceder al servidor SFTP. </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> Archivo </li> 
      </ul> </p> <p> <b>Nota</b>: La configuración de Protocolo solo se utiliza cuando hay información especificada en los campos Dirección del host y/o Ruta de archivo . Los documentos XML individuales se descargan mediante HTTP o HTTPS, según sus especificaciones de URL. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifica el elemento XML que define una "fila" en el archivo de origen de datos especificado. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Permite especificar asignaciones de columna a metadatos mediante números de columna. </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> Etiqueta </span> <p>Especifica una representación XPath de los datos XML analizados. Utilizando el documento XML de Adobe de ejemplo anterior, en la opción Itemtag, puede asignarlo con la siguiente sintaxis: </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La sintaxis anterior se traduce como: </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>El atributo <span class="codeph"> display url </span> del elemento <span class="codeph"> record </span> se asigna al campo de metadatos <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>El atributo <span class="codeph"> contenido </span> de cualquier elemento <span class="codeph"> meta </span> contenido dentro de un elemento <span class="codeph"> metadatos </span>, que se encuentra dentro de un elemento <span class="codeph"> registro </span>, cuyo atributo name es <span class="codeph"> título </span>, se asigna al título </span> del campo de metadatos&gt;.<span class="codeph"> </span></p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>El atributo <span class="codeph"> contenido </span> de cualquier elemento <span class="codeph"> meta </span> que se encuentre dentro de un elemento <span class="codeph"> metadatos </span> que se encuentra dentro del elemento <span class="codeph"> registro </span>, cuyo atributo name es <span class="codeph"> descripción </span>, se asigna al campo de metadatos <span class="codeph"> desc </span>. </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>El atributo <span class="codeph"> contenido </span> de cualquier elemento <span class="codeph"> meta </span> contenido dentro de un elemento <span class="codeph"> metadatos </span>, que se encuentra dentro del elemento <span class="codeph"> registro </span>, cuyo atributo name es <span class="codeph"> descripción </span>, se asigna al campo de metadatos <span class="codeph"> cuerpo </span>&gt;. </p> </li> 
      </ul> </p> <p>XPath es una notación relativamente complicada. Encontrará más información en la siguiente ubicación: </p> <p>Consulte <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> Campo </span> <p>Define el valor del atributo name que se utiliza para cada etiqueta &lt;meta&gt; generada. </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> Metadatos? </span> <p>Hace que <span class="uicontrol"> Field </span> se convierta en una lista desplegable desde la cual puede seleccionar campos de metadatos definidos para la cuenta actual. </p> <p>El valor <span class="uicontrol"> Field </span> puede ser un campo de metadatos no definido, si lo desea. Un campo de metadatos no definido a veces resulta útil para crear contenido utilizado por el <span class="wintitle"> script de filtrado </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Acerca del filtrado de secuencias de comandos </a>. </p> <p>Cuando el conector de índice procesa documentos XML con varias visitas en cualquier campo de mapa, los varios valores se concatenan en un solo valor en el documento en caché resultante. De forma predeterminada, estos valores se combinan con un delimitador de coma. Sin embargo, supongamos que el valor <span class="wintitle"> Field </span> correspondiente es un campo de metadatos definido. Además, ese campo tiene establecido el atributo <span class="wintitle"> Lista de permitidos </span> . En este caso, el valor de los delimitadores de lista del campo, que es el primer delimitador definido, se utiliza en la concatenación. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> Clave principal  </span> <p>Solo se identifica una definición de mapa como clave principal. Este campo se convierte en la referencia única que se presenta cuando este documento se agrega al índice. Este valor se utiliza en la dirección URL del documento en el índice. </p> <p>Los valores <span class="uicontrol"> Clave principal </span> deben ser únicos en todos los documentos representados por la configuración del conector de índice; cualquier duplicado encontrado se omitirá. Si los documentos de origen no contienen un solo valor único para su uso como <span class="uicontrol"> Clave principal </span>, pero dos o más campos juntos <i>pueden</i> formar un identificador único, puede definir la <span class="uicontrol"> Clave principal </span> combinando varias definiciones de etiqueta </span> con una barra vertical ("|") que delimite los valores.<span class="uicontrol"> </span></p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> ¿Borrar HTML?  </span> <p>Cuando se selecciona esta opción, se eliminan todas las etiquetas HTML que se encuentren en los datos de este campo. </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> Acción </span> <p>Permite agregar filas al mapa o eliminarlas del mapa. El orden de las filas no es importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Haga clic en **[!UICONTROL Setup Maps]** para descargar una muestra de la fuente de datos. Los datos se examinan para determinar la idoneidad de la indexación. Esta función solo está disponible para tipos de texto y fuente.
1. (Opcional) Haga clic en **[!UICONTROL Preview]** para probar el funcionamiento real de la configuración. Esta función solo está disponible para tipos de texto y fuente.
1. Haga clic **[!UICONTROL Add]** para añadir la configuración a la página [!DNL Index Connector Definitions] y a la lista desplegable [!DNL Index Connector Configurations] en la página [!DNL URL Entrypoints].

   Consulte [Acerca de los puntos de entrada de URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).
1. En la página [!DNL Index Connector Definitions], haga clic en **[!UICONTROL rebuild your staged site index]**.
1. (Opcional) En la página [!DNL Index Connector Definitions], realice una de las acciones siguientes:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de la definición del conector de índice {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

Puede editar un conector de índice existente que haya definido.

>[!NOTE]
>
>No todas las opciones están disponibles para cambiar, como Nombre del conector de índice o Tipo de la lista desplegable [!DNL Type].

**Para editar una definición de conector de índice**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la página [!DNL Index Connector], en el encabezado de la columna [!DNL Actions], haga clic en **[!UICONTROL Edit]** para ver el nombre de la definición del conector de índice cuya configuración desee cambiar.
1. En la página [!DNL Index Connector Edit], configure las opciones que desee.

   Consulte la tabla de opciones en [Adición de una definición de conector de índice](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) En la página [!DNL Index Connector Definitions], haga clic en **[!UICONTROL rebuild your staged site index]**.
1. (Opcional) En la página [!DNL Index Connector Definitions], realice una de las acciones siguientes:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Visualización de la configuración de una definición de conector de índice {#task_D0B71A7426E54247BDB3468EC576D871}

Puede revisar los ajustes de configuración de una definición de conector de índice existente.

Una vez añadida la definición del conector de índice a la página [!DNL Index Connector Definitions], no se puede cambiar su configuración de tipo. En su lugar, debe eliminar la definición y luego agregar una nueva.

**Ver la configuración de una definición de conector de índice**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la página [!DNL Index Connector], en el encabezado de la columna [!DNL Actions], haga clic en **[!UICONTROL Edit]** para el nombre de la definición del conector de índice cuya configuración desee revisar o editar.

## Copia de una definición de conector de índice {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

Puede copiar una definición de conector de índice existente para utilizarla como base para un nuevo conector de índice que desee crear.

Al copiar una definición de conector de índice, la definición copiada se desactiva de forma predeterminada. Para habilitar o &quot;activar&quot; la definición, debe editarla desde la página [!DNL Index Connector Edit] y seleccionar **[!UICONTROL Enable]**.

Consulte [Edición de la definición de un conector de índice](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9).

**Copia de una definición de conector de índice**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la página [!DNL Index Connector], en el encabezado de la columna [!DNL Actions], haga clic en **[!UICONTROL Copy]** para obtener un nombre de definición del conector de índice cuya configuración desee duplicar.
1. En la página [!DNL Index Connector Copy], introduzca el nuevo nombre de la definición.
1. Haga clic **[!UICONTROL Copy]**.
1. (Opcional) En la página [!DNL Index Connector Definitions], realice una de las acciones siguientes:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cambio del nombre de una definición de conector de índice {#task_5132118FC21B47D99881E0ED425225D7}

Puede cambiar el nombre de una definición de conector de índice existente.

Después de cambiar el nombre de la definición, marque **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Desea asegurarse de que el nuevo nombre de definición se refleje en la lista desplegable de la página [!DNL URL Entrypoints].

Consulte [Adición de varios puntos de entrada de URL que desea indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

**Cambio del nombre de una definición de conector de índice**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la página [!DNL Index Connector], en el encabezado de la columna [!DNL Actions], haga clic en **[!UICONTROL Rename]** para obtener el nombre de definición del conector de índice que desea cambiar.
1. En la página [!DNL Index Connector Rename], introduzca el nuevo nombre de la definición en el campo [!DNL Name].
1. Haga clic **[!UICONTROL Rename]**.
1. Haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Si el nombre del conector de índice anterior está presente en la lista, elimínelo y añada la entrada con el nuevo nombre.

   Consulte [Adición de varios puntos de entrada de URL que desea indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45). 1. (Opcional) En la página [!DNL Index Connector Definitions], realice una de las acciones siguientes:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una definición de conector de índice {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

Puede eliminar una definición de conector de índice existente que ya no necesite ni utilice.

**Eliminación de una definición de conector de índice**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. En la página [!DNL Index Connector Definitions], en el encabezado de la columna [!DNL Actions], haga clic en **[!UICONTROL Delete]** para el nombre de definición del conector de índice que desea eliminar.
1. En la página [!DNL Index Connector Delete], haga clic en **[!UICONTROL Delete]**.
