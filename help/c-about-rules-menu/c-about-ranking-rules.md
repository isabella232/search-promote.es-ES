---
description: Puede utilizar las reglas de clasificación para controlar la posición relativa o la clasificación de los resultados de búsqueda de un cliente en función del contenido de las etiquetas meta y las métricas de Adobe Analytics relacionadas.
seo-description: Puede utilizar las reglas de clasificación para controlar la posición relativa o la clasificación de los resultados de búsqueda de un cliente en función del contenido de las etiquetas meta y las métricas de Adobe Analytics relacionadas.
seo-title: Acerca de las reglas de clasificación
solution: Target
subtopic: Ranking Rules
title: Acerca de las reglas de clasificación
topic: Rules,Site search and merchandising
uuid: 21962f9a-1d9c-442f-a6c4-5f452436c640
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '4647'
ht-degree: 0%

---


# Acerca de las reglas de clasificación{#about-ranking-rules}

Puede utilizar las reglas de clasificación para controlar la posición relativa o la clasificación de los resultados de búsqueda de un cliente en función del contenido de las etiquetas meta y las métricas de Adobe Analytics relacionadas.

## Uso de reglas de clasificación {#concept_F555C076759B4E81B925441CFE707397}

Las reglas de clasificación se definen para que afecten a la ubicación relativa de los documentos dentro de los resultados de búsqueda, según el contenido de cada documento. Puede basar las reglas de clasificación en contenido de etiquetas meta, métricas de Adobe Analytics (si la cuenta está configurada para funcionar con Adobe Analytics) o métricas de HBX de Adobe Analytics (si la cuenta está configurada para funcionar con Adobe Analytics HBX).

Puede configurar las páginas Web que contengan metaetiquetas con las características deseadas, como un determinado nombre de marca o precio, o las páginas Web que tengan indicadores de rendimiento clave de Adobe Analytics deseables, como visores únicos, para que reciban una clasificación más alta que las páginas Web que no. Las características &quot;deseables&quot; se actualizan fácilmente agregando o editando reglas de clasificación y luego volviendo a indexar su sitio web.

Si tiene más de una etiqueta meta de tipo &quot;clasificación&quot; definida, puede crear colecciones independientes de reglas para utilizarlas en el cálculo de los distintos campos de clasificación. Puede agregar un grupo de reglas de clasificación, que luego puede asignar a uno de los campos de clasificación definidos. Normalmente, los grupos de reglas contienen una o varias definiciones de reglas, pero también pueden hacer referencia a otros grupos de reglas, de modo que puede crear uno o más grupos de reglas de uso común que se comparten durante el cálculo de las distintas clasificaciones.

Consulte [Añadir un grupo de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

Un valor de clasificación positiva promueve los resultados de búsqueda hacia la parte superior; un valor de clasificación negativa baja los resultados de búsqueda hacia la parte inferior de los resultados de búsqueda. El intervalo normal para los valores de clasificación es 1,0, que es la promoción máxima dentro de los resultados de búsqueda, mientras que -1,0 es la degradación máxima. Aunque puede personalizar este rango editando el campo Clasificación en definiciones de metadatos, este tipo de personalización suele ser innecesaria.

Consulte [Acerca de las definiciones](../c-about-settings-menu/c-about-metadata-menu.md#concept_AE48035C210145169BE067D396975620).

Si ha definido más de un campo de clasificación en Configuración > Metadatos > Definiciones, tiene la opción de crear conjuntos adicionales de reglas de clasificación, uno para cada campo de clasificación. Puede definir conjuntos adicionales de reglas de clasificación sin estar directamente asociados con un campo de clasificación. Esta flexibilidad permite crear conjuntos de reglas comunes que se pueden compartir en el cálculo de uno o varios valores de clasificación.

**Importante**: Antes de utilizar las reglas de clasificación, debe completar varios pasos de configuración de cuenta.

Consulte [Configuración de la clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5)

## Configuración de la clasificación {#task_4CEBC13925B047FC95BDC217B48089C5}

Antes de utilizar las reglas de clasificación, debe completar varios pasos de configuración de cuenta.

**Para configurar la clasificación**

1. Elija una de las siguientes opciones:

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Tarea </p> </th> 
      <th colname="col2" class="entry"> <p>Configuración </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Para crear reglas de clasificación basadas en etiquetas meta </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_28ABB980143948DFA79AC4360AAB7556"> 
      <li id="li_544075CFA0964C6F8FAF7941AAA9ECCC"> En el menú del producto, haga clic en <span class="uicontrol"> Configuración </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Definiciones </span>. </li> 
      <li id="li_F237F13B89E8425080C15D3BD697652C"> En la página Definiciones, haga clic en <span class="uicontrol"> Añadir nuevo campo </span>. </li> 
      <li id="li_2A839874D71D45FEA661B3D3B8BE2A86"> En la página Añadir campo, en el campo de texto <span class="uicontrol"> Nombre de campo </span>, escriba 
      <code>
        rank 
      </code>; en el campo de texto <span class="uicontrol"> Meta Tag Name </span>, escriba 
      <code>
        rank 
      </code>; en la lista desplegable <span class="uicontrol"> Tipo de datos </span>, seleccione <span class="uicontrol"> Clasificación </span>. Deje el resto de opciones de campo tal cual. <p>Consulte el parámetro de consulta <span class="codeph"> sp_sr </span> en <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parámetros CGI de búsqueda back-end </a>. </p> </li> 
      <li id="li_8E91AF4BE51A4A41ABBF9680DDE0B7CE">Haga clic en <span class="uicontrol">Agregar </span>. </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Para crear reglas de clasificación basadas en métricas de Adobe Analytics </p> </td> 
      <td colname="col2"> <p> 
      <ol id="ol_BE57CBC303D941778B10D855ADC93C68"> 
      <li id="li_8DF5D8F924B24ECBBD2D93C76C69D00C"> Asegúrese de configurar la autenticación de Adobe Analytics desde la búsqueda o comercialización del sitio. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42" type="task" format="dita" scope="local"> Configuración de la autenticación de métricas de Adobe Analytics </a>. </p> </li> 
      <li id="li_CF7DD073FC5A432DADBD282AA8BB9920"> Seleccione y agregue un grupo de informes disponible. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0" type="task" format="dita" scope="local"> Añadir un grupo de informes de Adobe Analytics </a>. </p> </li> 
      <li id="li_9A63448577D04E028DF211D8715F943A"> Configure la lista de las métricas de Adobe Analytics que desee que estén disponibles para la creación de nuevas reglas de clasificación. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> Edición de las métricas de Adobe Analytics de un grupo de informes </a>. </p> </li> 
      <li id="li_1ACA3611D9B44AC394604CD89209C966"> Cargue las métricas iniciales de Adobe Analytics para las páginas del sitio web. <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181" type="task" format="dita" scope="local"> Carga de datos de Adobe Analytics </a>. </p> </li> 
      </ol> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Añada una o más reglas de clasificación.

   Consulte [Añadir una regla de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

1. Haga clic en **[!UICONTROL regenerate your staged site index]** para realizar un reíndice completo del sitio Web (desde **[!UICONTROL Index]** > **[!UICONTROL Full Index]**).

   Consulte [Ejecución de un índice completo de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Configuración de un índice incremental de un sitio Web escalonado](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. Compruebe los valores de la columna Clasificación en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** para verificar que las reglas de clasificación se hayan aplicado correctamente.

## Acerca de la clasificación de documentos por edad {#topic_770815CF1B2A491F83FF765871B6F1B8}

Puede clasificar un documento HTML por su edad con una función de decadencia exponencial. La velocidad de descomposición se especifica con una constante de semivida elegida, la cantidad de tiempo que debe transcurrir antes de que el valor descienda a la mitad de su valor inicial.

La clasificación de edad se basa en las dos ecuaciones siguientes:

`K = -ln(2) / H`

`RANK = e^(K * T)`

Las variables `H` y `T` son entradas para esta función: `H` es el período de semivida deseado y `T` es la edad del documento, expresada en segundos. `K` es la semivida calculada y  `RANK` es la decadencia exponencial del valor de edad especificado. El valor resultante es de 0 a 1. Un documento más reciente tiene un valor de clasificación más cercano a 1 en comparación con un documento más antiguo. En teoría, los documentos nunca deben alcanzar el valor de 0, pero los errores de redondeo pueden hacer que el resultado sea 0.

## Requisitos para utilizar la clasificación de edad {#section_D716507D589442C6B7848892BD28F966}

* Su cuenta ya debe estar configurada correctamente para la clasificación. Si no está configurado, consulte [Configuración de la clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).
* El documento HTML debe tener un campo de etiqueta meta HTML que represente su fecha de nacimiento, su inicio como una marca de hora o cualquier otro valor de fecha significativo.
* La función especial integrada, `search_get_age_rank()`, según se especifica en las páginas Añadir o Editar regla de clasificación, se utiliza para calcular la clasificación por edades de un documento. Las siguientes secciones describen en detalle el uso general de la función de clasificación por edades. También se presenta un ejemplo que muestra la función de clasificación por edad.

## Uso de search_get_age_rank () en la página Añadir regla de clasificación o en la página Editar regla de clasificación {#section_34BC5276F2AB4419AD92872A397CA0AF}

Especifique `search_get_age_rank()` como se indica a continuación:

`search_get_age_rank(Birthdate#Half_Life#Default_Rank)`

* Fecha de nacimiento: la fecha de nacimiento o de inicio del archivo debe ser una cadena con formato de fecha de acuerdo con los formatos de fecha del campo. Esta cadena con formato de fecha debe ser una referencia de campo, como en `{field_name}`.
* Half_Life: la vida media es la cantidad de tiempo que debe pasar antes de que el valor caiga a la mitad de su valor inicial. Este valor se expresa en el número de días y es un número entero o un número de coma flotante.
* Default_Rank: la clasificación predeterminada se utiliza como red de seguridad en caso de que la fecha de nacimiento no sea válida o la fecha esté en el futuro. No puede utilizar este valor predeterminado si su campo de metadatos asociado también tiene un valor predeterminado válido. El valor aquí es un número de coma flotante o un entero. Consulte a continuación las sugerencias si tiene problemas con qué valor predeterminado se está utilizando.

Consulte [Añadir una regla de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

Consulte [Edición de una regla de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275).

**Ejemplo**

En el siguiente ejemplo,

`search_get_age_rank({birthdate}#28#0.20)`

la fecha contenida en el campo `birthdate` del documento se pasa como marca de hora. La vida media es de 28 días. El valor de clasificación predeterminado es 0,20 si la fecha no es válida.

Consulte la tabla de opciones en [Añadir una regla de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

En la sección Valores/Clasificaciones de la página Añadir regla de clasificación o en la página Editar regla de clasificación, solo puede utilizar `search_get_age_rank` con reglas personalizadas. Por lo tanto, asegúrese de elegir **Personalizado** en la lista desplegable Valores/Clasificaciones. Cuando la regla utiliza la función de clasificación por edad, no se permiten espacios en la parte de valores de la regla. Asegúrese de que no hay espacios en los argumentos de función o entre ellos. Y no hay espacios entre operadores matemáticos o condicionales.

A continuación se muestra un ejemplo de una regla de valores/clasificación, una regla asociada a un campo de texto:

`regexp .* search_get_age_rank({other_field}#365#0.20)`

En este ejemplo se asume que `other_field` contiene un valor de fecha. Si este campo no es en sí mismo un campo de tipo fecha, este valor se interpreta utilizando los formatos de fecha asociados con el campo Fecha predefinido. De lo contrario, se utilizan los formatos de fecha de este campo. Esta entrada de valores/clasificación se utiliza siempre que el campo del documento, que identifica la fuente de datos de la regla, no está vacío y el valor devuelto por la función (de 0 a 1) es la clasificación asignada.

Para una regla asociada a un campo Numérico, específicamente un campo Fecha:

`9999999999 search_get_age_rank({other_field}#365#0.20)`

A medida que se procesa cada documento, el valor de `other_field` se convierte al formulario Unix &quot;epoch&quot;, utilizando las definiciones de formato de fecha del campo. Este valor se utiliza en la llamada `search_get_age_rank()`. Dado que cada valor &quot;epoch&quot; es menor que 99999999999 (por lo menos por ahora), la regla simplemente proporciona el valor devuelto de la función (de 0 a 1) como clasificación.

En los dos ejemplos anteriores, es típico que la fuente de datos de la regla sea el mismo campo que se utiliza en la función `search_get_age_rank()`: `other_field` en este caso.

## Un ejemplo de integración de la clasificación de edad en las reglas de clasificación {#section_A86D909687CC45E19D4EA7A4A9283F28}

A continuación se muestra un ejemplo de cómo se puede integrar la clasificación de edad en las reglas de clasificación. El ejemplo también muestra los resultados sin procesar de la función de clasificación por edad y los resultados de las reglas de clasificación. El ejemplo asume lo siguiente:

* Las páginas web rastreadas tienen una etiqueta meta HTML denominada &quot;cumpleaños&quot;. El contenido de esta etiqueta es una marca de hora relacionada con el documento.
* Las definiciones de metadatos tienen un campo de metadatos definido para la etiqueta de fecha de nacimiento. Este campo está configurado para el tipo &quot;date&quot;.

**Reglas de clasificación**

Consulte [Añadir un nuevo campo de etiqueta meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

Ahora agrega una nueva regla de clasificación. La regla se define para utilizar el campo &quot;fecha de nacimiento&quot; del documento. Se agrega una nueva regla de clasificación con las siguientes propiedades establecidas:

* Tipo de fuente de datos: Meta Tag
* Nombre de fuente de datos: fecha de nacimiento
* Pesos/Condiciones: 10 - Importancia máxima
* Valores/Clasificaciones: 9999999999 search_get_age_rank({fecha de nacimiento}#14#0.10)
* Clasificación predeterminada: -1

La regla hace varias cosas. El peso de la regla se establece en 10. El valor de clasificación es simplemente el resultado de la función de clasificación de edad, un valor entre 0 y 1. No se pueden usar espacios con `search_get_age_rank()`. Además, observe que el campo &quot;fecha de nacimiento&quot; está entre llaves. Por último, al guardar esta regla, las comas en la definición Valores/Clasificaciones se sustituyen por `#` caracteres; este comportamiento es normal.

**Visualización de los resultados**

Utilice la función Vista de datos para ver rápidamente los resultados de la función de clasificación por edad. Añada los campos de metadatos correspondientes. En el ejemplo, `age_val` y `myrank` son los dos campos de metadatos que deben agregarse a la Vista de datos. El campo `myrank` muestra cómo la clasificación de edad afecta los valores de clasificación. El campo `age_val` muestra la salida sin procesar de la función exponencial-decadencia de ese documento.

## Valores predeterminados {#section_CB109EF78F914E92955D512ACFC3310E}

A continuación se indican tres valores predeterminados relacionados con la función `search_get_age_rank()`:

* El valor predeterminado que se puede introducir en la función `search_get_age_rank()` misma.
* El valor de clasificación predeterminado de la regla de clasificación.
* El valor predeterminado de la definición de metadatos.

Según el lugar donde se produzca el error, puede obtener diferentes valores predeterminados.

Por ejemplo, el valor predeterminado de la definición de metadatos no debería ocurrir nunca si la clasificación y el filtrado están correctamente implementados. Este valor predeterminado es el último recurso cuando no existe contenido válido o conocido para ese campo de metadatos. El valor predeterminado de las reglas de clasificación puede aparecer cuando `search_get_age_rank()` hace referencia a su propia etiqueta asociada y la etiqueta falta en el documento. En este caso, esta regla va directamente al valor predeterminado de la regla. Si la función de clasificación por edad hace referencia a otra etiqueta de regla de clasificación, es posible que se utilice el valor predeterminado pasado a esa función de clasificación por edad si falta la etiqueta a la que se hace referencia o no es válida.

## Añadir una regla de clasificación {#task_A132789FD4E5423DAD090DCDA7311E8A}

Puede agregar [!DNL Ranking Rules] para afectar la ubicación relativa de las páginas Web dentro de los resultados de búsqueda, en base al contenido de cada página Web.

Consulte [Configuración de la clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Para agregar una regla de clasificación**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Opcional) Si ha creado un grupo de reglas y ha agregado reglas al grupo, en la página [!DNL Define Ranking Rules], en la lista desplegable **[!UICONTROL Select Rule Group]**, seleccione un grupo de reglas que contenga las reglas que desee editar.

   Consulte [Añadir un grupo de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).
1. En la página [!DNL Define Ranking Rules], haga clic en **[!UICONTROL Add Rule]** para agregar una nueva regla de clasificación o para agregar una referencia a un conjunto de reglas.
1. En la página [!DNL Add Ranking Rule], configure las opciones que desee. Los campos marcados con un asterisco (*) son obligatorios.

   El tipo de fuente de datos seleccionado afecta a las opciones disponibles en la lista desplegable [!DNL Data Source Name]. Por ejemplo: si seleccionó **[!UICONTROL Meta Tag]** como Tipo de fuente de datos, el nombre de la fuente de datos hace referencia al nombre de una etiqueta meta en las páginas del sitio web. Si seleccionó **[!UICONTROL Adobe Analytics Metric (Number)]**, el nombre de la fuente de datos hace referencia a uno de los nombres de métricas de Adobe Analytics que seleccionó en un grupo de informes, tal como se encuentra en la página **[!UICONTROL Edit Adobe Analytics Metrics]** en la búsqueda o comercialización del sitio.

   Consulte [Edición de las métricas de Adobe Analytics de un grupo de informes](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Tipo de fuente de datos </p> </td> 
      <td colname="col2"> <p>Determina las características del origen de datos que se utiliza como entrada para esta regla de clasificación. </p> <p>Los tipos de fuentes de datos que puede seleccionar incluyen lo siguiente: 
      <ul id="ul_B0A97BF0E314495985F44A642C86918D"> 
      <li id="li_4D8BDE32853540809AE78FF5FF5677A1"> <span class="uicontrol"> Meta Tag  </span> <p> Basa esta regla en datos numéricos o de texto que se almacenan en una etiqueta meta con nombre en las páginas del sitio web. </p> </li> 
      <li id="li_4976C31D67254C7F81D554EC49DDBB40"> <span class="uicontrol"> Métrica de Adobe Analytics (número)  </span> <p>Basa esta regla en una métrica numérica de Adobe Analytics asociada con las páginas del sitio. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de la fuente de datos </p> </td> 
      <td colname="col2"> <p>Si elige <span class="uicontrol"> Meta Tag </span> como Tipo de fuente de datos, éste es el nombre de una meta etiqueta que se encuentra en las páginas del sitio Web. Los nombres del menú desplegable proceden de la lista de los valores de metadatos definidos que se configuraron en Configuración &gt; Metadatos &gt; Definiciones. </p> <p>Consulte <a scope="local" href="../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5" type="task" format="dita"> Añadir un nuevo campo de etiqueta meta </a>. </p> <p>Si elige Métrica de Adobe Analytics (número) como Tipo de fuente de datos, este es el nombre de una métrica de Adobe Analytics. Los nombres del menú desplegable provienen de las métricas de Adobe Analytics disponibles definidas por la lista que se configuraron en Configuración &gt; Adobe Analytics &gt; Métricas &gt; Editar. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664" type="task" format="dita" scope="local"> Edición de las métricas de Adobe Analytics de un grupo de informes </a>. </p> <p>Si el nombre de la métrica de Adobe Analytics que ha seleccionado no está definido en <span class="uicontrol"> Configuración </span> &gt; <span class="uicontrol"> Metadatos </span> &gt; <span class="uicontrol"> Definiciones </span>, se muestra un campo de texto y un botón Añadir. Escriba el nombre del campo de metadatos (el nombre del campo de metadatos no puede exceder los 20 caracteres) y haga clic en <span class="uicontrol"> Añadir </span>. </p> <p>Cuando se encuentran páginas con varias claves de Adobe Analytics, como con una página de producto que muestra varios productos, el esquema compuesto especifica cómo tratar los valores de varias métricas de Adobe Analytics asociados con esa página. Seleccione una de las siguientes opciones: </p> <p> 
      <ul id="ul_D6E51748BB3949048A37C1895F2C0A58"> 
      <li id="li_04F00F382A264C96A519B0D975E25E94"> <span class="uicontrol"> Suma </span> <p>Devuelve la suma de los valores de la métrica. </p> </li> 
      <li id="li_FA44219B663F4CC197BD3A094EB84396"> <span class="uicontrol"> Promedio </span> <p>Devuelve el promedio de los valores (la suma dividida por el número de valores). </p> </li> 
      <li id="li_F0EAAE1EA1754FFEB30F611E5550097B"> <span class="uicontrol"> Máximo  </span> <p>Devuelve el mayor de los valores. </p> </li> 
      <li id="li_38E3E3F3D9AF4C57803B84B60223FB9D"> <span class="uicontrol"> Primero </span> <p>Devuelve el valor correspondiente a la primera clave. </p> </li> 
      <li id="li_4AEE470CE6BB4D899E975915EC226624"> <span class="uicontrol"> Última </span> <p>Devuelve el valor correspondiente a la última clave. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pesos/Condiciones </p> </td> 
      <td colname="col2"> <p>Contiene un número de peso de regla simple o una lista emparejada de números de peso y condiciones de prueba de reglas. </p> <p>Un número de peso de regla es un valor entre 1 y 10 que indica la importancia de esta regla de clasificación en relación con las demás reglas de clasificación para determinar la clasificación general de un documento. Un peso de regla más alto indica una mayor importancia. Un peso de cero (0) ignora la regla. </p> <p>Elija <span class="uicontrol"> Personalizar </span> en la lista desplegable para personalizar el peso de reglas para varias páginas mediante la definición de una lista de pares de pesos de reglas y condiciones de prueba. Las condiciones de prueba son fragmentos de Perl que se utilizan para probar los valores de la fuente de datos o variables globales que se definen en el script de filtro personalizado (por ejemplo, vistas de precio, marca, temporada o página, como en el ejemplo siguiente). Si una condición de prueba se evalúa como "true", se aplica el valor de peso de regla asociado. Si una condición de prueba se evalúa como "false", se evalúa la siguiente condición de la lista. <code> 0&nbsp;({price}&nbsp;&gt;&nbsp;50.00)&nbsp;&amp;&amp;&nbsp;({brand}=~/Kuhl/)5&nbsp;{season}&nbsp;=~&nbsp;/Fall/10&nbsp;{pageviews}&nbsp;&gt;&nbsp;1000005 </code>En el ejemplo de peso o condición creado a medida anterior, el peso de regla 0 se aplica si la primera condición de prueba se evalúa como "true". Es decir, el precio contiene un valor bueno de 50 y la marca contiene "Kuhl"). Si la primera condición de prueba se evalúa como "false", se evalúa la siguiente condición. Si no se cumple ninguna de las condiciones anteriores, se asigna el peso 5 de la regla. </p> <p>Siempre debe proporcionar un peso de regla sin condiciones al final de la lista. Si no lo hace, la regla obtiene un peso de 0 en el caso de que ninguna de las pruebas de condición se evalúe como "true". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valores/Clasificaciones </p> </td> 
      <td colname="col2"> <p>Consiste en una de las funciones de clasificación integradas o en un posible contenido de fuente de datos junto con las clasificaciones deseadas. </p> <p>Si elige <span class="uicontrol"> Métrica de Adobe Analytics (Número) </span> como Tipo de fuente de datos, se le mostrará una lista desplegable con las siguientes opciones: 
      <ul id="ul_104906B6AA8547BAB6979AA37C4FAB90"> 
      <li id="li_7656A2855A054DB8B64E90FE501517AA"> <span class="uicontrol"> Clasificación automática por pedido (predeterminado)  </span> <p>Calcula una clasificación basada en la posición relativa del documento, según su métrica de Adobe Analytics. Por ejemplo, cuanto más se acerque la posición del documento al documento de mayor clasificación, mayor será su clasificación. </p> </li> 
      <li id="li_1A7D60EA6965434AA6D39B215C158306"> <span class="uicontrol"> Clasificación automática por valor  </span> <p>Calcula una clasificación según el valor relativo del documento, según su métrica de Adobe Analytics. Por ejemplo, cuanto más se acerque el valor del documento al valor del documento de mayor clasificación, mayor será su clasificación. </p> </li> 
      <li id="li_457DE44D6ADA40619DC77220BF12318E"> <span class="uicontrol"> Personalizado </span> <p>Especifica la configuración personalizada. Por ejemplo: una fuente de datos con el nombre de "marca" puede contener el nombre de la marca de un producto en particular. Puede especificar la importancia relativa de cada marca enumerándola junto con su clasificación. </p> </li> 
      </ul> </p> <p>Los valores de clasificación devueltos por los cálculos de clasificación automática están en el rango de 0,0 (menor) a 1,0 (mayor). No se ajustan según los rangos definidos para el campo Clasificación en Configuración &gt; Metadatos &gt; Definiciones. </p> <p>En el siguiente ejemplo, si la fuente de datos de marca para un resultado de búsqueda en particular coincide exactamente con "DKNY", la clasificación aplicada para ese resultado es 0,5. De lo contrario, si la marca es "Levis", la clasificación aplicada es 0,1. El contenido de la fuente de datos debe coincidir con el valor establecido. En otras palabras, si el contenido de la fuente de datos es "Levis Corp.", no coincidirá con el valor "Levis". Se ignora el caso, por lo que "DKNY" coincide con "dkny" y "Dkny". <code> DKNY&nbsp;0.5 Levis&nbsp;0.1 Lee&nbsp;0.2 </code> </p> <p>Como opción más avanzada, puede especificar valores como expresiones regulares. Por ejemplo: supongamos que algunas de las páginas del sitio contienen un valor de marca de "Levis" y que otras páginas del sitio contienen un valor de marca de "jeans de Levis". Puede utilizar una expresión normal especificada con la palabra clave 
      <code>
        regexp 
      </code>. </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expresiones regulares </a>. </p> <p>En el siguiente ejemplo, a un documento de resultados de búsqueda que contenga contenido de marca "jeans de Levis" se le asigna una clasificación de 0,1. Al igual que con la comparación estándar, se omiten las mayúsculas y minúsculas en las expresiones regulares. <code> DKNY&nbsp;0.5 regexp&nbsp;Levis.*&nbsp;0.1 Lee&nbsp;0.2 </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Clasificación predeterminada </p> </td> 
      <td colname="col2"> <p> Especifica la clasificación que se aplicará a los documentos de resultados de búsqueda que no coincidan con ninguno de los valores especificados. En el ejemplo anterior, a un documento de resultados de búsqueda con una fuente de datos de "marca" que contenga "la brecha" se le asigna el valor de clasificación predeterminado porque "la brecha" no coincide con ninguno de los valores definidos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Notas </p> </td> 
      <td colname="col2"> <p>Añada información que se refiera a la definición de regla de clasificación o a la definición de grupo de reglas que ha creado. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   El rango de valores de clasificación válidos es normalmente de -1.0 a 1.0, como se muestra a continuación:

   * `-1.0` es &quot;Clasificación mínima (mostrar abajo en los resultados de búsqueda)&quot;.
   * `0.0` es &quot;Clasificación neutra (no cambiar el orden de los resultados de búsqueda)&quot;.
   * `1.0` es &quot;Clasificación máxima (mostrar más alto en los resultados de búsqueda).&quot;

   Las clasificaciones definidas deben estar dentro del mismo rango para cada regla. Los rangos de clasificación también deben coincidir con los rangos definidos para el campo Clasificación en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Consulte [Añadir un nuevo campo de etiqueta meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

   Consulte también [Edición de una regla de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_5EBF55A43D6545FEA46BAE5E586FA275).
1. Haga clic **[!UICONTROL Add]**.
1. Para previsualización de los resultados de la adición de la regla, haga clic en **[!UICONTROL regenerate your staged site index]** para volver a generar el índice del sitio Web escalonado.

   Consulte [Ejecución de un índice completo de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Ejecución de un índice incremental de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una regla de clasificación {#task_5EBF55A43D6545FEA46BAE5E586FA275}

Puede editar una regla de clasificación existente que ya haya agregado.

Consulte [Configuración de la clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

**Para editar una regla de clasificación**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Opcional) Si ha creado un grupo de reglas y ha agregado reglas al grupo, en la página **[!UICONTROL Define Ranking Rules]**, en la lista desplegable **[!UICONTROL Select Rule Group]**, seleccione un grupo de reglas que contenga las reglas que desee editar.

   Consulte [Añadir un grupo de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).
1. En la tabla, debajo del encabezado de columna **[!UICONTROL Actions]**, haga clic en **[!UICONTROL Edit]** para el nombre del origen de datos que desee cambiar.
1. En la página [!DNL Edit Ranking Rule], establezca las opciones que desee. Los campos marcados con un asterisco (*) son obligatorios.

   Consulte la tabla de opciones en [Añadir una regla de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).
1. Haga clic **[!UICONTROL Save Changes]**.
1. Vuelva a generar el índice del sitio web escalonado para previsualización de los resultados de la edición de la regla.

   Consulte [Ejecución de un índice completo de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Ejecución de un índice incremental de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una regla de clasificación {#task_742A3BCC2A6E4164BE84CC7408807EBB}

Puede eliminar las reglas de clasificación que ya no necesite utilizar.

Consulte [Configuración de la clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

Consulte [Añadir un grupo de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Para eliminar una regla de clasificación**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. (Opcional) Si ha creado un grupo de reglas y ha agregado reglas al grupo, en la página [!DNL Define Ranking Rules], en la lista desplegable **[!UICONTROL Select Rule Group]**, seleccione un grupo de reglas que contenga reglas que desee eliminar.
1. En la tabla, debajo del encabezado de columna **[!UICONTROL Actions]**, haga clic en **[!UICONTROL Delete]** para el nombre del origen de datos que desee cambiar.
1. En la página [!DNL Delete Ranking Rule], haga clic en **[!UICONTROL Delete]**.

   Volverá a la página [!DNL Define Ranking Rules].
1. Vuelva a compilar el índice del sitio web escalonado para previsualización de los resultados de la eliminación de la regla.

   Consulte [Ejecución de un índice completo de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Ejecución de un índice incremental de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Añadir un grupo de reglas de clasificación {#task_B65081B3CC9E4330A7FEE77B7BCD36C8}

Si ha definido más de una etiqueta meta de tipo &quot;clasificación&quot;, puede crear colecciones de reglas independientes para utilizarlas en el cálculo de los distintos campos de clasificación. Puede agregar un grupo de reglas de clasificación, que luego puede asignar a uno de los campos de clasificación definidos.

Los grupos de reglas generalmente contienen una o más reglas que se han agregado. Sin embargo, los grupos de reglas también pueden hacer referencia a otros grupos de reglas. Por ejemplo, puede crear uno o más grupos de reglas y luego agregar reglas comúnmente utilizadas a cada uno de ellos. Estas reglas se comparten durante el cálculo de las distintas clasificaciones.

Consulte [Edición de un grupo de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_D3EC0437E47144BC9E754FEF99C725E5).

Consulte [Eliminación de un grupo de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_BE5BE01F377843BEA9846E094A07F2EA).

Consulte [Revisión de los grupos de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_5694459D050C4254A25186038CD66B6E).

**Para agregar un grupo de reglas de clasificación**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. En la página [!DNL Define Ranking Rules], a la derecha de la lista desplegable **[!UICONTROL Select Rule Group]**, haga clic en **[!UICONTROL Add]**.
1. En la página [!DNL Add Ranking Rule Group], en el campo **[!UICONTROL Rule Group Name]**, escriba un nombre único para el nuevo grupo de reglas.
1. En la lista desplegable **[!UICONTROL Rank Field Name]**, seleccione un nombre de campo de metadatos de clasificación que desee asociar al nuevo grupo de reglas. Seleccione **[!UICONTROL None]** si no desea asignar una clasificación.

   La lista de los nombres de campo de clasificación proviene de definiciones de metadatos que se agregaron en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Consulte la tabla de opciones en [Añadir un nuevo campo de etiqueta meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Haga clic **[!UICONTROL Add]**.
1. Vuelva a compilar el índice del sitio web escalonado para previsualización de los resultados de la adición de la regla.

   Consulte [Ejecución de un índice completo de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Ejecución de un índice incremental de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de un grupo de reglas de clasificación {#task_D3EC0437E47144BC9E754FEF99C725E5}

Puede editar la configuración de un grupo de reglas de clasificación existente.

Consulte [Añadir un grupo de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Para editar un grupo de reglas de clasificación**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. En la página [!DNL Define Ranking Rules], a la derecha de la lista desplegable **[!UICONTROL Select Rule Group]**, haga clic en **[!UICONTROL Edit]**.
1. En la página [!DNL Edit Ranking Rule Group], en el campo **[!UICONTROL Rule Group Name]**, escriba un nombre único para el grupo de reglas.
1. En la lista desplegable **[!UICONTROL Rank Field Name]**, seleccione un nombre de campo de metadatos de clasificación que desee asociar al grupo de reglas. Seleccione **[!UICONTROL None]** si no desea asignar una clasificación.

   La lista de los nombres de campo de clasificación proviene de definiciones de metadatos que se agregaron en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.

   Consulte la tabla de opciones en [Añadir un nuevo campo de etiqueta meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Haga clic **[!UICONTROL Save Changes]**.
1. Vuelva a compilar el índice del sitio web escalonado para previsualización de los resultados de la adición de la regla.

   Consulte [Ejecución de un índice completo de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Ejecución de un índice incremental de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de un grupo de reglas de clasificación {#task_BE5BE01F377843BEA9846E094A07F2EA}

Puede eliminar un grupo de reglas de clasificación que ya no necesite ni use. Al eliminar un grupo, también se eliminan todas las reglas que se hayan agregado al grupo. No puede eliminar el grupo predeterminado &quot;Reglas de clasificación&quot;.

No se elimina el contenido de los grupos de reglas contenidos en el grupo de eliminación; solo se eliminan las referencias a estos grupos.

Asegúrese de volver a indexar el sitio web para que el cambio se refleje correctamente en los resultados de búsqueda.

Consulte [Añadir un grupo de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Para eliminar un grupo de reglas de clasificación**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. En la página [!DNL Define Ranking Rules], en la lista desplegable **[!UICONTROL Select Rule Group]**, seleccione el grupo que desee eliminar.
1. A la derecha de la lista desplegable **[!UICONTROL Select Rule Group]**, haga clic en **[!UICONTROL Delete]**.
1. En la página [!DNL Delete Ranking Rule Group], haga clic en **[!UICONTROL Delete]**.
1. Vuelva a compilar el índice del sitio web escalonado para previsualización de los resultados de la adición de la regla.

   Consulte [Ejecución de un índice completo de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Ejecución de un índice incremental de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Revisión de los grupos de reglas de clasificación {#task_5694459D050C4254A25186038CD66B6E}

Puede utilizar Información general de grupos de reglas de clasificación para ver el nombre de cada grupo Campo de clasificación y la fuente de datos y ponderación asociadas.

Consulte [Añadir un grupo de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_B65081B3CC9E4330A7FEE77B7BCD36C8).

**Para revisar los grupos de reglas de clasificación**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. En la página [!DNL Define Ranking Rules], a la derecha de la lista desplegable **[!UICONTROL Select Rule Group]**, haga clic en **[!UICONTROL Overview]**.
1. En la página [!DNL Ranking Rule Groups Overview], haga clic en **[!UICONTROL Close]** para volver a la página [!DNL Define Ranking Rules].
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Prueba de las reglas de clasificación {#task_56F64EE7ED5B42E481F0990A9DD98ADB}

Puede proporcionar una prueba de URL adecuada para las definiciones de reglas de clasificación que haya configurado. Se muestran las métricas utilizadas en los cálculos, junto con el valor de clasificación calculado.

Consulte [Acerca de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

**Para probar las reglas de clasificación**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Edit Rules]**.
1. En la página [!DNL Define Ranking Rules], en el área **[!UICONTROL Test URL]**, escriba la dirección URL de una página Web que se encuentre en el sitio Web.
1. Haga clic **[!UICONTROL Test]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Ajuste del peso asociado con las reglas de clasificación {#task_3CB6FC92A66F4D99874A42D55825DB64}

Puede cambiar las contribuciones relativas de sus reglas de clasificación individuales y la contribución de Clasificación a los resultados de búsqueda finales.

Cuando no se define la clasificación, los resultados de la búsqueda son 100% en el lado **[!UICONTROL Natural Relevance]** de la barra deslizante Reglas y relevancia en la página **[!UICONTROL Adjust Ranking Weights]**. Este balance simplemente significa que los resultados de la búsqueda se ordenan basándose únicamente en los términos de búsqueda.

Cuando se define la clasificación, al campo de metadatos de clasificación asociado se le asigna un valor de relevancia, que oscila entre 1 y 10. Un valor de 1 significa que la clasificación calculada representa el 10 % del pedido de resultados de búsqueda y la relevancia natural el 90 % restante.

Si tiene más de una regla definida en un grupo de reglas, el valor de Peso de cada regla determina en qué medida el resultado de la regla contribuye a la clasificación calculada total. Por ejemplo, supongamos que tiene una relevancia natural del 80 %, lo que significa que la relevancia del campo Clasificación asociado es 2. También ha definido dos reglas: una con un peso de 3 y la segunda con un peso de 7. En tal caso, la contribución de la primera regla al resultado final es del 6 % ((3 / (3+7)) * 20 %). La contribución de la segunda regla al resultado final es del 14 % ((7 / (3+7)) * 20 %).

**Para ajustar el peso asociado con las reglas de clasificación**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Ranking Rules]** > **[!UICONTROL Adjust Weights]**.
1. En la página [!DNL Adjust Ranking Weights], en la lista desplegable **[!UICONTROL Select Rule Group]**, seleccione un grupo cuyos pesos de clasificación desee ajustar.
1. Arrastre los controles deslizantes para cambiar los valores de contribución correspondientes.

   El gráfico circular refleja los cambios gráficamente.
1. Haga clic **[!UICONTROL Save Changes]**.
1. Vuelva a compilar el índice del sitio web escalonado para previsualización de los resultados de la adición de la regla.

   Consulte [Ejecución de un índice completo de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Consulte [Ejecución de un índice incremental de un sitio Web activo o en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
