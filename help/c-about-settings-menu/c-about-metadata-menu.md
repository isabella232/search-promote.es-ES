---
description: Utilice el menú Metadatos para personalizar las definiciones de búsqueda y las inyecciones de índice.
seo-description: Utilice el menú Metadatos para personalizar las definiciones de búsqueda y las inyecciones de índice.
seo-title: Acerca del menú Metadatos
solution: Target
subtopic: Metadata
title: Acerca del menú Metadatos
topic: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '8039'
ht-degree: 1%

---


# Acerca del menú Metadatos{#about-the-metadata-menu}

Utilice el menú Metadatos para personalizar las definiciones de búsqueda y las inyecciones de índice.

## Acerca de las definiciones {#concept_AE48035C210145169BE067D396975620}

Puede utilizar [!DNL Definitions] para personalizar el contenido y la relevancia de los campos de metadatos y HTML que se tienen en cuenta cuando un cliente envía una consulta de búsqueda.

Puede editar los campos que ya están predefinidos. O bien, también puede crear campos nuevos definidos por el usuario basados en el contenido de etiquetas de metadatos. Cada definición se muestra en una sola línea en la página [!DNL Staged Definitions].

Consulte también [Acerca de las Vistas de datos](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3).

## Añadir un nuevo campo de etiqueta meta {#task_6DF188C0FC7F4831A4444CA9AFA615E5}

Puede definir y agregar sus propios campos de etiqueta de metadatos.

Antes de que los clientes vean los efectos de la nueva definición de etiqueta meta, debe volver a generar el índice del sitio.

**Adición de un nuevo campo de etiqueta meta**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. En la página [!DNL Definitions], haga clic en **[!UICONTROL Add New Field]**.
1. En la página [!DNL Add Field], establezca las opciones que desee.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nombre del campo </p> </td> 
      <td colname="col2"> <p>Especifica un nombre que se utiliza para hacer referencia al campo. </p> <p>El nombre del campo debe cumplir las siguientes reglas: </p> <p> 
      <ul id="ul_D39D09CD7E7D41A59ECB6C5A6F4F263D"> 
      <li id="li_11CE852BE3C64CEF90FEC7A6E1079E13"> El nombre sólo debe contener caracteres alfanuméricos. </li> 
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> Se permiten guiones en el nombre, pero no espacios. </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> Puede introducir un nombre de hasta 20 caracteres. </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> El nombre no distingue entre mayúsculas y minúsculas, pero se muestra y almacena exactamente mientras se escribe. </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> No se pueden usar los nombres que existen en los campos predefinidos como se ve en la tabla de la página <span class="wintitle"> Definiciones escalonadas </span>. </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> No se puede utilizar la palabra "any" como valor del nombre de campo definido por el usuario. </li> 
      <li id="li_9B8287EED1784E79BFCBBBA956705CD2"> No se pueden editar los nombres de los campos predefinidos. </li> 
      </ul> </p> <p> Ejemplos de nombres de campo: </p> <p> 
      <ul id="ul_5881669913D04E35A6D4A6D31BEE7DF3"> 
        <li id="li_0AFFB8B516FE40F8A615C2F578F2CEA3"> author </li> 
        <li id="li_7F0ADFBFB21E4B84ACA8A1CEBFE344D1"> PublishDate </li> 
        <li id="li_6D1BEB3D19AC499E9227EC115AEB6296"> algo-wild </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Meta Tag Name(s) </p> </td> 
      <td colname="col2"> <p>Determina el contenido asociado al campo definido. </p> <p>La lista de nombres puede tener hasta 255 caracteres. Y, el nombre puede contener cualquier carácter permitido en el atributo name de una etiqueta meta HTML. </p> <p>Puede especificar varias etiquetas meta en una sola definición de campo. </p> <p>Los valores múltiples deben estar separados por comas y el nombre de la etiqueta meta que se encuentra más a la izquierda en cualquier página Web tiene prioridad. </p> <p>Por ejemplo, supongamos que ha definido un campo llamado "auth". El nombre del campo tiene las etiquetas meta asociadas "author, dc.author". En este caso, el contenido de la etiqueta meta "author" se indexará y buscará sobre el de "dc.author" si ambas etiquetas meta aparecen en una página web. </p> <p>Los campos definidos por el usuario deben tener al menos un nombre de etiqueta meta en su definición. Los campos predefinidos no necesitan tener una etiqueta meta asociada. Sin embargo, si se especifican una o varias etiquetas meta, el contenido de las etiquetas meta sobrescribe el origen de datos actual para cada etiqueta. </p> <p>Por ejemplo, si la etiqueta meta "dc.title" está asociada al campo predefinido "title", el contenido de la etiqueta meta "dc.title" se indexará sobre el de la etiqueta 
      <code>
        &lt;title&gt; 
      </code> para cualquier documento en particular. </p> <p>Estos son algunos ejemplos: </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc.date </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> description </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> propietarytag </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo de datos </p> </td> 
      <td colname="col2"> <p>Cada campo tiene un tipo de datos asociado, como texto, número, fecha, versión, clasificación o ubicación. Este tipo de datos determina cómo se indexa, busca y ordena el contenido del campo. </p> <p>No se puede cambiar el tipo de datos después de crear la definición del campo. </p> <p>Utilice la siguiente información para ayudarle a seleccionar el tipo de datos que es relevante para la información que contiene el campo. </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> Los campos  </span> de tipo de datos de texto se tratan como cadenas de caracteres. </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> Los campos  </span> de tipo de datos numéricos se tratan como valores numéricos enteros o de coma flotante. </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> Los campos  </span> de tipo de datos de fecha se tratan como especificadores de fecha y hora. Puede personalizar los formatos de fecha y hora permitidos al agregar o editar el nuevo campo. </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> Los campos  </span> de tipo de datos de versión se tratan como datos numéricos de forma libre. Por ejemplo, 1.2.3 ordena antes de 1.2.2. </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> Los campos  </span> de tipo de datos de clasificación se tratan del mismo modo que los campos de tipo "Número", excepto que influyen adicionalmente en los cálculos de clasificación/relevancia en los resultados de búsqueda. <p>Consulte <a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local">Acerca de reglas de clasificación </a>. </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> Los campos  </span> de tipo de datos de ubicación se tratan como una ubicación física en cualquier parte del mundo. Los formatos de ubicación permitidos son los siguientes: <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> Códigos postales de 5 o 9 dígitos en forma de DDDD o DDDDD-DDDD, donde cada "D" es de 0 a 9 dígitos. </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> Códigos de área de tres dígitos en forma de DDD. </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> Pares de latitud/longitud en la forma ±DD.DDDD±DDD.DDDD, donde el primer número especifica la latitud y el segundo número especifica la longitud. </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>listas de permitidos </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si se selecciona el tipo de datos <span class="uicontrol"> Texto </span> o <span class="uicontrol"> Número </span>. </p> <p>Indique por separado los valores delimitados en el contenido de metadatos de este campo. </p> <p>Por ejemplo, el contenido "Rojo, Amarillo, Verde, Azul" se trata como cuatro valores distintos en lugar de uno cuando se selecciona "Listas de permitidos". Este tratamiento resulta más útil con la búsqueda de rango (mediante 
      <code>
        sp_q_min 
      </code>, 
      <code>
        sp_q_max 
      </code> o 
      <code>
        sp_q_exact 
      </code>) y con la variable 
      <code>
        &lt;search-field-value-list&gt; 
      </code>, 
      <code>
        &lt;search-field-values&gt; 
      </code> y 
      <code>
        &lt;search-display-field-values&gt; 
      </code>. </p> <p>No disponible si se selecciona el tipo de datos Versión. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Faceta dinámica </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>Nota: Esta característica no está activada de forma predeterminada. Póngase en contacto con el servicio de asistencia técnica para activarlo para su uso. Una vez activado, aparece en la interfaz de usuario. </p> </p> <p>Establece la faceta identificada como dinámica. </p> <p>Las facetas se crean sobre los campos de etiquetas meta. Un campo de etiqueta meta es una capa de búsqueda básica de bajo nivel de Search&amp;Promote de Adobe. Por otro lado, las facetas son parte de GS (Búsqueda guiada): la capa de presentación de alto nivel de Search&amp;Promote de Adobe. Sin embargo, las facetas tienen campos de etiquetas meta propios, los campos de etiquetas meta no saben nada acerca de las facetas. </p> <p>Consulte <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Acerca de las facetas dinámicas </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Permitir deduplicación </p> </td> 
      <td colname="col2"> <p>Marque esta opción para habilitar la deduplicación para este campo. Es decir, permita que este campo se especifique en tiempo de búsqueda mediante la variable 
        <code>
          sp_dedupe_field 
        </code> Parámetro CGI de búsqueda. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Buscar parámetros CGI </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de tabla </p> </td> 
      <td colname="col2"> <p>Asocia permanentemente el campo dado con el nombre de tabla dado. </p> <p>Cada vez que un campo de este tipo se menciona dentro de un parámetro CGI de búsqueda principal o de una etiqueta de plantilla, el nombre de la tabla se proporciona automáticamente. Esta función permite seleccionar facetas dinámicas mediante coincidencias de tabla, pero también puede utilizarla para campos de facetas no dinámicas, si lo desea. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Delimitadores de lista </p> </td> 
      <td colname="col2"> <p>Solo está disponible si se seleccionan <span class="uicontrol"> Listas de permitidos </span>. </p> <p>Especifica qué caracteres separan valores de lista individuales. Puede especificar varios caracteres, cada uno de los cuales se trata como un separador de valores. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Buscar de forma predeterminada </p> </td> 
      <td colname="col2"> <p>Cuando se selecciona, se busca en el contenido del campo incluso cuando el campo no se especifica explícitamente en una consulta de búsqueda determinada. Si anula la selección de esta opción, solo se buscará en el campo cuando se solicite. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Campo de actualización vertical </p> </td> 
      <td colname="col2"> <p> <p>Nota: Esta característica no está activada de forma predeterminada. Póngase en contacto con el servicio de asistencia técnica para activarlo para su uso. Una vez activado, aparece en la interfaz de usuario. </p> </p> <p>Define el campo identificado como un campo de actualización vertical. </p> <p>Los campos de actualización vertical son candidatos para actualizarse mediante el proceso de actualización vertical ( <span class="uicontrol"> Índice </span> &gt; <span class="uicontrol"> Actualización vertical </span>). Debido al modo en que se realizan las actualizaciones verticales, el contenido de estos campos no se puede buscar en las búsquedas de texto libre. Si activa esta opción, el contenido de este campo no se agregará al índice "palabra" durante ninguna operación de índice. También habilita la actualización de este campo durante una operación de actualización vertical. </p> <p>Para obtener más información sobre las actualizaciones verticales, consulte <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> Acerca de la actualización vertical </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Relevancia </p> </td> 
      <td colname="col2"> <p>Puede editar la relevancia de los campos predefinidos y definidos por el usuario. </p> <p>La relevancia se especifica en una escala 1-10. Un ajuste de 1 significa que es el menos relevante y 10 el más relevante. Estos valores se tienen en cuenta cuando el software considera que la consulta coincide en cada campo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Clasificación </p> </td> 
      <td colname="col2"> <p>Especifica cuándo se ordenan los resultados por el campo con nombre, a través de la variable 
        <code>
          sp_s 
        </code> Parámetro CGI de búsqueda. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Buscar parámetros CGI </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Idioma  </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si se selecciona el tipo de datos <span class="uicontrol"> Clasificación </span>, <span class="uicontrol"> Número </span> o <span class="uicontrol"> Fecha </span>. </p> <p>Controla las convenciones de idioma y configuración regional que se aplican al indizar los valores de fecha, número y clasificación de este campo. </p> <p>Puede elegir aplicar el idioma de la cuenta (Lingüística &gt; Palabras e idiomas). O bien, puede aplicar el idioma asociado al documento que contiene cada número o valor de fecha, o un idioma específico. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formato(s) de fecha </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si se selecciona el tipo de datos <span class="uicontrol"> Fecha </span>. </p> <p>Controla los formatos de fecha que se reconocen al indexar valores de fecha para este campo. </p> <p>Se proporciona una lista predeterminada de cadenas de formato de fecha para cada campo de fecha. Puede agregar a la lista o editar la lista para adaptarla a las necesidades de su propio sitio. </p> <p>Consulte <a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local"> Formatos de fecha </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formatos de fecha de prueba </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si el tipo de datos <span class="uicontrol"> Fecha </span> está seleccionado como Tipo de datos. </p> <p>Permite la previsualización de los formatos de fecha que ha especificado para asegurarse de que tienen el formato correcto. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zona horaria </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si el tipo de datos <span class="uicontrol"> Fecha </span> está seleccionado como Tipo de datos. </p> <p>Controla la zona horaria asumida que se aplica al indizar los valores de fecha de este campo que no especifican una zona horaria. </p> <p>Por ejemplo: si la zona horaria de su cuenta está configurada en "América/Los Ángeles" y selecciona <span class="uicontrol"> Usar zona horaria de la cuenta </span>, el siguiente valor de fecha meta, que no tiene una zona horaria específica, se trata como si fuera hora del Pacífico, teniendo en cuenta los ahorros de luz del día: </p> <p>&lt;meta name="dc.date" content="Mon, 05 Sep 201213:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor de clasificación menos importante </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si el tipo de datos <span class="uicontrol"> Clasificación </span> está seleccionado como Tipo de datos. </p> <p>Controla el valor de clasificación que representa la clasificación mínima de cualquier documento. </p> <p>Si las clasificaciones de documentos van de 0 para la clasificación más baja a 10 para la clasificación más alta, este valor se establece en 0. </p> <p>Si las clasificaciones de documentos van de 1 para la clasificación más alta a 10 para la clasificación más baja, este valor se establece en 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor de clasificación predeterminado </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si el tipo de datos <span class="uicontrol"> Clasificación </span> está seleccionado como Tipo de datos. </p> <p>Controla el valor de clasificación que se utiliza si un documento no contiene ninguna de las etiquetas meta definidas para este campo de clasificación. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valor de clasificación más importante </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si el tipo de datos <span class="uicontrol"> Clasificación </span> está seleccionado como Tipo de datos. </p> <p>Controla el valor de clasificación que representa la clasificación máxima de cualquier documento. </p> <p>Si las clasificaciones de documentos van de 0 para la clasificación más baja a 10 para la clasificación más alta, este valor se establece en 10. </p> <p>Si las clasificaciones de documentos van de 1 para la clasificación más alta a 10 para la clasificación más baja, este valor se establece en 1. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Unidades predeterminadas </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si el tipo de datos <span class="uicontrol"> Ubicación </span> está seleccionado como Tipo de datos. </p> <p>Controla el tratamiento de los valores de distancia para las búsquedas de proximidad. </p> <p>Si establece las unidades predeterminadas en <span class="uicontrol"> Millas </span>, cualquier criterio de distancia mínima/máxima de búsqueda de proximidad que se aplique a este campo (a través de la variable 
      <code>
        sp_q_min[_#] 
      </code> o la variable 
      <code>
        sp_q_max[_#] 
      </code> Los parámetros CGI de búsqueda) se tratan como millas, de lo contrario como kilómetros. </p> <p>Esta opción también controla las unidades de distancia predeterminadas que se aplican a la salida de la variable 
      <code>
        &lt;Search-Display-Field&gt; 
      </code> etiqueta de plantilla de resultados de búsqueda cuando se aplica a un campo de salida de búsqueda de proximidad. </p> <p>Consulte <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> Acerca de la búsqueda de proximidad </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>¿Crear descripción de rango? </p> </td> 
      <td colname="col2"> <p>Solo está disponible si <span class="uicontrol"> Número </span> está seleccionado como Tipo de datos. </p> <p>Controla la creación automática de descripciones de rango de campos para su uso con <span class="uicontrol"> Diseño </span> &gt; <span class="uicontrol"> Navegación </span> &gt; <span class="uicontrol"> Facetas </span>. </p> <p>Consulte <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local"> Acerca de las facetas </a>. </p> <p> <p>Nota:  Si este campo tiene <span class="uicontrol"> Campo de actualización vertical </span> activado, el campo de descripción del rango de campos generado se actualiza durante una actualización vertical. Sin embargo, se recomienda que el campo identificado en <span class="uicontrol"> Campo de rango </span> también tenga <span class="uicontrol"> Campo de actualización vertical </span> marcado. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Campo de rango </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si <span class="uicontrol"> Crear descripción de rango </span> está marcado. </p> <p>Campo <span class="uicontrol"> Texto </span> que se actualizará con descripciones de rango para el campo actual. Esta lista contiene todos los campos <span class="uicontrol"> Texto </span> que no se están utilizando con otros campos para la generación del rango de campos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valores de rango </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si <span class="uicontrol"> Crear descripción de rango </span> está marcado y se selecciona un elemento <span class="uicontrol"> Campo de rango </span>. </p> <p>Una lista delimitada en blanco de los puntos de datos que se utilizarán al crear las descripciones del rango de campos. Por ejemplo: </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>Puede introducir estos valores en cualquier orden. Los valores se ordenan y se eliminan los duplicados antes de guardarlos. También puede especificar valores negativos y no enteros. </p> <p>Para cada uno de los valores de este campo: 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">si el valor es menor que (&lt;) el valor más pequeño en <span class="uicontrol"> Valores de rango </span>, se utiliza el formato <span class="uicontrol"> "Menor que" </span> </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">si el valor es bueno o igual a (&gt;=) el valor más alto en <span class="uicontrol"> Valores de rango </span>, se utiliza el formato <span class="uicontrol"> "Bueno que" </span>. </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">de lo contrario, se encuentra un "rango" donde el valor del campo se encuentra entre dos <span class="uicontrol"> Valores del rango consecutivos </span> (buenos que (&gt;) el valor menor y menor o igual que (&lt;=) el valor mayor), y se utiliza el <span class="uicontrol"> Formato intermedio </span>. </li> 
    </ul> </p> <p>Por ejemplo, el conjunto de valores de ejemplo anterior definirá un conjunto de descripciones para los valores: 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">menos de 10 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">buenos iguales o iguales a 10 y menores de 20 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">buenos iguales o iguales a 20 y menores de 50 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">buenos iguales o iguales a 50 y menores de 100 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">buenos iguales o iguales a 100 y menores de 10000 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">buenos iguales o iguales a 10000 </li> 
      </ul> </p> <p>Consulte <span class="uicontrol"> Prueba con Bueno que? </span> para cambiar la forma en que se realizan estas pruebas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formato "Menor que" </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si <span class="uicontrol"> Crear descripción de rango </span> está marcado y se selecciona un elemento <span class="uicontrol"> Campo de rango </span>. </p> <p>Esta es la plantilla que se utiliza para especificar la descripción del rango para valores inferiores al valor más pequeño que se encuentra en <span class="uicontrol"> Valores del rango </span>. El valor más pequeño se representará utilizando el token de marcador de posición numérico <span class="uicontrol"> ~N~ </span>. Por ejemplo: </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>O bien: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>Normalmente, el valor tendrá el formato "tal cual", es decir, para una definición <span class="uicontrol"> Valores de rango </span> de "5 10 20" y un valor proporcionado de 1, la descripción del rango generado será simplemente algo como "Menos de 5". Si desea que sea "4.99 y inferior", establezca <span class="uicontrol"> Precision </span> en <span class="uicontrol"> 2 </span> y utilice este formato: </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p>En el formato <span class="uicontrol"> "Menor que" </span>, las letras minúsculas <span class="uicontrol"> ~n~ </span> harán que el valor se redondee <i>hacia abajo</i> según la configuración <span class="uicontrol"> Precision </span>. </p> <p>Nota: para incluir cualquier marcador de posición numérico en la descripción del rango, tal como está, especifique con un prefijo de barra invertida (\), por ejemplo <span class="uicontrol"> \~N~ </span> o <span class="uicontrol"> \~n~ </span>. Para incluir un carácter de barra invertida, especifíquelo con otra barra invertida (p. ej. <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formato intermedio </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si <span class="uicontrol"> Crear descripción de rango </span> está marcado y se selecciona un elemento <span class="uicontrol"> Campo de rango </span>. </p> <p>Esta es la plantilla que se utiliza para especificar la descripción del rango para los valores que se encuentran entre los valores más pequeños y los más altos que se encuentran en <span class="uicontrol"> Valores del rango </span>. Para el rango dado, el valor del rango inferior se representará usando el token numérico de marcador de posición <span class="uicontrol"> ~L~ </span> y el valor del rango superior se representará usando el token <span class="uicontrol"> ~H~ </span>. Por ejemplo: </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>O bien: </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>O bien: </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>Normalmente, los valores tendrán el formato "tal cual", es decir, para una definición <span class="uicontrol"> Valores de rango </span> de "5 10 20" y un valor proporcionado de 8, la descripción del rango generado sería simplemente algo como "Entre 5 y 10". Si desea que sea "Entre 5 y 9,99", con el valor más alto ajustado <i>a la baja</i>, establezca <span class="uicontrol"> Precision </span> en <span class="uicontrol"> 2 </span> y utilice este formato: </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>Del mismo modo, <span class="uicontrol"> ~L~ </span> se puede reemplazar por <span class="uicontrol"> ~l~ </span> para que el valor inferior se ajuste <i>hacia arriba</i>, también según la configuración <span class="uicontrol"> Precision </span>. Esto significa que una definición como: </p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>con un valor <span class="uicontrol"> Precision </span> de <span class="uicontrol"> 2 </span> crearía "Entre 5.01 y 10". </p> <p>La <span class="uicontrol"> ~l~ </span> minúscula hará que el valor inferior se redondee <i>hacia arriba</i> de acuerdo con la configuración <span class="uicontrol"> Precision </span> y la <span class="uicontrol"> ~h~ </span> minúscula hará que el valor más alto se redondee <i>hacia abajo</i>. </p> <p>Nota: para incluir cualquier marcador de posición numérico en la descripción del rango, tal como está, especifique con un prefijo de barra invertida (\), por ejemplo <span class="uicontrol"> \~L~ </span> o <span class="uicontrol"> \~h~ </span>. Para incluir un carácter de barra invertida, especifíquelo con otra barra invertida (p. ej. <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formato "Bueno que" </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si <span class="uicontrol"> Crear descripción de rango </span> está marcado y se selecciona un elemento <span class="uicontrol"> Campo de rango </span>. </p> <p>Es la plantilla que se utiliza para especificar la descripción del rango para los valores buenos que no sean el valor más alto encontrado en <span class="uicontrol"> Valores del rango </span>. El valor más alto se representará utilizando el token de marcador de posición numérico <span class="uicontrol"> ~N~ </span>. Por ejemplo: </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>O bien: </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>Normalmente, el valor tendrá el formato "tal cual", es decir, para una definición <span class="uicontrol"> Valores de rango </span> de "5 10 20" y un valor proporcionado de 30, la descripción del rango generado sería simplemente algo así como "Bueno que 20". Si desea que sea "20.01 y superior", establezca <span class="uicontrol"> Precision </span> en <span class="uicontrol"> 2 </span> y utilice este formato: </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p>En el formato <span class="uicontrol"> "Bueno que" </span>, las letras minúsculas <span class="uicontrol"> ~n~ </span> harán que el valor se redondee <i>hacia arriba</i> según la configuración <span class="uicontrol"> Precision </span>. </p> <p>Nota: para incluir cualquier marcador de posición numérico en la descripción del rango, tal como está, especifique con un prefijo de barra invertida (\), por ejemplo <span class="uicontrol"> \~N~ </span> o <span class="uicontrol"> \~n~ </span>. Para incluir un carácter de barra invertida, especifíquelo con otra barra invertida (p. ej. <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Precisión </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si <span class="uicontrol"> Crear descripción de rango </span> está marcado y se selecciona un elemento <span class="uicontrol"> Campo de rango </span>. </p> <p>Un valor entero que especifica el número de dígitos a la derecha de una coma decimal. Esto también controla las operaciones de redondeo. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>¿Tira ceros? </p> </td> 
      <td colname="col2"> <p>Disponible sólo si <span class="uicontrol"> Crear descripción de rango </span> está marcada, se selecciona un elemento <span class="uicontrol"> Campo de rango </span> y se establece un valor <span class="uicontrol"> Precisión </span> distinto de cero. </p> <p>¿Deberíamos mostrar "0,50" como ".50"? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>¿Quitar ceros finales? </p> </td> 
      <td colname="col2"> <p>Disponible sólo si <span class="uicontrol"> Crear descripción de rango </span> está marcada, se selecciona un elemento <span class="uicontrol"> Campo de rango </span> y se establece un valor <span class="uicontrol"> Precisión </span> distinto de cero. </p> <p>¿Deberíamos mostrar "10.00" como "10"? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>¿Mostrar miles de separadores? </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si <span class="uicontrol"> Crear descripción de rango </span> está marcado y se selecciona un elemento <span class="uicontrol"> Campo de rango </span>. </p> <p>¿Deberíamos mostrar "10000" como "10,000"? Se utilizarán valores específicos de la configuración regional. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>¿Ajustar valores cero? </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si <span class="uicontrol"> Crear descripción de rango </span> está marcado y se selecciona un elemento <span class="uicontrol"> Campo de rango </span>. </p> <p>Cuando se muestran valores de cero redondeados, ¿se deben redondear hacia arriba o hacia abajo según la configuración <span class="uicontrol"> Precisión </span>? es decir, mostrar "0.01"? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>¿Desea realizar la prueba utilizando Bueno que? </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si <span class="uicontrol"> Crear descripción de rango </span> está marcado y se selecciona un elemento <span class="uicontrol"> Campo de rango </span>. </p> <p>Dado que cada valor se compara con los valores de <span class="uicontrol"> Valores de rango </span>, procesados en orden <i><b>descendente</b></i>, se compara, de forma predeterminada, usando el operador Bueno que o igual (&gt;=), deteniéndose una vez que esta prueba se realiza correctamente. Esto significa que con un conjunto de <span class="uicontrol"> Valores de rango </span> como "10 20 50 100 1000", el valor 100 caerá en el rango de 100 a 1000, ya que 100 es realmente &gt;= 100. Si prefiere que caiga en el rango de 50 a 100, marque esta opción, que hará que las comparaciones utilicen el operador Bueno que (&gt;). </p> <p>Por ejemplo, para cada uno de los valores de este campo, cuando se marca esta opción: 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">si el valor es menor o igual que (&lt;=) el valor más pequeño en <span class="uicontrol"> Valores de rango </span>, se utilizará el formato <span class="uicontrol"> "Menor que" </span> </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">si el valor es bueno que (&gt;) el mayor valor en <span class="uicontrol"> Valores de rango </span>, se utilizará el formato <span class="uicontrol"> "Bueno que" </span> </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">de lo contrario, se encontrará un intervalo en el que el valor del campo se encuentra entre dos <span class="uicontrol"> Valores de rango consecutivos </span> (buenos o iguales a (&gt;=) el valor menor y menores que (&lt;) el valor mayor), y se utilizará el <span class="uicontrol"> Formato intermedio </span> </li> 
    </ul> </p> <p>y, cuando no está marcado: 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">si el valor es menor que (&lt;) el valor más pequeño en <span class="uicontrol"> Valores de rango </span>, se utilizará el formato <span class="uicontrol"> "Menor que" </span> </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">si el valor es bueno o igual a (&gt;=) el valor más alto en <span class="uicontrol"> Valores de rango </span>, se utilizará el formato <span class="uicontrol"> "Bueno que" </span> </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">de lo contrario, se encontrará un intervalo en el que el valor del campo se encuentra entre dos <span class="uicontrol"> Valores del rango consecutivos </span> (buenos que (&gt;) el valor menor y menor o igual que (&lt;=) el valor mayor), y se utilizará el <span class="uicontrol"> Formato intermedio </span> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Prueba </p> </td> 
      <td colname="col2"> <p>Sólo está disponible si <span class="uicontrol"> Crear descripción de rango </span> está marcado y se selecciona un elemento <span class="uicontrol"> Campo de rango </span>. </p> <p>Proporcione un valor numérico de muestra y presione el botón <span class="uicontrol"> Probar </span> para ver cómo se crea el campo Intervalo. La descripción del rango generado se mostrará en la ventana. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Consulte también [Añadir un nuevo campo de etiqueta meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Haga clic **[!UICONTROL Add]**.
1. (Opcional) Vuelva a generar el índice del sitio escalonado si desea realizar una previsualización de los resultados.

   Consulte [Configuración de un índice incremental de un sitio Web escalonado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) En la página [!DNL Definitions], realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de campos de etiquetas meta predefinidos o definidos por el usuario {#task_0A7657B63596421BB6DB3ED44F827AB3}

Solo se pueden editar determinados campos en etiquetas meta predefinidas o todos los campos de las etiquetas meta definidas por el usuario.

Antes de que los clientes vean los efectos de los cambios en las etiquetas meta, debe volver a generar el índice del sitio.

**Edición de campos de etiquetas meta predefinidos o definidos por el usuario**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. En la página [!DNL Definitions], en la columna [!DNL Actions] de la tabla, haga clic en **[!UICONTROL Edit]** en la fila del nombre del campo de etiqueta meta que desee cambiar.
1. En la página [!DNL Pinned Keyword Results Manager], en la tabla, haga clic en **[!UICONTROL Edit]** en la fila de la palabra clave que desee cambiar.
1. En la página [!DNL Edit Field], establezca las opciones que desee.

   Si ha elegido realizar cambios en un campo de etiqueta meta predefinido, tenga en cuenta que no todos los campos son editables.

   Consulte la tabla de opciones en [Añadir un nuevo campo de etiqueta meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Vuelva a generar el índice del sitio escalonado si desea realizar una previsualización de los resultados.

   Consulte [Configuración de un índice incremental de un sitio Web escalonado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) En la página [!DNL Definitions], realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de un campo de etiqueta meta definido por el usuario {#task_9361EF38B5E743038B6672FA6CF70FD3}

Puede eliminar un campo de etiqueta meta definido por el usuario que ya no necesite ni use.

No se pueden eliminar campos de etiqueta meta predefinidos. Sin embargo, puede editar determinados campos.

Consulte [Edición de campos de etiquetas meta predefinidos o definidos por el usuario](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3).

Antes de que los clientes vean los efectos de la etiqueta meta de eliminación, debe volver a generar el índice del sitio.

**Eliminar un campo de etiqueta meta definido por el usuario**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. En la página [!DNL Definitions], en la sección [!DNL User-defined fields] de la tabla, haga clic en **[!UICONTROL Delete]** en la fila del nombre del campo de etiqueta meta que desee eliminar.
1. En el cuadro de diálogo Confirmación, haga clic en **[!UICONTROL OK]**.
1. (Opcional) Vuelva a generar el índice del sitio escalonado si desea realizar una previsualización de los resultados.

   Consulte [Configuración de un índice incremental de un sitio Web escalonado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Opcional) En la página [!DNL Definitions], realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca de las inyecciones {#concept_DA091920671948A0A893A26B3A2FAAE5}

Puede utilizar [!DNL Injections] para insertar contenido en las páginas Web sin necesidad de editar las páginas.

Puede anexar contenido a campos indexados específicos como &quot;destinatario&quot; o &quot;cuerpo&quot;, o reemplazar contenido indexado por nuevos valores. Por ejemplo, si ha insertado contenido nuevo en el campo de etiqueta meta &quot;destinatario&quot;, esta información se trata del mismo modo que se trataría con el contenido de la página codificado. Puede editar el contenido de cualquier campo de etiqueta meta predefinido independientemente de si las páginas del sitio tienen contenido correspondiente. Por ejemplo, puede editar el contenido de los siguientes nombres de campo de etiqueta meta predefinidos:

* alt
* body
* charset
* date
* desc
* claves
* language
* Target
* title
* url

## Uso de las inyecciones de campos de prueba {#section_74939EA9E6EA4D2A92E8066B3B11CF92}

Opcionalmente, puede utilizar **[!UICONTROL Test]** en la página [!DNL Staged Injections]. Escriba un nombre de campo de prueba (por ejemplo, &quot;título&quot; o &quot;cuerpo&quot;), el valor de campo original (por ejemplo, &quot;Página de inicio&quot;) y una dirección URL de prueba del sitio web. El valor resultante se muestra para su referencia. Los valores actuales no se modifican durante la prueba.

## Uso de definiciones de inyección de campo {#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

Las definiciones de inyección tienen la siguiente forma:

```
append|replace field [regexp] URL value
```

El `append|replace`, `field`, `URL`. y `value` elementos son obligatorios. Se introduce una definición de inyección por línea. El siguiente ejemplo contiene seis definiciones de inyección diferentes.

```
replace title  https://www.yoursite.com/company/contactus.html Adobe: Contact Us 
append body https://www.yoursite.com/products/* On Sale Now! 
append target https://www.yoursite.com/news/bob_white/ Regular Weekly Feature 
append target regexp https://www.yoursite.com/travel/mr_travel/.*\column.html$ Regular Weekly Feature 
replace charset https://www.yoursite.com/japanese/intro.txt shift-jis 
replace language https://www.yoursite.com/japanese/intro.txt ja_JP
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Definición de inyección </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> append|replace  </span> </p> </td> 
   <td colname="col2"> <p>Elija "anexar" para agregar el valor de la definición de inyección ("Adobe: Contáctenos" o "¡En venta ahora!" en los ejemplos anteriores) al contenido de los campos existentes. Elija "reemplazar" para sobrescribir el contenido del campo existente con el valor definido. Si un campo no tiene contenido actualmente, el valor definido se agrega automáticamente, independientemente de la opción (anexar o reemplazar) que se utilice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> field  </span> </p> </td> 
   <td colname="col2"> <p>Se requiere un nombre de campo. Los siguientes son diez nombres de campo predefinidos que puede utilizar: </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> alt  </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> body </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> date </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desc  </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> claves  </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> language </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> destinatario  </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> title </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url </span> </li> 
     </ul> </p> <p>Cada nombre de campo corresponde a los elementos de las páginas del sitio. Si especifica el nombre del campo <span class="codeph"> desc </span> por ejemplo, puede agregar el valor de definición de inyección al campo que corresponde a las etiquetas Meta de descripción en las páginas del sitio. </p> <p>Si no hay ninguna etiqueta Meta de descripción en las páginas, el contenido definido crea la etiqueta por usted. El contenido especificado en una inyección de <span class="codeph"> desc </span> se muestra en la página de resultados del mismo modo que el contenido de Meta-description codificado. </p> <p>También puede crear varias definiciones con el mismo nombre de campo. Por ejemplo, se supone que tiene las siguientes inyecciones: </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>Todas las páginas del sitio en el ejemplo anterior reciben un título insertado "Bienvenido a mi sitio". Las páginas de la carpeta "/compañía/" se insertan con un nuevo título "Mi sitio: Contáctenos" que sustituye al anterior. </p> <p>Observe que las inyecciones se aplican en el orden en que aparecen en el cuadro de texto <span class="wintitle"> Definiciones de inyección de campo </span>. Si el mismo campo ("título" en este ejemplo) se define más de una vez para las páginas en la misma ubicación, la definición posterior tiene prioridad. </p> <p> <span class="codeph"> [regexp]  </span> - opcional. Si decide utilizar la opción <span class="codeph"> regexp </span>, la dirección URL definida se tratará como una expresión normal. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expresiones regulares </a>. </p> <p>En la siguiente definición: </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> "Información importante" se inserta en el campo "destinatario" en todas las páginas que coinciden con la expresión regular <span class="codeph"> ^.*/informe de productos/.*\.html$ </span>. </p> <p>Por lo tanto, tiene lo siguiente: </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>En el siguiente ejemplo: </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>La inyección añade "Millennium Science" al contenido "title" de todas las páginas que finalizan con una extensión de nombre de archivo ".pdf". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Dirección URL </span> </p> </td> 
   <td colname="col2"> <p>Se requiere una dirección URL y especifica qué documentos se insertan. </p> <p>La dirección URL es cualquiera de los siguientes: </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> Una ruta completa, como en https://www.mydomain.com/products.html </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> Una ruta parcial, como en https://www.mydomain.com/products </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> Dirección URL que utiliza comodines, como en https://www.mydomain.com/*.html </li> 
     </ul> </p> <p>El valor de la dirección URL no debe contener caracteres de espacio. Si se utiliza la opción <span class="codeph"> regexp </span>, la dirección URL se trata como una expresión normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>Se requiere un valor que se utiliza para reemplazar o agregar contenido de campo existente. Puede especificar varios valores para el mismo nombre de campo. Por ejemplo: </p> <p>anexe <b>claves</b> https://www.mysite.com/travel/ <b>verano</b>, <b>playa</b>, <b>arena</b> </p> <p>anexar <b>claves</b> https://www.mysite.com/travel/fare/*.html <b>tickets baratos</b> </p> <p>En el ejemplo anterior, las palabras "verano, playa, arena" se anexan al campo "claves" en todas las páginas del directorio "/travel/". Las palabras "billetes baratos" también se anexan al campo "claves" en todas las páginas del directorio "/travel/fare/". </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte también [Selección de tipos de contenido para rastrear e indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

## Añadiendo definiciones de inyección de campo {#task_E86566FA1FF74CF68115C0ADA05172AE}

Puede utilizar [!DNL Injections] para insertar contenido en las páginas Web sin necesidad de editar las páginas.

Opcionalmente, puede utilizar **[!UICONTROL Test]** en la página [!DNL Injections]. Escriba un nombre de campo de prueba (por ejemplo, &quot;título&quot; o &quot;cuerpo&quot;), el valor de campo original (por ejemplo, &quot;Página de inicio&quot;) y una dirección URL de prueba del sitio web. El valor resultante se muestra para su referencia. Los valores actuales no se modifican durante la prueba.

**Agregar definiciones de inyección de campo**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**.
1. (Opcional) En la página [!DNL Injections], en el área [!DNL Test Field Injections], introduzca el campo de prueba, el valor original de la prueba y la dirección URL de la prueba y, a continuación, haga clic en **[!UICONTROL Test]**.
1. En el campo [!DNL Field Injection Definitions], introduzca una definición de inyección por línea.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice cualquiera de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Acerca del cargador de atributos {#concept_9EF38E98811B42CDA41996432B9AD209}

Utilice [!DNL Attribute Loader] para definir fuentes de entrada adicionales para aumentar los datos rastreados desde un sitio Web.

>[!NOTE]
>
>Para utilizar el cargador de atributos, es posible que deba habilitarlo en su cuenta por parte del representante de cuentas de Adobe o de la asistencia de Adobes.

Puede utilizar un origen de entrada de fuente de datos para acceder al contenido almacenado en un formulario distinto del que se suele descubrir en un sitio web. Esto se realiza mediante uno de los métodos de rastreo disponibles. Los datos de estas fuentes se pueden insertar en los datos de contenido rastreado.

Después de agregar una definición de cargador de atributos a la página [!DNL Staged Attribute Loader Definitions], puede cambiar cualquier configuración excepto los valores Nombre y Tipo

La página [!DNL Attribute Loader] muestra la siguiente información:

* Nombre de la configuración definida del cargador de atributos que ha configurado y agregado.
* Uno de los siguientes tipos de fuentes de datos para cada conector que ha agregado:

   * **Texto** : archivos sencillos &quot;planos&quot;, delimitados por comas, delimitados por tabuladores u otros formatos delimitados de forma consistente.
   * **Fuente** : fuentes XML.

* Indica si la configuración está habilitada o no para el siguiente rastreo e indexación.
* La dirección del origen de datos.

Consulte también [Cómo funciona el proceso de inyección de atributos para Texto y fuente...](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

Consulte también [Acerca de la configuración de varios cargadores de atributos](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)

Consulte también [Acerca del uso de la Previsualización al agregar un atributo...](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)

## Cómo funciona el proceso de inyección de atributos para las configuraciones de texto y fuente en el cargador de atributos {#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p>Para <span class="uicontrol"> texto </span>, cada línea de texto delimitada por líneas nuevas corresponde a un documento individual y se analiza utilizando el delimitador especificado, como una coma o una tabulación. </p> <p>Para <span class="uicontrol"> Fuente </span>, los datos de cada documento se extraen usando un patrón de expresión regular en el siguiente formulario: </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>Mediante <span class="uicontrol"> Asignar </span> en la página <span class="wintitle"> Loader de atributos Añadir </span>, cree una copia en caché de los datos y luego cree una lista de vínculos para el buscador. Los datos se almacenan en una caché local y se rellenan con los campos configurados. </p> <p>Los datos analizados se escriben en la caché local. </p> <p>Esta caché se lee más tarde para crear los documentos HTML simples que necesita el rastreador. Por ejemplo, </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>El elemento <span class="codeph"> &lt;title&gt; </span> sólo se genera cuando existe una asignación al campo de metadatos Título. Del mismo modo, el elemento <span class="codeph"> &lt;body&gt; </span> sólo se genera cuando existe una asignación al campo de metadatos Body. </p> <p> <b>Importante</b>: No se admite la asignación de valores a la etiqueta meta de URL predefinida. </p> <p>Para todas las demás asignaciones, se generan etiquetas <span class="codeph"> &lt;meta&gt; </span> para cada campo que tiene datos encontrados en el documento original. </p> <p>Los campos de cada documento se agregan a la caché. Para cada documento que se escribe en la caché, también se genera un vínculo como en los siguientes ejemplos: </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>La asignación de la configuración debe tener un campo identificado como Clave principal. Esta asignación forma la clave que se utiliza cuando se recuperan datos de la caché. </p> <p>El buscador reconoce el índice de la dirección URL <span class="codeph">: </span> prefijo de esquema, que luego puede acceder a los datos almacenados en caché localmente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Arrastre el conjunto de documentos en caché. </p> </td> 
   <td colname="col3"> <p>El índice <span class="codeph">: Los vínculos </span> se agregan a la lista pendiente del rastreador y se procesan en la secuencia de rastreo normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Procese cada documento. </p> </td> 
   <td colname="col3"> <p>El valor clave de cada vínculo corresponde a una entrada de la caché, por lo que al rastrear cada vínculo se obtienen los datos de ese documento de la caché. Luego se "integra" en una imagen HTML que se procesa y se agrega al índice. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Acerca de la configuración de varios cargadores de atributos {#section_4CC49C74EF294608A184E233F215ADFF}

Puede definir varias configuraciones del cargador de atributos para cualquier cuenta.

Al agregar un cargador de atributos, puede utilizar opcionalmente la función **[!UICONTROL Setup Maps]** para descargar una muestra del origen de datos. Se examinan los datos para determinar su idoneidad.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Tipo de cargador de atributos </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Texto </p> </td> 
   <td colname="col2"> <p>Determina el valor del delimitador probando las fichas primero y luego las barras verticales ( <span class="codeph"> | </span>), y finalmente comas ( <span class="codeph"> , </span>). Si ya especificó un valor delimitador antes de hacer clic en <span class="uicontrol"> Mapas de configuración </span>, se utilizará ese valor en su lugar. </p> <p>El mejor ajuste resulta en que los campos de mapa se rellenen con suposiciones en los valores de etiqueta y campo correspondientes. Además, se muestra un muestreo de los datos analizados. Asegúrese de seleccionar <span class="uicontrol"> Encabezados en Primera fila </span> si sabe que el archivo incluye una fila de encabezado. La función de configuración utiliza esta información para identificar mejor las entradas de mapa resultantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fuente </p> </td> 
   <td colname="col2"> <p>Descarga el origen de datos y realiza un análisis XML sencillo. </p> <p>Los identificadores XPath resultantes se muestran en las filas Tag de la tabla Map y valores similares en Fields. Estas filas sólo identifican los datos disponibles y no generan las definiciones XPath más complicadas. Sin embargo, sigue siendo útil porque describe los datos XML e identifica Itemtag. </p> <p> <p>Nota:  La función de mapas de configuración descarga el origen XML completo para realizar su análisis. Si el archivo es grande, esta operación podría agotarse. </p> </p> <p>Cuando se realiza correctamente, esta función identifica todos los elementos XPath posibles, muchos de los cuales no son deseables de usar. Asegúrese de examinar las definiciones de mapa resultantes y eliminar las que no necesita o desea. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Es posible que la función de mapas de configuración no funcione para grandes conjuntos de datos XML porque el analizador de archivos intenta leer todo el archivo en la memoria. Como resultado, podría experimentar una condición de memoria insuficiente. Sin embargo, cuando se procesa el mismo documento en el momento de la indexación, no se lee en la memoria. En cambio, los documentos grandes se procesan &quot;sobre la marcha&quot; y no se leen en la memoria en primer lugar.

## Acerca del uso de la Previsualización al agregar un cargador de atributos {#section_E9CAB000A94C4D9189786C1EDB1CDB46}

Los datos del cargador de atributos se cargan antes de una operación de índice.

En el momento de agregar un cargador de atributos, puede utilizar opcionalmente la función **[!UICONTROL Preview]** para validar los datos, como si lo estuviera guardando. Ejecuta una prueba con la configuración, pero sin guardar la configuración en la cuenta. La prueba accede al origen de datos configurado. Sin embargo, escribe la caché de descarga en una ubicación temporal; no entra en conflicto con la carpeta de caché principal que utiliza el buscador de indexación.

Previsualización sólo procesa un valor predeterminado de cinco documentos, como se controla con **Acct:IndexConnector-Previsualización-Max-Documentos**. Los documentos previsualizados se muestran en el formulario de origen, a medida que se presentan en el buscador de indexación. La visualización es similar a una función &quot;Origen de Vista&quot; en un explorador Web. Puede desplazarse por los documentos del conjunto de previsualizaciones mediante los vínculos de navegación estándar.

Previsualización no admite configuraciones XML porque estos documentos se procesan directamente y no se descargan en la memoria caché.

## Añadir una definición de cargador de atributos {#task_A735E5EF763343A9B675E1A3B09AFDBC}

Cada configuración del cargador de atributos define un origen de datos y asignaciones para relacionar los elementos de datos definidos para ese origen con los campos de metadatos del índice.

>[!NOTE]
>
>Para utilizar el cargador de atributos, es posible que deba habilitarlo en su cuenta por parte del representante de cuentas de Adobe o de la asistencia de Adobes.

Antes de que los clientes vean los efectos de la definición nueva y habilitada, vuelva a generar el índice del sitio.

**Adición de una definición de cargador de atributos**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. En la página [!DNL Stage Attribute Loader Definitions], haga clic en **[!UICONTROL Add New Attribute Loader]**.
1. En la página [!DNL Attribute Loader Add], establezca las opciones de configuración que desee. Las opciones disponibles dependen del **[!UICONTROL Type]** que haya seleccionado.

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
      <td colname="col2"> <p>Nombre exclusivo de la configuración del cargador de atributos. Puede utilizar caracteres alfanuméricos. También se permiten los caracteres "_" y "-". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo  </p> </td> 
      <td colname="col2"> <p>La fuente de los datos. El tipo de fuente de datos que seleccione afecta a las opciones resultantes que están disponibles en la página <span class="wintitle"> Añadir </span> cargador de atributos. Puede elegir entre las opciones siguientes: </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Texto </span> <p>Archivos de texto planos sencillos, delimitados por comas, delimitados por tabuladores u otros formatos delimitados de forma consistente. Cada nueva línea de texto delimitada por líneas corresponde a un documento individual y se analiza utilizando el delimitador especificado. </p> <p>Puede asignar cada valor, o columna, a un campo de metadatos, al que se hace referencia mediante el número de columna, comenzando en 1 (uno). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Fuente </span> <p>Descarga un documento XML principal que contiene varias "filas" de información. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fuente de datos: Texto</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Habilitado </p> </td> 
      <td colname="col2"> <p>Activa la configuración para su uso. O bien, puede desactivar la configuración para evitar que se utilice. </p> <p> <b>Nota</b>: Se omiten las configuraciones deshabilitadas del cargador de atributos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dirección del host </p> </td> 
      <td colname="col2"> <p>Especifica la dirección del host del servidor donde se ubican los datos. </p> <p>Si lo desea, puede especificar una ruta URI completa (identificador uniforme de recursos) al documento de origen de datos como en los siguientes ejemplos: </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>o </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>El URI se desglosa en las entradas correspondientes para los campos Dirección del host, Ruta de archivo, Protocolo y, opcionalmente, Nombre de usuario y Contraseña </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al archivo de texto plano simple, delimitado por comas, delimitado por tabuladores u otro archivo de formato delimitado por tabuladores. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> </td> 
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
      <td colname="col2"> <p>Especifica el carácter que desea utilizar para delimitar cada campo del archivo de origen de datos especificado. </p> <p>El carácter de coma ( <span class="codeph"> , </span>) es un ejemplo de delimitador. La coma actúa como delimitador de campo que ayuda a separar los campos de datos en el archivo de origen de datos especificado. </p> <p>Seleccione la ficha <span class="uicontrol">? </span> para utilizar el carácter de tabulación horizontal como delimitador. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Encabezados en primera fila </p> </td> 
      <td colname="col2"> <p>Indica que la primera fila del archivo de origen de datos contiene sólo información de encabezado, no datos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Días antiguos </p> </td> 
      <td colname="col2"> <p>Establece el intervalo mínimo entre las descargas de datos del cargador de atributos. Las descargas desencadenadas por índices que se producen dentro del intervalo de frecuencia de actualización de la descarga se omiten. Cuando este valor se establece en el valor predeterminado de 1, los datos del cargador de atributos no se descargan más de una vez en un período de 24 horas. Todos los índices de búsqueda que se producen dentro del intervalo de frecuencia de actualización de la descarga utilizan el último conjunto de datos que se descargó. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Especifica las asignaciones de columna a metadatos mediante números de columna. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Columna </span> <p> Especifica un número de columna, siendo la primera columna 1 (una). Para agregar nuevas filas de mapa para cada columna, en <span class="wintitle"> Acción </span>, haga clic en <span class="uicontrol"> + </span>. </p> <p>No es necesario hacer referencia a cada columna en el origen de datos. En su lugar, puede omitir valores. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Campo </span> <p>Define el valor del atributo name que se utiliza para cada etiqueta &lt;meta&gt; generada. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Metadatos? </span> <p>Hace que <span class="uicontrol"> Campo </span> se convierta en una lista desplegable desde la cual puede seleccionar campos de metadatos definidos para la cuenta actual. </p> <p>El valor <span class="uicontrol"> Campo </span> puede ser un campo de metadatos no definido, si lo desea. Un campo de metadatos no definido a veces resulta útil para crear contenido utilizado por una <span class="wintitle"> secuencia de comandos de filtrado </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Acerca del filtrado de secuencias de comandos </a>. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> ¿Clave principal?  </span> <p>Solo se identifica un campo como clave principal. Este campo se utilizará como "clave externa" para hacer coincidir los datos del cargador de atributos con el documento correspondiente en el índice. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> ¿Eliminar HTML?  </span> <p>Cuando se selecciona esta opción, se eliminan todas las etiquetas HTML que se encuentren en los datos de este campo. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Acción </span> <p>Permite agregar filas al mapa o quitar filas del mapa. El orden de las filas no es importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Tipo de fuente de datos: Fuente</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Habilitado </p> </td> 
      <td colname="col2"> <p>Activa la configuración para su uso. O bien, puede desactivar la configuración para evitar que se utilice. </p> <p> <b>Nota</b>: Se omiten las configuraciones deshabilitadas del cargador de atributos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dirección del host </p> </td> 
      <td colname="col2"> <p>Especifica la dirección del host del servidor donde se ubican los datos. </p> <p>Si lo desea, puede especificar una ruta URI completa (identificador uniforme de recursos) al documento de origen de datos como en los siguientes ejemplos: </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>o </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>El URI se desglosa en las entradas correspondientes para los campos Dirección del host, Ruta de archivo, Protocolo y, opcionalmente, Nombre de usuario y Contraseña. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ruta de archivo </p> </td> 
      <td colname="col2"> <p>Especifica la ruta al documento XML principal que contiene varias "filas" de información. </p> <p>La ruta es relativa a la raíz de la dirección del host. </p> </td> 
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
      <td colname="col2"> <p>Identifica el elemento XML que puede utilizar para identificar líneas XML individuales en el archivo de origen de datos que especificó. </p> <p>Por ejemplo, en el siguiente fragmento de fuente de un documento XML de Adobe, el valor de Itemtag es <span class="codeph"> record </span>: </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; 
        &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
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
      <td colname="col1"> <p>Nombre de campo de referencia cruzada </p> </td> 
      <td colname="col2"> <p>Especifica un campo de metadatos cuyos valores se utilizan como "claves" de búsqueda en los datos de la configuración del cargador de atributos. Si no hay ningún valor seleccionado (<b>—None—</b>), los datos de esta configuración no están disponibles para su uso en cálculos de clasificación (<b>Rules</b> &gt; <b>Ranking Rules</b> &gt; <b>Edit Rules</b>). Al seleccionar un valor, los valores de este campo se utilizan para hacer referencia cruzada a los documentos de búsqueda y comercialización del sitio con los datos de esta configuración. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Días antiguos </p> </td> 
      <td colname="col2"> <p>Establece el intervalo mínimo entre las descargas de datos del cargador de atributos. Las descargas desencadenadas por índices que se producen dentro del intervalo de frecuencia de actualización de la descarga se omiten. Cuando este valor se establece en el valor predeterminado de 1, los datos del cargador de atributos no se descargan más de una vez en un período de 24 horas. Todos los índices de búsqueda que se producen dentro del intervalo de frecuencia de actualización de la descarga utilizan el último conjunto de datos que se descargó. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mapa </p> </td> 
      <td colname="col2"> <p>Permite especificar asignaciones de elementos XML a metadatos mediante expresiones XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Etiqueta </span> <p>Especifica una representación XPath de los datos XML analizados. Utilizando el documento XML de Adobe de ejemplo anterior, en la opción Itemtag, se puede asignar con la siguiente sintaxis: </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La sintaxis anterior se traduce como: </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>El atributo <span class="codeph"> display url </span> del elemento <span class="codeph"> record </span> se asigna al campo de metadatos <span class="codeph"> page-url </span>. </p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>El atributo <span class="codeph"> content </span> de cualquier elemento <span class="codeph"> meta </span> contenido que se encuentra dentro de un elemento <span class="codeph"> metadatos </span>, que se encuentra dentro de un elemento <span class="codeph"> record </span>, cuyo atributo name es <span class="codeph"> title </span>, corresponde al campo de metadatos <span class="codeph"> title </span>&gt;. </p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>El atributo <span class="codeph"> content </span> de cualquier elemento <span class="codeph"> meta </span> contenido que se encuentra dentro de un elemento <span class="codeph"> metadatos </span>, que se encuentra dentro del elemento <span class="codeph"> record </span>, cuyo atributo name es <span class="codeph"> description </span>, se asigna al campo de metadatos <span class="codeph"> desc &lt;a111111./&gt;.</span> </p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>El atributo <span class="codeph"> content </span> de cualquier elemento <span class="codeph"> meta </span> contenido que se encuentra dentro de un elemento <span class="codeph"> metadatos </span>, que se encuentra dentro del elemento <span class="codeph"> record </span>, cuyo atributo name es <span class="codeph"> description </span>, se asigna al campo de metadatos <span class="codeph"> cuerpo </span>.&gt;. </p> </li> 
        </ul> </p> <p>XPath es una notación relativamente complicada. Hay más información disponible en la siguiente ubicación: </p> <p>Consulte <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Campo </span> <p>Define el valor del atributo name que se utiliza para cada etiqueta <span class="codeph"> &lt;meta&gt; </span> generada. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Metadatos? </span> <p>Hace que <span class="uicontrol"> Campo </span> se convierta en una lista desplegable desde la cual puede seleccionar campos de metadatos definidos para la cuenta actual. </p> <p>El valor <span class="uicontrol"> Campo </span> puede ser un campo de metadatos no definido, si lo desea. Un campo de metadatos no definido a veces resulta útil para crear contenido utilizado por <span class="wintitle"> secuencia de comandos de filtrado </span>. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> Acerca del filtrado de secuencias de comandos </a>. </p> <p>Cuando el cargador de atributos procesa documentos XML con varias visitas en cualquier campo de mapa, los valores múltiples se concatenan en un solo valor en el documento en caché resultante. De forma predeterminada, estos valores se combinan con un delimitador de coma. Sin embargo, supongamos que el valor correspondiente de <span class="wintitle"> Campo </span> es un campo de metadatos definido. Además, ese campo tiene el conjunto de atributos <span class="wintitle"> Listas de permitidos </span>. En este caso, el valor Delimitadores de Lista del campo, que es el primer delimitador definido, se utiliza en la concatenación. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> ¿Clave principal?  </span> <p>Solo se identifica un campo como clave principal. Este campo se utilizará como "clave externa" para hacer coincidir los datos del cargador de atributos con el documento correspondiente en el índice. </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> ¿Eliminar HTML?  </span> <p>Cuando se selecciona esta opción, se eliminan todas las etiquetas HTML que se encuentren en los datos de este campo. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Acción </span> <p>Permite agregar filas al mapa o quitar filas del mapa. El orden de las filas no es importante. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Opcional) Haga clic en **[!UICONTROL Setup Maps]** para descargar una muestra de la fuente de datos. Se examinan los datos para determinar su idoneidad.
1. Haga clic en **[!UICONTROL Add]** para agregar la configuración a la página [!DNL Attribute Loader Definitions].
1. En la página [!DNL Attribute Loader Definitions], haga clic en **[!UICONTROL rebuild your staged site index]**.
1. (Opcional) En la página [!DNL Attribute Loader Definitions], realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una definición de cargador de atributos {#task_AA2D1B2BCAFA44A6A0C59A0318274E80}

Puede editar un cargador de atributos existente que haya definido.

>[!NOTE]
>
>Para utilizar el cargador de atributos, es posible que deba habilitarlo en su cuenta por parte del representante de cuentas de Adobe o de la asistencia de Adobes.

No todas las opciones del cargador de atributos están disponibles para que pueda cambiarlas, como el nombre del cargador de atributos o el tipo en la lista desplegable [!DNL Type].

**Para editar una definición de cargador de atributos**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. En la página [!DNL Attribute Loader], en el encabezado de columna [!DNL Actions], haga clic en **[!UICONTROL Edit]** para obtener un nombre de definición del cargador de atributos cuya configuración desee cambiar.
1. En la página [!DNL Attribute Loader Edit], configure las opciones que desee.

   Consulte la tabla de opciones en [Añadir una definición de cargador de atributos](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) En la página [!DNL Attribute Loader Definitions], haga clic en **[!UICONTROL rebuild your staged site index]**.
1. (Opcional) En la página [!DNL Attribute Loader Definitions], realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copia de una definición de cargador de atributos {#task_9B40D5ECFC81411E9480F62A0FD5F2E0}

Puede copiar una definición de cargador de atributos existente para utilizarla como base para un nuevo cargador de atributos que desee crear.

>[!NOTE]
>
>Para utilizar el cargador de atributos, es posible que deba habilitarlo en su cuenta por parte del representante de cuentas de Adobe o de la asistencia de Adobes.

Al copiar una definición de cargador de atributos, la definición copiada se desactiva de forma predeterminada. Para habilitar o &quot;activar&quot; la definición, debe editarla desde la página [!DNL Attribute Loader Edit] y seleccionar **[!UICONTROL Enable]**.

Consulte [Edición de una definición de cargador de atributos](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80).

**Para copiar una definición de cargador de atributos**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. En la página [!DNL Attribute Loader], debajo del encabezado de la columna [!DNL Actions], haga clic en **[!UICONTROL Copy]** para obtener un nombre de definición del cargador de atributos cuya configuración desee duplicado.
1. En la página [!DNL Attribute Loader Copy], introduzca el nuevo nombre de la definición.
1. Haga clic **[!UICONTROL Copy]**.
1. (Opcional) En la página [!DNL Attribute Loader Definitions], realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cambio de nombre de una definición de cargador de atributos {#task_58D5DFD7EBC04111BCB91118E4440DB4}

Puede cambiar el nombre de una definición de cargador de atributos existente.

>[!NOTE]
>
>Para utilizar el cargador de atributos, es posible que deba habilitarlo en su cuenta por parte del representante de cuentas de Adobe o de la asistencia de Adobes.

**Cambio del nombre de una definición de cargador de atributos**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. En la página [!DNL Attribute Loader], debajo del encabezado de la columna [!DNL Actions], haga clic en **[!UICONTROL Rename]** para obtener el nombre de definición del cargador de atributos que desea cambiar.
1. En la página [!DNL Attribute Loader Rename], introduzca el nuevo nombre de la definición en el campo [!DNL Name].
1. Haga clic **[!UICONTROL Rename]**.
1. (Opcional) En la página [!DNL Attribute Loader Definitions], realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cargando datos del cargador de atributos {#task_2F3C55189B0A4049AB2113F2291CC181}

Puede descargar los datos configurados del cargador de atributos en la búsqueda o comercialización del sitio.

La página [!DNL Data Load] muestra la siguiente información sobre el estado de la última operación de carga de datos del cargador de atributos:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Campo Estado </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Estado </p> </td> 
   <td colname="col2"> <p>Indica el éxito o error del último intento de carga de datos. O bien, muestra el estado de una operación de carga de datos que ya está en curso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hora de inicio </p> </td> 
   <td colname="col2"> <p>Muestra la fecha y la hora en que se inició la última operación de carga de datos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hora de detención </p> </td> 
   <td colname="col2"> <p>Muestra la fecha y hora de finalización de la última operación de carga de datos. O bien, indica que la operación de carga de datos actual aún está en curso. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Para cargar datos del cargador de atributos**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. En la página [!DNL Attribute Loader Definitions], haga clic en **[!UICONTROL Load Attribute Loader Data]**.
1. En la página **[!UICONTROL Attribute Loader Data Load]**, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Start Load]** para inicio de la operación de carga.

      Durante una operación de carga de datos, la fila **Progress** proporciona información sobre su progreso.

   * Haga clic en **[!UICONTROL Stop Load]** para detener la operación de carga.

1. Haga clic en **[!UICONTROL Close]** para volver a la página [!DNL Attribute Loader Definitions].

## Vista previa de datos del cargador de atributos {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

Puede utilizar la Previsualización para vista de los datos del cargador de atributos cargados más recientemente.

La columna Fila de la tabla muestra el número de cada fila de datos, indicando el orden original en que se cargaron los valores del cargador de atributos.

Las columnas restantes muestran los valores asociados a cada entrada.

Si la tabla está vacía, significa que aún no ha cargado ningún dato del cargador de atributos. Puede cerrar la página [!DNL Attribute Loader Data Preview] y luego cargar los datos del cargador de atributos.

Consulte [Carga de datos del cargador de atributos](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**A los datos del cargador de atributos de previsualización**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. En la página [!DNL Attribute Loader Definitions], en la columna [!DNL Actions], haga clic en **[!UICONTROL Preview]** para ver la configuración cuyos datos descargados desee vista.
1. En la página [!DNL Attribute Loader Data Preview], utilice las opciones de navegación y visualización en la parte superior e inferior de la página para realizar una vista de los datos.

   Haga clic en cualquier encabezado de columna de la tabla para ordenar los datos en orden ascendente o descendente.
1. Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Download to Desktop]** para descargar y guardar la tabla como archivo .xlt.
   * Cierre la página cuando haya terminado de obtener una vista previa de los datos del cargador de atributos y vuelva a la página que ha visto anteriormente.

## Visualización de la configuración de una definición de cargador de atributos {#task_EA99A9694FE948ADA82C1DBA0667851B}

Puede revisar la configuración de una definición de cargador de atributos existente.

Después de agregar una definición de cargador de atributos a la página [!DNL Attribute Loader Definitions], no podrá cambiar su configuración de tipo. En su lugar, debe eliminar la definición y luego agregar una nueva.

>[!NOTE]
>
>Para utilizar el cargador de atributos, es posible que deba habilitarlo en su cuenta por parte del representante de cuentas de Adobe o de la asistencia de Adobes.

**Vista de la configuración de una definición de cargador de atributos**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. En la página [!DNL Attribute Loader], bajo el encabezado de columna [!DNL Actions], haga clic en **[!UICONTROL Edit]** para obtener un nombre de definición del cargador de atributos cuya configuración desee revisar o editar.

## Visualización del registro desde la carga de datos más reciente del cargador de atributos {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

Puede utilizar [!DNL View Log] para examinar el archivo de registro de datos del cargador de atributos del proceso de descarga más reciente. También puede utilizar la vista de registro para supervisar una descarga en ejecución.

Consulte [Carga de datos del cargador de atributos](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Para vista del registro desde la carga de datos más reciente del cargador de atributos**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. En la página [!DNL Attribute Loader Definitions], haga clic en **[!UICONTROL View Log]**. Página de registro,
1. En la página [!DNL Attribute Loader Data Log], utilice las opciones de navegación y visualización en la parte superior e inferior de la página para vista de la información del registro.
1. Cuando haya terminado, cierre la página para volver a la página [!DNL Attribute Loader Definitions].

## Eliminación de una definición de cargador de atributos {#task_E8980F66888B476E98C228C1D307EDF8}

Puede eliminar una definición de cargador de atributos existente que ya no necesite ni use.

>[!NOTE]
>
>Para utilizar el cargador de atributos, es posible que deba habilitarlo en su cuenta por parte del representante de cuentas de Adobe o de la asistencia de Adobes.

**Para eliminar una definición de cargador de atributos**

1. En el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. En la página [!DNL Attribute Loader Definitions], debajo del encabezado de la columna [!DNL Actions], haga clic en **[!UICONTROL Delete]** para el nombre de definición del cargador de atributos que desee eliminar.
1. En la página [!DNL Attribute Loader Delete], haga clic en **[!UICONTROL Delete]**.
