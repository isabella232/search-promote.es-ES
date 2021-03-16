---
description: La búsqueda de proximidad permite asociar una ubicación única con cualquier página del sitio web y luego buscar y ordenar los resultados por proximidad (distancia) desde una ubicación determinada.
solution: Target
title: Acerca de la búsqueda por proximidad
topic: Apéndices, búsqueda de sitios y comercialización
uuid: 24fc9265-3400-46a7-b6e0-4de5b049a39a
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 0%

---


# Acerca de la búsqueda por proximidad{#about-proximity-search}

La búsqueda de proximidad permite asociar una ubicación única con cualquier página del sitio web y luego buscar y ordenar los resultados por proximidad (distancia) desde una ubicación determinada.

Por ejemplo, supongamos que ha rellenado páginas de su sitio web con metadatos de código postal de Estados Unidos, como los siguientes:

```
<meta name="zipcode" content="84057">
```

A continuación, configure su cuenta para indexar los metadatos del código postal. En **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** > **[!UICONTROL Add New Field]**, en la página [!DNL Add Field], se configuran las siguientes opciones:

* Nombre del campo: `zip`
* Meta Tag Name(s): `zipcode`
* Tipo de datos: **[!UICONTROL Location]**
* Clasificación: **[!UICONTROL Ascending]**
* Unidades predeterminadas: **[!UICONTROL Miles]**

Después de indexar el sitio, realiza la siguiente búsqueda:

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_s=zip_proximity
```

El conjunto de resultados contiene cualquier documento ubicado a menos de 100 millas del código postal 84057, ordenado en orden ascendente a distancia de este código postal.

También puede utilizar códigos de área telefónica para ubicaciones de Estados Unidos. O bien, puede usar pares de latitud/longitud para especificar ubicaciones en los metadatos del sitio y en los criterios de búsqueda. El tipo de ubicación se determina automáticamente a partir de la forma de los datos proporcionados.

Los valores de ubicación de tres dígitos (&quot;DDD&quot;, donde cada &quot;D&quot; representa un dígito decimal entre 0 y 9) se tratan como un código de área telefónica de los Estados Unidos.

Los valores de ubicación de cinco o cinco dígitos (cuatro dígitos) (&quot;DDDD&quot; o &quot;DDDD-DDD&quot;) se tratan como código postal de Estados Unidos.

Los valores de ubicación en la forma exacta de &quot;±DD.DDDD±DDD.DDD&quot; se tratan como un par de latitud/longitud. El primer valor numérico firmado especifica latitud y el segundo valor numérico firmado representa longitud.

**Importante**: Si especifica un valor de latitud positivo, un valor de longitud positivo o ambos, el carácter &quot;+&quot; de la URL debe codificarse como  `%2b`. De lo contrario, &quot;+&quot; se interpreta como un espacio y el valor no se reconoce como una ubicación válida. Por ejemplo, suponga que tenía un valor de latitud de +49 2394 y un valor de longitud de -123 1892. La parte de ubicación de la dirección URL, con codificación de &quot;+&quot;, tendría el siguiente aspecto:

```
...&sp_q_location_1=%2b49.2394-123.1892...
```

* Los valores de latitud positivos representan grados norte del ecuador.
* Los valores de latitud negativos representan grados Sur del ecuador.
* Los valores de longitud positiva representan los grados este de Prime Meridian.
* Los valores de longitud negativos representan grados al oeste del Primer Meridiano.

Por ejemplo, el valor &quot;+48.8577+002.2950&quot; representa 48.8577 grados norte del ecuador, 2.295 grados este del Primer Meridiano, la ubicación exacta de la Torre Eiffel en París, Francia. Se requieren los signos numéricos y cada dígito, incluso los ceros a la izquierda y a la derecha. Por ejemplo, los tres valores &quot;48.8577+2.2950&quot;, &quot;+48.8577+2.2950&quot; y &quot;+48.8577+02.295&quot; no son ubicaciones. Al primer valor le falta el signo inicial en la latitud. Al segundo valor le faltan los dos ceros a la izquierda de la longitud. Al tercer valor le falta el cero al final de la longitud. Asegúrese de examinar detenidamente su registro de índice para detectar cualquier problema relacionado con la ubicación.

Cuando busca por proximidad, hay un &quot;campo de salida de proximidad&quot; especial creado para esa búsqueda. El campo se rellena con la distancia relativa entre la ubicación especificada en los criterios de búsqueda y la ubicación asociada con cada resultado de búsqueda. Este campo especial recibe el nombre del campo de tipo ubicación que se utiliza en los criterios de búsqueda con &quot;_proximity&quot; añadido al final.

En la búsqueda de ejemplo anterior, los resultados se ordenan en orden ascendente como &quot;zip_proximity&quot;. Es decir, la distancia entre el código postal especificado (84057) y la ubicación del campo &quot;zip&quot; de cada resultado. También puede utilizar este &quot;campo de salida de proximidad&quot; especial para mostrar la distancia relativa para cada resultado de búsqueda, en kilómetros o millas, utilizando la etiqueta de plantilla de búsqueda `<Search-Display-Field>`.

Consulte [Buscar etiquetas de plantilla](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

También puede buscar sin la opción sp_s . En tal caso, los resultados se ordenan por puntuación (sp_s=0, que es el valor predeterminado). La puntuación está influida por la distancia relativa de cada resultado desde la ubicación de búsqueda de proximidad especificada mediante el parámetro sp_q_location[_#]. Se agrega un nuevo parámetro cgi sp_q_max_relevant_distance[#] para controlar opcionalmente el cálculo de relevancia aplicado a las búsquedas por proximidad.

El siguiente es un ejemplo de búsqueda de relevancia de proximidad:

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_q_2=shirt&sp_x_2=title&sp_q_max_relevant_distance_2=50
```

El conjunto de resultados contiene cualquier documento ubicado a menos de 100 millas del código postal 84057 y contiene la palabra &quot;camisa&quot; en el campo de título, ordenado por puntuación que influyó en la puntuación de relevancia de proximidad. Una puntuación de relevancia perfecta para el componente de proximidad representaría una distancia de 0. Una puntuación de relevancia mínima para el componente de proximidad representaría una distancia de poco más de 50 millas.

Para obtener más información sobre la búsqueda por proximidad, consulte `sp_location`, `sp_location_#`, `sp_q_min`, `sp_q_min_#`, `sp_q_max`, `sp_q_max_#` y `sp_s` en el tema de referencia Buscar parámetros CGI.

Consulte [Buscar parámetros CGI](../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890).

Consulte [Adición de un nuevo campo de metaetiqueta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
