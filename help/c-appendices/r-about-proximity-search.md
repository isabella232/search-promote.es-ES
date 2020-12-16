---
description: La búsqueda de proximidad permite asociar una ubicación única con cualquier página del sitio web y luego buscar y ordenar los resultados por proximidad (distancia) desde una ubicación determinada.
seo-description: La búsqueda de proximidad permite asociar una ubicación única con cualquier página del sitio web y luego buscar y ordenar los resultados por proximidad (distancia) desde una ubicación determinada.
seo-title: Acerca de la búsqueda de proximidad
solution: Target
title: Acerca de la búsqueda de proximidad
topic: Appendices,Site search and merchandising
uuid: 24fc9265-3400-46a7-b6e0-4de5b049a39a
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---


# Acerca de la búsqueda de proximidad{#about-proximity-search}

La búsqueda de proximidad permite asociar una ubicación única con cualquier página del sitio web y luego buscar y ordenar los resultados por proximidad (distancia) desde una ubicación determinada.

Por ejemplo, supongamos que ha llenado páginas del sitio web con metadatos de código postal de Estados Unidos como los siguientes:

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

El conjunto de resultados contiene todos los documentos ubicados a menos de 100 millas del código postal 84057, ordenados en orden ascendente de distancia desde este código postal.

También puede utilizar códigos de área telefónica para ubicaciones de Estados Unidos. O bien, puede utilizar pares de latitud y longitud para especificar ubicaciones en los metadatos del sitio y en los criterios de búsqueda. El tipo de ubicación se determina automáticamente a partir de los datos proporcionados.

Los valores de ubicación de tres dígitos (&quot;DDD&quot;, donde cada &quot;D&quot; representa un dígito decimal de 0 a 9) se tratan como un código de área telefónica de Estados Unidos.

Los valores de ubicación de cinco o cinco dígitos (&quot;DDDD&quot; o &quot;DDDDD-DDDD&quot;) se tratan como un código postal de Estados Unidos.

Los valores de ubicación en la forma exacta de &quot;±DD.DDDD±DDD.DDDD&quot; se tratan como un par de latitud/longitud. El primer valor numérico firmado especifica la latitud y el segundo valor numérico firmado representa la longitud.

**Importante**: Si especifica un valor de latitud positivo, un valor de longitud positivo o ambos, el carácter &quot;+&quot; de la URL debe codificarse como  `%2b`. De lo contrario, &quot;+&quot; se interpreta como un espacio y el valor no se reconoce como una ubicación válida. Por ejemplo, supongamos que tiene un valor de latitud de +49.2394 y un valor de longitud de -123.1892. La porción de ubicación de la dirección URL, con la codificación &quot;+&quot;, tendría el siguiente aspecto:

```
...&sp_q_location_1=%2b49.2394-123.1892...
```

* Los valores positivos de latitud representan los grados norte del ecuador.
* Los valores negativos de latitud representan grados sur del ecuador.
* Los valores de longitud positiva representan grados al este del Meridiano principal.
* Los valores de longitud negativos representan grados al oeste del Meridiano principal.

Por ejemplo, el valor &quot;+48.8577+002.2950&quot; representa 48.857 grados al norte del ecuador, 2.295 grados al este del Primer Meridiano, la ubicación exacta de la Torre Eiffel en París, Francia. Se requieren los signos numéricos y cada dígito, incluso los ceros al inicio y al final. Por ejemplo, los tres valores &quot;48.8577+2.2950&quot;, &quot;+48.8577+2.2950&quot; y &quot;+48.8577+02.295&quot; no son ubicaciones. Al primer valor le falta el signo de interlineado en la latitud. Al segundo valor le faltan los dos ceros a la izquierda de la longitud. Al tercer valor le falta el cero final en la longitud. Asegúrese de examinar detenidamente el registro de índice para detectar cualquier problema relacionado con la ubicación.

Al buscar por proximidad, se crea un &quot;campo de salida de proximidad&quot; especial para esa búsqueda. El campo se rellena con la distancia relativa entre la ubicación especificada en los criterios de búsqueda y la ubicación asociada con cada resultado de búsqueda. Este campo especial recibe el nombre del campo de tipo ubicación que se utiliza en los criterios de búsqueda con &quot;_proximity&quot; agregado al final.

En la búsqueda de ejemplo anterior, los resultados se ordenan en orden ascendente por &quot;zip_proximity&quot;. Es decir, la distancia entre el código postal especificado (84057) y la ubicación del campo &quot;zip&quot; de cada resultado. También puede utilizar este &quot;campo de salida de proximidad&quot; especial para mostrar la distancia relativa de cada resultado de búsqueda, en kilómetros o millas, utilizando la etiqueta de plantilla de búsqueda `<Search-Display-Field>`.

Consulte [Buscar etiquetas de plantilla](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

También puede buscar sin la opción sp_s. En ese caso, los resultados se ordenan por puntuación (sp_s=0, que es el valor predeterminado). La puntuación depende de la distancia relativa de cada resultado de la ubicación de búsqueda de proximidad especificada mediante el parámetro sp_q_location[_#]. Se agrega un nuevo parámetro cgi sp_q_max_relevant_distance[#] para controlar opcionalmente el cálculo de relevancia aplicado a las búsquedas de proximidad.

A continuación se muestra un ejemplo de búsqueda de relevancia de proximidad:

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_q_2=shirt&sp_x_2=title&sp_q_max_relevant_distance_2=50
```

El conjunto de resultados contiene cualquier documentos ubicado a menos de 100 millas del código postal 84057 y contiene la palabra &quot;camisa&quot; en el campo de título, ordenada por puntuación que influye en la puntuación de proximidad-relevancia. Una puntuación de relevancia perfecta para el componente de proximidad representaría una distancia de 0. Una puntuación de relevancia mínima para el componente de proximidad representaría una distancia de poco más de 50 millas.

Para obtener más información sobre la búsqueda por proximidad, consulte `sp_location`, `sp_location_#`, `sp_q_min`, `sp_q_min_#`, `sp_q_max`, `sp_q_max_#` y `sp_s` en el tema de referencia Buscar parámetros CGI.

Consulte [Buscar parámetros CGI](../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890).

Consulte [Añadir un nuevo campo de etiqueta meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
