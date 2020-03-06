---
description: 'null'
seo-description: 'null'
seo-title: Preguntas más frecuentes
solution: Target
title: Preguntas más frecuentes
topic: Appendices,Site search and merchandising
uuid: 4ce454a4-e770-4587-91a0-a25491818ac6
translation-type: tm+mt
source-git-commit: 4270ea66ba645ad0f71c9c8b5c2a1fcc6eb02ad2

---


# Preguntas más frecuentes{#frequently-asked-questions}

## Adobe Flash {#reference_4A25BBDE32214AF5A1A454F38FD51243}

Página de preguntas más frecuentes que explica la compatibilidad con la indexación y búsqueda de archivos SWF en un sitio web.

Las siguientes son preguntas habituales sobre los archivos SWF:

* [¿Cuándo se rastrea e indexa un archivo SWF?](#section_01BB5259140D4D5FB04CCB7A1A63DE99)
* [Qué tengo que hacer para indexar un SWF...](#section_0A6A52CC70D4495BBE14D91906318F95)
* [¿Cómo se reconocen los archivos SWF?](#section_B36C0536AB544F509601DC6A11A8E656)
* [¿Cómo se indexan los archivos SWF?](#section_36856058A4B54FA5ABF921344F50410C)
* [¿Un archivo SWF cuenta como una página?](#section_0158D6DE70BC40D78E2374787B9F58AB)
* [Cómo evito la indexación de archivos SWF individuales...](#section_E38AD37989EF410B97AF5125057BFD22)
* [Cómo evito que los archivos SWF se indiquen en...](#section_DF2606A50E9A44859CFA0D44D7C5F2E4)
* [¿Cómo es que no puedo buscar archivos SWF chinos, japoneses o coreanos en mi sitio web?](#section_EE1A3A705AE74148BD195A0CE513A5C4)

## ¿Cuándo se rastrea e indexa un archivo SWF? {#section_01BB5259140D4D5FB04CCB7A1A63DE99}

Un archivo SWF se arrastra e indexa si está contenido en una etiqueta embed u object en una página HTML, como en el siguiente ejemplo:

```
<embed src="Flash-file-URL">  
 
<object>  
<param name=movie value="Flash-file-URL">  
</object> 
```

También se reconoce un archivo SWF si se indica la URL del archivo como punto de entrada.

Consulte [Adición de varios puntos de entrada de URL que desea indizar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## ¿Qué tengo que hacer para indexar un archivo SWF? {#section_0A6A52CC70D4495BBE14D91906318F95}

Para rastrear e indexar archivos SWF, seleccione el tipo de contenido **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Siempre que se haga referencia al archivo Flash desde una `<embed>` etiqueta o una `<object>` etiqueta de un documento HTML, el texto se indexará y se rastrearán todas las direcciones URL enumeradas en el archivo.

Si no se hace referencia al archivo desde una `<embed>` etiqueta o una `<object>` etiqueta, puede enumerar el archivo SWF en una `<a href=...>` etiqueta de un documento HTML o como un punto de entrada URL.

Consulte [Adición de varios puntos de entrada de URL que desea indizar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## ¿Cómo se reconocen los archivos SWF? {#section_B36C0536AB544F509601DC6A11A8E656}

Los archivos SWF se identifican con el siguiente tipo MIME:

`application/x-shockwave-flash`

Los archivos SWF también se reconocen con los tipos `application/octet-stream`&quot; o `text/plain` MIME, siempre que la extensión del archivo sea .swf.

Un servidor mal configurado puede utilizar un tipo MIME diferente para archivos SWF. Asegúrese de comprobar la configuración del servidor si tiene problemas para rastrear e indexar archivos SWF.

## ¿Cómo se indexan los archivos SWF? {#section_36856058A4B54FA5ABF921344F50410C}

El texto contenido en un archivo SWF se indiza como si fuera `<body>` texto en la página HTML que lo rodea. Si un resultado de búsqueda encuentra texto contenido en un archivo SWF incrustado, el resultado en realidad se vincula a la página HTML que lo rodea y no al archivo SWF. De este modo, el archivo SWF se muestra en el contexto correcto.

Si un archivo SWF contiene una URL como acción &quot;Cargar película&quot;, el texto del archivo SWF al que se hace referencia se indexará como parte de la página HTML que lo rodea.

Si un archivo SWF contiene una URL como acción &quot;Obtener URL&quot;, la URL se rastrea e indexa más tarde, tal como se rastrea e indiza posteriormente una referencia HTML `<a href=...>` .

Si un archivo SWF aparece como un punto de entrada URL, el texto del archivo SWF se indexará como una sola página. Resultado de búsqueda que encuentra texto desde un SWF de punto de entrada directamente a la película, no a una página HTML que lo rodea.

Consulte [Adición de varios puntos de entrada de URL que desea indizar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## ¿Un archivo SWF cuenta como una página? {#section_0158D6DE70BC40D78E2374787B9F58AB}

No. Un archivo SWF se considera parte de su página HTML adjunta. Todas las direcciones URL &quot;Cargar película&quot; contenidas en archivos SWF también se consideran parte de la página HTML que la rodea. Por lo tanto, los archivos SWF a los que se hace referencia desde una página HTML no se cuentan como una &quot;página&quot; para el total de páginas de la cuenta.

Si un archivo SWF aparece como un punto de entrada URL, ese archivo SWF y todas las URL de &quot;Cargar película&quot; enumeradas en ese archivo SWF se cuentan como una &quot;página&quot; para el total de páginas de la cuenta.

## ¿Cómo puedo evitar la indexación de archivos SWF individuales? {#section_E38AD37989EF410B97AF5125057BFD22}

Para evitar la indexación de un archivo SWF, puede agregar una etiqueta meta ( `<meta name="ROBOTS" content="NOINDEX">`) de robots o una `<noindex>` etiqueta al documento HTML que lo rodea. Es decir, el documento que contiene la `<embed>` etiqueta o `<object>` .

También puede utilizar la etiqueta meta robots ( `<meta name="ROBOTS" content="NOFOLLOW">`) para evitar las siguientes direcciones URL contenidas en el archivo SWF. Si el documento HTML que lo rodea tiene lo siguiente desactivado, no se siguen las URL enumeradas como acciones &quot;Get URL&quot; en el archivo SWF.

## ¿Cómo puedo evitar que los archivos SWF se indiquen en mi sitio web? {#section_DF2606A50E9A44859CFA0D44D7C5F2E4}

Para desactivar la indexación SWF, anule la selección del tipo de contenido **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

También puede optar por utilizar [!DNL URL Masks] para desactivar la indexación de archivos SWF.

Consulte [Adición de máscaras URL para indexar o no partes de índice de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Para desactivar la indexación SWF, introduzca una de las siguientes máscaras URL:

* `exclude *.swf` (si no utiliza expresiones regulares)
* `exclude regexp ^.*\.swf$` (si utiliza expresiones regulares)

Consulte Expresiones [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## ¿Cómo es que no puedo buscar archivos SWF chinos, japoneses o coreanos en mi sitio web? {#section_EE1A3A705AE74148BD195A0CE513A5C4}

La búsqueda/comercialización del sitio obtiene UTF-8 de archivos SWF creados con Adobe Flash. El UTF-8 no contiene indicación de idioma. Si ha seleccionado el tipo de contenido **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), debe utilizar inyecciones de metadatos para especificar el idioma que utiliza el archivo SWF.

Consulte [Adición de definiciones](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de inyección de campo.

Los archivos SWF anteriores tampoco especifican un conjunto de caracteres. Si ha seleccionado el tipo de contenido SWF **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), debe utilizar las inyecciones de metadatos para especificar el conjunto de caracteres que se utiliza en el archivo SWF.

## Búsqueda general {#reference_E2C675162789452A9B99C6633B12CBEF}

Una página de preguntas más frecuentes que explica cómo la búsqueda o comercialización del sitio ayuda a los clientes que visitan el sitio Web a encontrar lo que buscan.

Las siguientes son preguntas comunes con respecto a la búsqueda general:

* [Tengo que instalar cualquier software para usar el sitio...](#section_02AB2AFF71984F9DAA3AF2B7C0847A22)
* [¿Qué sucede cuando mi sitio supera el límite de páginas?](#section_ECA5FA01032D4322BABA4E2C7FE498C1)
* [¿Cómo cambio la dirección de correo electrónico donde la semana...](#section_AE27F63DD13F425B940C8E7D9ED5C614)
* [¿Cuán segura es la información de mis clientes en la búsqueda y comercialización del sitio?](#section_5484CB954167412BB7F0480CB0C504B8)
* [¿Qué sucede con la privacidad de la información de mis clientes?](#section_8FB493F15E51454BA92A0C83E14C0CC7)
* [¿Puedo mostrar mis propias publicidades de titular en la búsqueda?...](#section_611EB8B32C16418386CB7DC7FB6954B8)

Las siguientes son preguntas comunes con respecto a las funciones de búsqueda:

* [¿Puedo personalizar los resultados de búsqueda de mi sitio?](#section_A64B3A621B794DF78D35ED06D9C43D0B)
* [¿Puedo ver qué buscan los clientes en mi...](#section_73709E1B0E82478DA7B4D15B6C845F33)
* [¿Cómo puedo controlar qué tipos de contenido (PDF, texto, Flash, MP3 y Microsoft Office) se indexan y buscan?](#section_0AB8CB4B6BFA4286AA082055FEBFBE1C)
* [¿Se admiten las páginas web generadas dinámicamente mediante contenido basado en ASP, JSP, PHP, CFM o Perl?](#section_E279F004F1C542A2B9773B832E7B013F)
* [¿Cómo puedo usar sinónimos para mejorar los resultados de la búsqueda?...](#section_E6E36E12514F4D7BAB01F8D1AB61D57B)
* [¿Tengo control sobre el orden de los resultados de búsqueda...](#section_C6361048502745779D9749A842C4C370)
* [¿Puedo cambiar el idioma de la página de resultados de búsqueda?...](#section_6EE41DA8241247D48BBEB061A50599C5)
* [¿Puedo tener más de un sitio en mi Adobe?...](#section_AFA8825182094660A71EEC84B8329D6D)
* [¿Puedo buscar más de un dominio?](#section_BFBB0E9861D942F095B56CF0A8F16596)
* [¿Puedo subdividir mi sitio en secciones separadas para que...](#section_52153A9DE9F9493B967A70583848B2A4)
* [Cómo excluyo partes de mi sitio web de ser...](#section_D452EDE153654EF398F4A87780C6D43B)
* [¿Qué conjuntos de caracteres se admiten?](#section_A62A6F8F15804F968C77F2DEBDE8F8FD)
* [¿Qué sucede si cambio o actualizo mi sitio web?](#section_489050E0EBC14D0594DBBAA0CCF4F6BA)
* [¿Se puede indexar automáticamente mi sitio?](#section_9C7D41636238488691ECDFEE4D4E5103)
* [Utilizo contraseñas en mi sitio web. ¿Puedo seguir utilizando la búsqueda o comercialización del sitio?](#section_4618EB5B66704640B5502D1B5CB4B32E)
* [¿Admite el rastreo y la indexación de https o...](#section_D5BB8B8FBEA4405583E86B4AEC37151B)
* [¿La búsqueda/comercialización del sitio honra el archivo robots.txt en mi sitio web?](#section_73BBF6FE93C64C109F45CBC2FA394DB2)
* [Ciertas partes de mi sitio web deben actualizarse con frecuencia para que...](#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3)
* [¿Puedo usar scripts o programas para iniciar un aumento?...](#section_0B6BB039557A42AA876D35D748E17DD0)

## ¿Tengo que instalar algún software para utilizar la búsqueda o comercialización del sitio? {#section_02AB2AFF71984F9DAA3AF2B7C0847A22}

No. Ésta es la ventaja principal de la búsqueda y comercialización del sitio. El motor es una aplicación profesional alojada y mantenida completamente en nuestros servidores de alto rendimiento. Esto hace que el software sea más fácil de usar que otras soluciones de búsqueda. Lo único que tiene que hacer es agregar una pequeña cantidad de código HTML a las páginas para que los clientes del sitio web puedan ingresar búsquedas. La búsqueda y comercialización del sitio se ocupa de todo el resto.

## ¿Qué sucede cuando mi sitio supera el límite de páginas? {#section_ECA5FA01032D4322BABA4E2C7FE498C1}

Seguimos realizando búsquedas para que los visitantes puedan buscar su sitio web sin interrupciones. Para ver si el sitio web supera el límite de páginas, revise el estado del índice completo o el registro activo.

Consulte [Acerca del índice](../c-about-index-menu/c-about-full-index.md#concept_C69BD21863FD4856B49326F35DB570D3)completo.

Consulte [Visualización del registro de índice completo de un activo o un ensayo...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

## ¿Cómo cambio la dirección de correo electrónico donde se envían los informes semanales? {#section_AE27F63DD13F425B940C8E7D9ED5C614}

Los informes semanales se envían al propietario de cada cuenta activa. Puede cambiar la dirección de correo electrónico haciendo clic en **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]**. Si tiene más de una cuenta de búsqueda activa, todas las newsletters se envían a la nueva dirección.

Consulte [Configuración de la información](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)personal del usuario.

## ¿Cuán segura es la información de mis clientes en la búsqueda y comercialización del sitio? {#section_5484CB954167412BB7F0480CB0C504B8}

La búsqueda y comercialización del sitio es segura, rápida, estable y fácil de usar. No está obligado a utilizar cookies (aunque puede hacerlo si lo desea) para utilizar nuestros productos, y la información confidencial, como las contraseñas, nunca se coloca en ningún vínculo URL que pueda recuperarse posteriormente de su explorador.

## ¿Qué sucede con la privacidad de la información de mis clientes? {#section_8FB493F15E51454BA92A0C83E14C0CC7}

Adobe se ha comprometido a respetar la privacidad de sus clientes y visitantes. Consulte el Centro de [privacidad](https://www.adobe.com/privacy.html)de Adobe.

## ¿Puedo mostrar mis propias publicidades de titular en las páginas de resultados de búsqueda? {#section_611EB8B32C16418386CB7DC7FB6954B8}

Sí. Usted controla la apariencia y el contenido de los resultados de búsqueda. Dentro de la plantilla de resultados de búsqueda del sitio web, puede crear vínculos a su propia red de intercambio de pancartas, como LinkExchange o SmartClicks. Las visitas realizadas por los visitantes se acreditan correctamente a su cuenta de intercambio de pancartas.

## ¿Puedo personalizar los resultados de búsqueda de mi sitio? {#section_A64B3A621B794DF78D35ED06D9C43D0B}

Sí. Esta es una característica exclusiva de la búsqueda y comercialización del sitio. Con nuestra avanzada tecnología de plantillas y un poco de conocimientos de HTML, puede controlar exactamente cómo aparecen los resultados de búsqueda.

Consulte [Buscar etiquetas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de plantilla.

La transición entre sus propios servidores y los servidores de mercadotecnia y búsqueda del sitio es completamente transparente e invisible para sus clientes. Si no conoce HTML o no tiene tiempo para crear una plantilla personalizada, puede elegir entre una variedad de plantillas atractivas y listas para usar que crea el equipo interno de desarrolladores web profesionales de Adobe.

## ¿Puedo ver qué buscan los clientes en el sitio? {#section_73709E1B0E82478DA7B4D15B6C845F33}

Sí. Mantenemos las estadísticas de búsqueda de las búsquedas realizadas por los visitantes en su sitio web durante los últimos dos meses. Puede revisar estas estadísticas en cualquier momento en Informes en el menú del producto. Los informes de búsqueda proporcionan información vital sobre qué buscan exactamente los visitantes en el sitio web. Puede utilizar esta información para mejorar el diseño o para ajustar el motor de búsqueda y comercialización del sitio a fin de servir mejor a los visitantes.

## ¿Cómo puedo controlar qué tipos de contenido (PDF, texto, Flash, MP3 y Microsoft Office) se indexan y buscan? {#section_0AB8CB4B6BFA4286AA082055FEBFBE1C}

Puede configurar fácilmente las cuentas para habilitar o deshabilitar la indexación y búsqueda de texto que se encuentra en documentos PDF, documentos de texto sin formato, películas Flash, archivos MP3 o documentos de Microsoft Office.

Esta configuración se controla en la [!DNL Staged Content Types] página.

Consulte [Acerca de los tipos](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)de contenido.

## ¿Se admiten las páginas web generadas dinámicamente mediante contenido basado en ASP, JSP, PHP, CFM o Perl? {#section_E279F004F1C542A2B9773B832E7B013F}

Las páginas web HTML estáticas o generadas dinámicamente se indexan, incluso las páginas creadas a partir de bases de datos, o cualquier otro proceso back-end. Dado que el código HTML que ve un navegador está indexado, puede utilizar la búsqueda/comercialización del sitio en sitios web siempre y cuando estas arquitecturas de back-end resulten en páginas HTML.

El robot de búsqueda rastrea el sitio Web comenzando con la primera página en la dirección del sitio Web especificada en [!DNL Account Settings], y sigue los vínculos de página en página.

Consulte [Configuración de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Cuando el robot de búsqueda rastrea e indexa todas las páginas del sitio Web, puede utilizar el motor de búsqueda para buscar en el sitio. En otras palabras, si los documentos generados dinámicamente se tejen en el sitio web con vínculos de otras páginas, el robot de búsqueda podrá rastrear e indexar el contenido dinámico.

Después de rastrear e indexar el contenido del sitio web, los clientes del sitio web pueden buscar información dentro del contenido indexado.

## ¿Cómo puedo utilizar sinónimos para mejorar los resultados de búsqueda de mi sitio? {#section_E6E36E12514F4D7BAB01F8D1AB61D57B}

Puede utilizar sinónimos cuando desee que los visitantes encuentren páginas relacionadas con su consulta de búsqueda.

Por ejemplo: supongamos que tiene una página que contiene una lista de precios de los productos en venta en el sitio. Sin embargo, después de examinar los informes de búsqueda proporcionados por la búsqueda o comercialización del sitio, se observa que los clientes buscan la palabra &quot;costo&quot;, &quot;gasto&quot;, &quot;cargo&quot; o &quot;pago&quot; en sus búsquedas. Estas palabras no muestran la página de lista de precios en los resultados de búsqueda. Con la [!DNL Add Synonyms] característica en [!DNL Dictionaries], puede especificar que estas palabras son sinónimos y que el cliente puede encontrar la lista de precios, independientemente del término de búsqueda que utilice.

Consulte [Acerca de los diccionarios](../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034).

## ¿Tengo control sobre el orden de los resultados de búsqueda? {#section_C6361048502745779D9749A842C4C370}

Sí. Mediante la interfaz de relevancia avanzada, puede controlar qué páginas se devuelven para una consulta de búsqueda específica. Esta función es útil si desea asegurarse de que los clientes ven una página específica cuando buscan determinadas palabras.

Consulte [Adición de un nuevo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de etiqueta meta.

## ¿Puedo cambiar el idioma de la página de resultados de búsqueda? {#section_6EE41DA8241247D48BBEB061A50599C5}

Sí. La plantilla de búsqueda y comercialización del sitio es flexible cuando se trata de permitirle construir una página de resultados que utilice el idioma que elija y que coincida con el aspecto del sitio web.

La plantilla consiste en una combinación de texto, etiquetas HTML estándar y etiquetas especiales que se definen para mostrar los resultados de la búsqueda. Cuando un cliente realiza una búsqueda, el robot de búsqueda lee la plantilla, envía el texto con etiquetas HTML estándar e inserta los vínculos de resultados basados en las etiquetas de plantilla especiales.

Consulte [Buscar etiquetas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de plantilla.

Si desea cambiar el idioma de los resultados, puede editar el texto en inglés que aparece en la plantilla.

Consulte [Edición de una presentación o una plantilla](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transporte.

## ¿Puedo tener más de un sitio en mi inicio de sesión de cliente de Adobe? {#section_AFA8825182094660A71EEC84B8329D6D}

Sí. Con un único inicio de sesión de cliente de Adobe, puede administrar un motor de búsqueda diferente para muchos sitios web diferentes. Seleccione y administre cuentas en &quot;Cuentas&quot;.

Consulte [Selección de una cuenta diferente para usar](../c-about-accounts-menu.md#task_03C0FE918E2D44529CDC3B8DB75D1B26).

## ¿Puedo buscar más de un dominio? {#section_BFBB0E9861D942F095B56CF0A8F16596}

Sí. Puede configurar el acceso a más de un dominio mediante [!DNL URL Entrypoints]. Proporcione puntos de entrada de URL para dominios adicionales que le pertenecen. Recuerde que debe tener permiso para indexar dominios que no sean de su propiedad.

Consulte [Acerca de los puntos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

## ¿Puedo subdividir mi sitio en secciones separadas para que los clientes puedan buscar cualquiera de estas áreas individualmente o en todo el sitio? {#section_52153A9DE9F9493B967A70583848B2A4}

Sí. Se incluye una función &quot;Colecciones&quot; que permite a los clientes buscar áreas específicas del sitio web para encontrar rápidamente lo que buscan.

Consulte [Acerca de las colecciones](../c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127).

Por ejemplo: los clientes pueden buscar una colección de direcciones URL relacionadas con la información de ventas de productos o una colección de direcciones URL relacionadas con los servicios de asistencia. Puede configurar colecciones para que sus clientes vean una lista desplegable de colecciones o un grupo de casillas de verificación.

## ¿Cómo excluyo partes de mi sitio web de la búsqueda? {#section_D452EDE153654EF398F4A87780C6D43B}

Sí. Especifique las máscaras URL para determinar qué páginas del sitio Web desea incluir o excluir de la indexación. Las máscaras URL determinan si las páginas del sitio Web aparecen en los resultados de búsqueda.

Consulte [Acerca de las máscaras](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

Consulte [Acerca del script](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)de máscaras URL.

Para evitar que se busquen partes de páginas web individuales, puede excluir partes de una página de la indexación. Rodee el texto con `<noindex>` etiquetas y `</noindex>` . Este método resulta útil si desea excluir el texto de navegación de las búsquedas.

## ¿Qué conjuntos de caracteres se admiten? {#section_A62A6F8F15804F968C77F2DEBDE8F8FD}

Las páginas Web suelen especificar el conjunto de caracteres con una etiqueta meta similar a la siguiente:

`<META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=iso-8859-1">`

El motor de búsqueda/comercialización del sitio indexa correctamente las páginas Web utilizando todos los conjuntos de caracteres comunes que se utilizan en Internet en la actualidad. Algunos de los conjuntos de caracteres admitidos son los siguientes:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Árabe (ISO-8859-6) </p> </td> 
   <td colname="col2"> <p>Chino (tradicional); Big5) </p> </td> 
   <td colname="col3"> <p>Japonés (Shift_JIS) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Árabe (Windows-1256) </p> </td> 
   <td colname="col2"> <p>Chino (tradicional); EUC-TW) </p> </td> 
   <td colname="col3"> <p>Ruso (KOI8-R) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Báltico (ISO-8859-4) </p> </td> 
   <td colname="col2"> <p>Cirílico (ISO-8859-5) </p> </td> 
   <td colname="col3"> <p>Europa meridional (ISO-8859-3) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Báltico (Windows-1257) </p> </td> 
   <td colname="col2"> <p>Cirílico (Windows-1251) </p> </td> 
   <td colname="col3"> <p>Turco (ISO-8859-9) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Centroeuropeo (ISO-8859-2) </p> </td> 
   <td colname="col2"> <p>Griego (ISO-8859-7) </p> </td> 
   <td colname="col3"> <p>Turco (Windows-1254) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Centroeuropeo (Windows-1250) </p> </td> 
   <td colname="col2"> <p>Griego (Windows-1253) </p> </td> 
   <td colname="col3"> <p>Unicode (UTF-8) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chino (ISO-2022-CN) </p> </td> 
   <td colname="col2"> <p>Hebreo (ISO-8859-8) </p> </td> 
   <td colname="col3"> <p>US-ASCII (us-ascii) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chino (ISO-2022-CN-EXT) </p> </td> 
   <td colname="col2"> <p>Hebreo (Windows-1255) </p> </td> 
   <td colname="col3"> <p>Europeo occidental (ISO-8859-1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chino (simplificado; EUC-CN) </p> </td> 
   <td colname="col2"> <p>Japonés (EUC-JP) </p> </td> 
   <td colname="col3"> <p>Europeo occidental (ISO-8859-15) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chino (simplificado; GB2312) </p> </td> 
   <td colname="col2"> <p>Japonés (ISO-2022-JP) </p> </td> 
   <td colname="col3"> <p>Europeo Occidental (Windows-1252) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chino (simplificado; GBK) </p> </td> 
   <td colname="col2"> <p>Japonés (ISO-2022-JP-1) </p> </td> 
   <td colname="col3"> <p>Europeo occidental (x-mac-roman) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chino (simplificado; HZ-GB-2312) </p> </td> 
   <td colname="col2"> <p>Japonés (ISO-2022-JP-2) </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Póngase en contacto con el servicio de asistencia técnica para preguntar sobre los conjuntos de caracteres que no aparecen en la lista anterior.

## ¿Qué sucede si cambio o actualizo mi sitio web? {#section_489050E0EBC14D0594DBBAA0CCF4F6BA}

Después de cambiar el contenido del sitio web, puede realizar un índice completo o un índice incremental. La búsqueda/comercialización del sitio descarga e indexa cualquier contenido modificado del sitio web. Una vez finalizada la indexación, los clientes pueden buscar el nuevo contenido. También puede programar una indexación automática del sitio en un momento determinado y en un día específico.

Consulte [Ejecución de un índice completo de un sitio web activo o en un sitio web escalonado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Consulte [Ejecución de un índice incremental de un sitio Web activo o en un sitio Web en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Consulte [Configuración de la programación de índice completa para un sitio web](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)activo.

Consulte [Configuración de la programación incremental de índices para un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)activo.

## ¿Se puede indexar automáticamente mi sitio? {#section_9C7D41636238488691ECDFEE4D4E5103}

Sí. Puede programar un índice automático del sitio cada día.

Además de la indexación automática diaria, puede elegir que las partes del sitio que cambian con frecuencia se indiquen de forma incremental. En los días en que tenga un índice automático programado, puede controlar la hora del día en que se produce el índice. Además, siempre puede iniciar manualmente un índice del sitio cuando lo desee.

Consulte [Configuración de la programación de índice completa para un sitio web](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0)activo.

Consulte [Configuración de la programación incremental de índices para un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)activo.

## Utilizo contraseñas en mi sitio web. ¿Puedo seguir utilizando la búsqueda o comercialización del sitio? {#section_4618EB5B66704640B5502D1B5CB4B32E}

Si utiliza la autenticación básica HTTP para proteger ciertas partes del sitio Web con contraseña, puede especificar los dominios y las contraseñas que la búsqueda o comercialización del sitio puede utilizar para indexar el sitio.

Consulte [Adición de contraseñas para acceder a las áreas del sitio web que lo requieran...](../c-about-settings-menu/c-about-crawling-menu.md#task_DED19D476FF04B48BB6456D5ECB8628A).

## ¿Admite el rastreo y la indexación de https o contenido seguro del servidor? {#section_D5BB8B8FBEA4405583E86B4AEC37151B}

Sí. Puede rastrear e indexar contenido en servidores seguros (https).

## ¿La búsqueda/comercialización del sitio honra el archivo robots.txt en mi sitio web? {#section_73BBF6FE93C64C109F45CBC2FA394DB2}

Sí. El Protocolo de exclusión de robots es compatible. El robot de búsqueda examina el archivo robots.txt si está presente en su sitio web. Si el archivo robots.txt excluye a todos los robots del rastreo del sitio, también se excluye el robot de búsqueda/comercialización del sitio. Para permitir que sólo el robot de búsqueda/comercialización del sitio rastree su sitio, configure el contenido del archivo robots.txt de la siguiente manera:

```
User-agent: Atomz/1.0 
Disallow:
```

```
User-agent: * 
Disallow: /
```

Puede obtener más información sobre los robots web y el Protocolo de exclusión de robots en:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

## Algunas partes de mi sitio web deben actualizarse con frecuencia para que mis clientes obtengan los resultados de búsqueda más precisos. ¿Ayuda la indexación incremental con este problema? {#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3}

Sí. Este escenario es lo que generó la característica de indexación incremental para facilitar la búsqueda y comercialización del sitio. El beneficio principal de la indexación incremental es que permite a las empresas indexar con frecuencia partes cambiantes dinámicamente de su sitio web. Esta funcionalidad garantiza que se muestren los resultados de la búsqueda con una precisión de &quot;hasta el minuto&quot;.

Consulte [Ejecución de un índice incremental de un sitio Web activo o en un sitio Web en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Consulte [Configuración de la programación incremental de índices para un sitio Web](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)activo.

## ¿Las páginas Web generadas dinámicamente son compatibles con una base de datos back-end, como catálogos de productos o sistemas de administración de inventario? {#section_26896C556483457E879785E751583B16}

Se indexan las páginas web HTML estáticas o generadas dinámicamente, incluidas las páginas creadas a partir de bases de datos, o cualquier otro proceso back-end. Dado que el código HTML, tal como lo ve un navegador, está indexado, puede utilizar la búsqueda/comercialización del sitio en sitios web siempre y cuando la información de la base de datos back-end resulte en páginas HTML.

El robot de búsqueda rastrea el sitio Web comenzando con la primera página en la dirección del sitio Web especificada en [!DNL Account Settings], y sigue los vínculos de página en página.

Consulte [Configuración de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Cuando el robot de búsqueda rastrea e indexa todas las páginas del sitio Web, puede utilizar el motor de búsqueda para buscar en el sitio. En otras palabras, si los documentos generados dinámicamente se tejen en el sitio web con vínculos de otras páginas, el robot de búsqueda podrá rastrear e indexar el contenido de la base de datos dinámica.

Después de rastrear e indexar el contenido del sitio web, los clientes del sitio web pueden buscar información dentro del contenido indexado.

Puede habilitar fácilmente la búsqueda de contenido completo o una búsqueda basada en temas más restringida restringida a la información del título, la metadescripción, las etiquetas de documento de metapalabras clave o las tres. Con las definiciones de metadatos, también puede crear campos de visualización personalizados, como una imagen de producto, en los resultados de búsqueda reales.

Consulte [Adición de un nuevo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de etiqueta meta.

## ¿Puedo utilizar secuencias de comandos o programas para iniciar un índice incremental de mi sitio? {#section_0B6BB039557A42AA876D35D748E17DD0}

Sí. Puede utilizar secuencias de comandos o programas para iniciar un índice incremental del sitio web, así como para hacer ping en los servidores para indexar el sitio cada vez que se cambie o actualice el contenido.

Consulte [Acerca del índice](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D)con secuencias de comandos.

## Implementaciones de funciones {#reference_2D0C4A80B8D64051BA9694D562DCE663}

Una página de preguntas más frecuentes que describe varias implementaciones de funciones en [!DNL Search&Promote].

Las siguientes son preguntas habituales sobre la implementación de funciones en [!DNL Search&Promote] un sitio web:

* [¿Por qué no se ejecutan mis reglas comerciales?](#section_7FEB60383D8A4B11A60DFF9067274699)
* [¿Por qué tengo problemas al programar la indexación, errores al iniciar la indexación y problemas al iniciar la indexación por etapas?](#section_E05758193DF5436784B0145839989F75)
* [Mi límite de tamaño de índice supera mi límite permitido. ¿Por qué sucede esto y cómo lo arreglo?](#section_12E7DA979C4C4B1D8A3A6415FC3DDA70)

## ¿Por qué no se ejecutan mis reglas comerciales? {#section_7FEB60383D8A4B11A60DFF9067274699}

Configure las reglas comerciales cuando aparezcan los letreros o para decidir qué resultados aparecerán y en qué orden. También puede configurar la posición de un elemento en la faceta y qué plantilla se utiliza para una búsqueda determinada.
Reordene las reglas comerciales para cambiar el orden en que se ejecutan en las plantillas de presentación. Las reglas comerciales se ejecutan en el orden en que se definieron; es decir, cuanto mayor sea el número de orden de una regla, más tarde se ejecutará en el proceso, superando las reglas anteriores. Las reglas se reordenan introduciendo un nuevo número en la columna Orden de la tabla de la página Reglas comerciales.

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## ¿Por qué tengo problemas al programar la indexación, errores al iniciar la indexación y problemas al iniciar la indexación por etapas? {#section_E05758193DF5436784B0145839989F75}

Cuando se genera un índice, ya sea completo o incremental, la información de estado del rastreo de índice se muestra en tiempo real. Por ejemplo, puede ver la hora de inicio, el tiempo transcurrido y cualquier error que se haya producido durante el proceso de indexación. También se muestra información sobre el estado del último índice. Utilice esta información para solucionar cualquier error de indexación que encuentre.

Para programar un índice, consulte [Configuración de la programación de índice completa para un sitio web](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0) activo y [Configuración de la programación de índice incremental para un sitio web](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33)activo.

Para iniciar un índice escalonado, consulte [Ejecución de un índice completo de un sitio Web activo o escalonado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D) o [Ejecutando un índice incremental de un sitio web activo o en un sitio web en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Mi límite de tamaño de índice supera mi límite permitido. ¿Por qué sucede esto y cómo lo arreglo? {#section_12E7DA979C4C4B1D8A3A6415FC3DDA70}

Un sitio Web puede crecer y con el tiempo Search&amp;Promote &quot;descubre&quot; más documentos y páginas Web que se agregaron. Finalmente, su cuenta puede superar el límite de tamaño de indexación. En estos casos, puede considerar el uso de **[!UICONTROL URL Mask]**. Esta función oculta documentos y páginas web del rastreo de índices que no desea o que no necesita indexar, reduciendo así el tamaño del índice. Otra opción puede ser ponerse en contacto con el servicio de asistencia técnica para que el límite de tamaño de indexación sea mayor en la cuenta.

Consulte [Acerca de las máscaras](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

Si no está seguro de qué hacer, póngase en contacto con el servicio de asistencia técnica. Es posible que haya muchas otras variables que afecten al tamaño del índice y que, si se ajustan, también afecten a la facturación de la cuenta.

## Internacional {#reference_F017C2968BFB446499EF1D3CE2CAC0FE}

Una página de preguntas más frecuentes que analiza la compatibilidad con la indexación y búsqueda de más de 19 idiomas, incluidos idiomas asiáticos de byte múltiple como chino (simplificado y tradicional), japonés y coreano.

Las siguientes son preguntas comunes sobre idiomas y conjuntos de caracteres:

* [Qué controla la codificación del conjunto de caracteres de la consulta de búsqueda...](#section_DF2E8570AFC2480FA199FD26C941A22F)
* [Son solo las páginas cuya codificación coincide con la codificación de...](#section_9E544F3DB7DE41618DC1BC8224B32C5A)
* [¿Qué codificación se utiliza para la página de resultados de búsqueda?](#section_DA68670F35D54EAABF7DBB010F4409BF)
* [¿Puedo utilizar la búsqueda/comercialización del sitio en páginas codificadas Unicode, UTF-8?](#section_130997CB08934A13A5261D85CF88040C)
* [¿Cómo es que no puedo buscar archivos PDF chinos, japoneses o coreanos en mi sitio web?](#section_539AFF482F814D28B5929F683D2F2175)
* [¿Cómo es que no puedo buscar archivos SWF chinos, japoneses o coreanos en mi sitio web?](#section_9C0849528AFF4C10AA97A2C912992638)
* [¿Cómo es que no puedo buscar los archivos de Microsoft Office en chino, japonés o coreano en mi sitio web?](#section_6764BA6863AF492EBA9BE5CCC12CDD1F)
* [¿Cómo es que no puedo buscar archivos MP3 chinos, japoneses o coreanos en mi sitio web?](#section_DB6D60CF46F94125BF4E54AF3036DBFC)
* [¿Necesito hacer algo especial para conseguir...](#section_A8BA6DDD3A6048319D3530BCFD6DA1A5)
* [¿Cómo es que las fuentes chinas, japonesas o coreanas aparecen en los resultados de búsqueda de Netscape 4.7 y versiones anteriores?](#section_DF42567063304F918D406AC76529DFB7)

## ¿Qué controla la codificación del conjunto de caracteres de la consulta de búsqueda? {#section_DF2E8570AFC2480FA199FD26C941A22F}

La sección &quot;Formularios Web&quot; de la cuenta de búsqueda contiene formularios de búsqueda de ejemplo que se utilizan para agregar funcionalidad de búsqueda al sitio Web. Si consulta este código de formularios de búsqueda, encontrará una línea similar a la siguiente:

`<input type=hidden name="sp_f" value="iso-8859-1">`

Esta línea de código le dice al motor de búsqueda que la consulta entrante está codificada en iso-8859-1, una codificación común para los idiomas europeos occidentales. Para cambiar esta configuración, vaya al menú de productos y haga clic en **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]**. En la [!DNL Personal Information] página, en la **[!UICONTROL Character Encoding]** lista desplegable, seleccione una nueva codificación.

Consulte [Configuración de la información](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)personal del usuario.

También puede cambiar manualmente el valor de codificación de las páginas Web editando la línea del `sp_f` formulario de búsqueda. Recuerde que el `sp_f` valor del formulario de búsqueda debe coincidir con la codificación del conjunto de caracteres de la página en la que aparece.

## ¿Solo se buscan las páginas cuya codificación coincide con la codificación de la consulta de búsqueda? {#section_9E544F3DB7DE41618DC1BC8224B32C5A}

De forma predeterminada, no. Siempre y cuando las páginas del sitio Web identifiquen correctamente su codificación de conjunto de caracteres, se realizan las conversiones necesarias entre la codificación de la consulta de búsqueda y la de las páginas, incluso cuando las páginas utilizan varias codificaciones.

## ¿Qué codificación se utiliza para la página de resultados de búsqueda? {#section_DA68670F35D54EAABF7DBB010F4409BF}

La codificación del conjunto de caracteres de la cuenta determina la codificación predeterminada para la plantilla de resultados.

Consulte [Configuración de la información](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6)personal del usuario.

Puede obtener más información sobre la especificación de un conjunto de caracteres en una plantilla HTML.

Consulte [Buscar etiquetas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de plantilla.

## ¿Puedo utilizar la búsqueda/comercialización del sitio en páginas codificadas Unicode, UTF-8? {#section_130997CB08934A13A5261D85CF88040C}

Sí. Sin embargo, los conjuntos de caracteres Unicode, como UTF-8, no proporcionan suficiente información para determinar el idioma en que se escriben las páginas. Para buscar correctamente estas páginas, es necesario especificar el idioma. Para determinar el idioma del documento, la información se procesa en el siguiente orden:

* Encabezado HTTP en lenguaje de contenido enviado para el documento por su servidor.
* Elementos META (por ejemplo, `META HTTP-EQUIV="Content-Language" Content="ja_JP"`) en la `<HEAD>` sección del documento.

* Atributo LANG de la `<HTML>` etiqueta (por ejemplo, `<HTML LANG="ja_JP">`).

Si el servidor no está configurado para entregar el encabezado HTTP Content-Language y los documentos no contienen el elemento META de idioma ni el atributo de idioma de la `<HTML>` etiqueta, puede utilizar inyecciones de metadatos para especificar el idioma adecuado.

Consulte [Adición de definiciones](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de inyección de campo.

## ¿Cómo es que no puedo buscar archivos PDF chinos, japoneses o coreanos en mi sitio web? {#section_539AFF482F814D28B5929F683D2F2175}

La búsqueda/comercialización del sitio obtiene UTF-8 de los archivos PDF de Adobe sin indicación de idioma. Si ha seleccionado **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), debe utilizar inyecciones de metadatos para especificar el idioma que se utiliza en el archivo PDF.

Consulte [Adición de definiciones](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de inyección de campo.

## ¿Cómo es que no puedo buscar archivos SWF chinos, japoneses o coreanos en mi sitio web? {#section_9C0849528AFF4C10AA97A2C912992638}

La búsqueda/comercialización del sitio obtiene UTF-8 de los archivos de película de Adobe Flash que se crearon con Adobe Flash sin indicación de idioma. Si ha seleccionado el tipo de contenido **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), debe utilizar inyecciones de metadatos para especificar el idioma que se utiliza en el archivo SWF.

Para Flash versión 4 o versiones anteriores de archivos SWF, no se especifica el conjunto de caracteres de los caracteres del archivo. Si ha seleccionado el tipo de contenido **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), debe utilizar inyecciones de metadatos para especificar el conjunto de caracteres que se utiliza en el archivo SWF.

Consulte [Adición de definiciones](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de inyección de campo.

## ¿Cómo es que no puedo buscar los archivos de Microsoft Office en chino, japonés o coreano en mi sitio web? {#section_6764BA6863AF492EBA9BE5CCC12CDD1F}

La búsqueda y comercialización de sitios obtiene UTF-8 de archivos de Microsoft Office (Microsoft Word, Microsoft Excel y Microsoft PowerPoint) sin indicación de idioma. Si ha seleccionado el tipo de contenido **[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), debe utilizar inyecciones de metadatos para especificar el idioma utilizado en los archivos de Microsoft Office.

Consulte [Adición de definiciones](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de inyección de campo.

## ¿Cómo es que no puedo buscar archivos MP3 chinos, japoneses o coreanos en mi sitio web? {#section_DB6D60CF46F94125BF4E54AF3036DBFC}

Si selecciona el tipo de contenido **[!UICONTROL Text in MP3 Music Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), debe utilizar inyecciones de metadatos para especificar el conjunto de caracteres que se utiliza para codificar los archivos MP3.

Consulte [Adición de definiciones](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de inyección de campo.

## ¿Necesito hacer algo especial para obtener los archivos .txt en mi sitio web para indexar correctamente? {#section_A8BA6DDD3A6048319D3530BCFD6DA1A5}

Si ha seleccionado el tipo de contenido **[!UICONTROL Text Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), debe utilizar inyecciones de metadatos para especificar el conjunto de caracteres utilizado para codificar los archivos .txt.

Consulte [Adición de definiciones](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de inyección de campo.

## ¿Cómo es que las fuentes chinas, japonesas o coreanas aparecen en los resultados de búsqueda de Netscape 4.7 y versiones anteriores? {#section_DF42567063304F918D406AC76529DFB7}

Si su cuenta utiliza la plantilla predeterminada, una de las plantillas listas para usar o una plantilla basada en cualquiera de esas plantillas, puede contener etiquetas de fuente que especifiquen Arial o Helvetica como caras de fuente. Por ejemplo, `<font face="arial, helvetica" size="+1">`. Netscape 4.7 y versiones anteriores no muestra caracteres chinos, japoneses o coreanos cuando se utiliza la cara de fuente Arial o Helvetica. Quite el `face` atributo o reemplace la cara de fuente por una que sea más apropiada para chino, japonés o coreano.

## Recuento de páginas bajo {#reference_4344E3E3CB2948939860F8C078BD7773}

Una página de preguntas más frecuentes que analiza problemas comunes asociados con un recuento de páginas de indexación bajo.

Las siguientes son preguntas comunes sobre el recuento bajo de páginas de indexación:

* [¿Ha examinado su registro de índice?](#section_D6626536DC3D40DDA4A1224F1CB276BF)
* [¿Tiene errores de escritura en la dirección URL?](#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676)
* [¿La página web de puntos de entrada tiene vínculos a otras páginas...](#section_1C2D6ED54E7249268B555D9DC33352B3)
* [Son vínculos a otras páginas del sitio web incrustadas en...](#section_EE34A67D60A844EBB0921C03544FF63E)
* [Son las etiquetas HTML de la página web en una...](#section_F31A2F5D2C284AC084158A5BD763DC5D)
* [¿Ha formado incorrectamente las etiquetas de comentarios HTML en su ...](#section_D1C39D79341845CB9C38579AABDF3A24)
* [¿Su página Web contiene vínculos a páginas de otra...](#section_F8082759184049AAA8FA6342C1F84389)
* [¿Está utilizando un servicio de dominio virtual para su URL...](#section_2861F09EA21A45E6B7E15F032739CDF3)
* [¿Utiliza la página web una etiqueta de actualización de metadatos?](#section_5A2F544C237C49B8B1A7FE0C45371C0D)
* [¿Su página Web utiliza una etiqueta meta robots?](#section_36275A33DDFE4620BABA948F8A63DBD2)
* [¿Su sitio web utiliza un archivo de exclusión de robots?](#section_BF7B663347814F58AD736066C86B7D25)

## ¿Ha examinado su registro de índice? {#section_D6626536DC3D40DDA4A1224F1CB276BF}

El registro de índice contiene información detallada que el robot de búsqueda/comercialización del sitio recopila a medida que indexa el sitio web. El registro incluye una lista de los vínculos rastreados y los errores encontrados. Examinar el registro de índice es el mejor lugar para empezar a determinar por qué no se indexan todas las páginas del sitio web.

Consulte [Visualización del registro de índice completo de un activo o un ensayo...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

Consulte [Visualización del registro de índice incremental de un activo o un ensayo...](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

## ¿Tiene errores de escritura en la dirección URL? {#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676}

Al escribir direcciones URL extensas en formularios HTML, puede introducir uno o más errores tipográficos. Recuerde que las direcciones URL no deben contener espacios. Además, tenga en cuenta que algunos servidores Web administran las direcciones URL de manera que distinguen entre mayúsculas y minúsculas.

En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. En la [!DNL Staged URL Entrypoints] página, compruebe lo siguiente:

* No hay errores tipográficos en las direcciones URL.
* Todos los caracteres de las direcciones URL utilizan la carcasa correcta.
* No hay caracteres de espacio en las direcciones URL.

Para probar los puntos de entrada de la URL, copie y pegue una URL en un navegador web para ver si aparece el sitio web. Si no aparece, vuelva a comprobar que no ha cometido ningún error en la ruta de URL.

Consulte [Acerca de los puntos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

## ¿La página Web de puntos de entrada tiene vínculos a otras páginas del sitio Web? {#section_1C2D6ED54E7249268B555D9DC33352B3}

El robot de búsqueda/comercialización del sitio rastrea su sitio web como lo hace su cliente; siguiendo los vínculos de página en página. Los vínculos deben estar presentes en la página Web de puntos de entrada para que el robot de búsqueda pueda encontrar e indexar otras páginas del sitio.

Consulte [Adición de varios puntos de entrada de URL que desea indizar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## ¿Los vínculos a otras páginas del sitio Web están incrustados en JavaScript? {#section_EE34A67D60A844EBB0921C03544FF63E}

Puede utilizar técnicas de navegación sofisticadas en el sitio web, como acciones de resumen y menús, que utilizan JavaScript para establecer vínculos con otras páginas. Sin embargo, el robot de búsqueda y comercialización del sitio no puede seguir los vínculos incrustados en JavaScript.

Una solución que puede utilizar para superar este problema es colocar vínculos ocultos a otras páginas en el HTML que contiene el código JavaScript. Aunque los clientes de su sitio web no ven estos vínculos, el robot de búsqueda los encuentra y los rastrea. Puede colocar etiquetas ocultas en la parte inferior de la página justo antes de la `</body>` etiqueta. Pueden tener el siguiente aspecto:

```
<a href="/mydir/mypag1.html"></a> 
<a href="/mydir/mypag2.html"></a>
```

Otra solución es enumerar las direcciones URL de las páginas adicionales del sitio web como puntos de entrada para rastrear e indexar. Comience las direcciones URL con `https://` , como se muestra en la siguiente sección:

```
https://www.mydomain.com/mydir/mypag1.html 
https://www.mydomain.com/mydir/mypag2.html
```

Consulte [Adición de varios puntos de entrada de URL que desea indizar](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## ¿Las etiquetas HTML de la página web están en una secuencia no válida? {#section_F31A2F5D2C284AC084158A5BD763DC5D}

La especificación HTML requiere que las etiquetas `<html>`, `<head>`, y `<body>` sigan una secuencia específica en un documento HTML. Las etiquetas de todas las páginas web deben tener la siguiente secuencia:

```
<html> 
<head> 
...  
<i>head tags go here</i> ... 
</head> 
<body> 
...  
<i>body tags go here</i> ... 
</body> 
</html>
```

Si las etiquetas HTML no están en el orden correcto, el robot de búsqueda/comercialización del sitio no puede analizar e indexar correctamente la página web. A continuación se muestra un ejemplo de etiquetas que no están en la secuencia correcta:

```
<body> 
<head> 
...  
<i>head tags are here</i> ... 
</head> 
...  
<i>body tags are here</i> ... 
</body>
```

En ese caso, coloque las etiquetas `<html>`, `<head>`y `<body>` en la secuencia adecuada de la página web.

## ¿Tiene etiquetas de comentarios HTML mal formadas en la página web? {#section_D1C39D79341845CB9C38579AABDF3A24}

Asegúrese de revisar y corregir cuidadosamente los comentarios HTML no válidos en las páginas web.

La especificación HTML requiere que un comentario HTML comience con los caracteres `<!--` y termine con los caracteres `-->`. Es fácil pasar por alto los comentarios con formato incorrecto que provocan que el robot de búsqueda/comercialización del sitio analice incorrectamente las etiquetas de la página web. Un comentario mal formado puede hacer que el robot de búsqueda/comercialización del sitio pierda otras etiquetas importantes que deben analizarse. Tenga en cuenta los comentarios justo antes de la `<body>` etiqueta en su página web.

A continuación se muestra un ejemplo de comentario correctamente formado:

`<!-- This HTML comment is OK. -->`

A continuación se muestra un ejemplo de comentarios mal formados:

```
<!- This HTML comment is improperly formed. -> 
<! This HTML comment is also improperly formed. >
```

## ¿Contiene la página web vínculos a páginas de otro dominio? {#section_F8082759184049AAA8FA6342C1F84389}

A menudo, un sitio Web puede constar de páginas que existen realmente en un servidor Web con una dirección de dominio diferente. Por ejemplo, si la dirección del sitio web principal es la siguiente:

`https://www.mydomain.com/`

El sitio web también puede tener páginas en otro dominio, como por ejemplo:

`https://www.otherdomain.com/`

De forma predeterminada, el robot de búsqueda/comercialización del sitio no sigue los vínculos de un dominio que no sea el principal. Sin embargo, al establecer puntos de entrada adicionales para la cuenta de búsqueda, puede indexar fácilmente varios dominios.

En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Agregue la dirección URL del &quot;punto de entrada al sitio web principal&quot; del sitio. A continuación, agregue puntos de entrada de URL adicionales a cualquier otro dominio que contenga páginas del sitio. Por ejemplo, puede configurar el punto de entrada de la dirección URL principal en:

`https://www.mydomain.com/`

y agregue el siguiente punto de entrada de URL de sitio adicional:

`https://www.otherdomain.com/`

## ¿Está utilizando un servicio de dominio virtual para su URL? {#section_2861F09EA21A45E6B7E15F032739CDF3}

Es posible que esté utilizando un servicio de dominio virtual (a veces llamado &quot;servicio de redirección de dominio&quot;) para proporcionar una mejor dirección URL para que los clientes accedan a su sitio web. Por ejemplo, supongamos que la dirección real del sitio web es la siguiente:

`https://www.myispdomain.com/~myname/mywebpages/`

Sin embargo, se utiliza un servicio de dominio virtual para que los clientes puedan llegar a su sitio en las siguientes direcciones:

`https://myname.adomain.com/`

o

`https://adomain.com/myname/`

De forma predeterminada, el robot de búsqueda/comercialización del sitio no sigue los vínculos de un dominio que no sea el principal. Sin embargo, al establecer puntos de entrada adicionales para la cuenta de búsqueda, puede indexar fácilmente varios dominios.

En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Agregue el &quot;punto de entrada de la dirección URL del sitio web principal&quot; al nombre de dominio virtual del sitio. A continuación, agregue puntos de entrada adicionales al dominio en el que se encuentre el sitio web.

Por ejemplo, podría establecer el punto de entrada de la dirección URL principal en lo siguiente:

`https://myname.adomain.com/`

Y agregue el siguiente punto de entrada de URL de sitio web adicional:

`https://www.myispdomain.com/~myname/mywebpages/`

## ¿Utiliza la página web una etiqueta de actualización de metadatos? {#section_5A2F544C237C49B8B1A7FE0C45371C0D}

Muchos sitios web tienen una página principal que incluye una etiqueta meta refresh entre las `<head>...</head>` etiquetas de forma similar a la siguiente:

`<meta http-equiv="Refresh" content="0;URL=https://www.adomain.com/apath/afile.html">`

En determinadas circunstancias, el robot de búsqueda/comercialización del sitio no puede seguir la URL de actualización meta para indexar el contenido del sitio web. Este problema es fácil de solucionar estableciendo puntos de entrada adicionales.

En el menú de producto, haga clic en **[!UICONTROL Settings]** > Rastreo > **[!UICONTROL URL Entrypoints]**. Agregue otro punto de entrada a la dirección URL de la etiqueta meta refresh.

## ¿Su página Web utiliza una etiqueta meta robots? {#section_36275A33DDFE4620BABA948F8A63DBD2}

A veces las páginas web utilizan etiquetas meta robots para controlar robots web que periódicamente intentan rastrear un sitio web. Las etiquetas Meta robots aparecen entre las `<head>...</head>` etiquetas de una página web y tienen un aspecto similar a la siguiente etiqueta:

`<meta name="robots" content="noindex, nofollow">`

Dado que el robot de búsqueda/comercialización del sitio es en sí mismo un robot web, sigue las indicaciones de la etiqueta meta robots. Al excluir otros robots de esta manera también excluye el robot de búsqueda/comercialización del sitio.

Puede obtener más información sobre los robots web y el Protocolo de exclusión de robots en:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Elimine o modifique la etiqueta meta robots en las páginas web que desee indizar en el sitio web.

## ¿Su sitio web utiliza un archivo de exclusión de robots? {#section_BF7B663347814F58AD736066C86B7D25}

A veces un sitio web tiene una página llamada robots.txt que excluye a todos o algunos robots de rastrearla. Para ver si su sitio web tiene un archivo robots.txt, búsquelo justo debajo del dominio de nivel superior, como se muestra en la siguiente imagen:

`https://www.yourdomain.com/robots.txt`

El contenido del archivo robots.txt tiene un aspecto similar al siguiente:

```
User-agent: * 
Disallow: /
```

Dado que el robot de búsqueda/comercialización del sitio es en sí mismo un robot web, sigue las indicaciones del archivo robots.txt, excluye el robot de búsqueda/comercialización del sitio. Para solucionar este problema, edite el archivo de exclusión de robots (robots.txt) para permitir que el robot de búsqueda/comercialización del sitio rastree e indexe su sitio web de la siguiente manera:

```
User-agent: Atomz/1.0 
Disallow: 
 
User-agent: * 
Disallow: /
```

## Microsoft Office {#reference_A85FCC8A96514A7584F4D2A8AC8111D1}

Página de preguntas más frecuentes que explica la compatibilidad con la indexación y búsqueda de archivos de Microsoft® Office en un sitio web.

Las siguientes son preguntas habituales sobre los archivos de Microsoft Office:

* [¿Qué se indexa en un archivo de Microsoft Office?](#section_8681DADFCFE24B7787B1FC08D431EE28)
* [Qué no se indexa en un archivo de Microsoft Office...](#section_BD53BDABFDD94D7EB0E1F55EC18017BB)
* [Cómo se indexan los archivos de Microsoft Office de forma diferente a las páginas HTML...](#section_C104B44684F340549A6B9EB8F39EDDBB)
* [Cómo evito que los archivos de Microsoft Office se indiquen...](#section_FEBA71274CD14CB99731ADF982087F4C)

## ¿Qué se indexa en un archivo de Microsoft Office? {#section_8681DADFCFE24B7787B1FC08D431EE28}

El contenido completo de los archivos de Microsoft Word, Microsoft Excel y Microsoft PowerPoint está indizado.

Las siguientes partes de un archivo de Microsoft Word están indizadas:

* Título
* Palabras clave
* Asunto (Descripción)
* Contenido basado en texto
* Hipervínculos a otros documentos

Las siguientes partes de un archivo de Microsoft Excel están indizadas:

* Título
* Palabras clave
* Asunto (Descripción)
* Texto en celdas
* Valores de fórmulas numéricas en celdas

Las siguientes partes de un archivo de Microsoft PowerPoint están indizadas:

* Título
* Palabras clave
* Asunto (Descripción)
* Texto en cada diapositiva

## ¿Qué no se indexa en un archivo de Microsoft Office? {#section_BD53BDABFDD94D7EB0E1F55EC18017BB}

Los gráficos contenidos en archivos de Microsoft Office o cualquier texto que forme parte de un gráfico contenido no se indizan. Las definiciones de propiedades personalizadas no se indexan como metadatos. Algunos textos de campos especiales, como encabezados y pies de página de un archivo de PowerPoint, tampoco están indexados.

## ¿Cómo se indexan los archivos de Microsoft Office de forma diferente a las páginas HTML? {#section_C104B44684F340549A6B9EB8F39EDDBB}

La diferencia entre la forma en que el robot de búsqueda indexa los archivos de Microsoft Office y los archivos HTML es que cada archivo HTML es una página individual y un solo archivo de Microsoft Office puede representar cientos de páginas. Por este motivo, cada página se cuenta dentro de un archivo de Microsoft Office como una página independiente en la cuenta de búsqueda.

## ¿Cómo puedo evitar que los archivos de Microsoft Office se indiquen en mi sitio web? {#section_FEBA71274CD14CB99731ADF982087F4C}

Si no desea que el robot de búsqueda rastree e indexe los archivos de Microsoft Office, anule la selección del tipo de contenido **[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

También puede utilizar [!DNL URL Masks] para deshabilitar la indexación de archivos de Microsoft Office.

Introduzca las siguientes máscaras URL:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Si no utiliza expresiones regulares </p> </td> 
   <td colname="col2"> 
    <ul id="ul_DFEC911DA11C484C8E4671A0F00E1F88"> 
     <li id="li_2E50374E3869426B97353A5A8CBE09EC">exclude *.doc </li> 
     <li id="li_9089D11161524D90849CA88F703772B6">exclude *.xls </li> 
     <li id="li_7F6CFC6212E64C04AAF38E21A667C763">exclude *.ppt </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Si utiliza expresiones regulares </p> </td> 
   <td colname="col2"> 
    <ul id="ul_012A45C3EC04460EA09C0ECFB49A8FA9"> 
     <li id="li_0C239F0A536D465F85A98EBF7B6ADF27">excluir regexp ^.*\.doc$ </li> 
     <li id="li_9F91DA35A2A646ACAFF2BA37F9136E2A">excluir regexp ^.*\.xls$ </li> 
     <li id="li_9D768D9EA2DB44FBB00A1979E21672E2">excluir regexp ^.*\.ppt$ </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Consulte [Adición de máscaras URL para indexar o no partes de índice de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Consulte Expresiones [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## MP3 {#reference_7614250EE81C4EEFA43E57A6A74E83D7}

Una página de preguntas más frecuentes que discute el soporte para indexar y buscar archivos de música MP3 en un sitio web.

Las siguientes son preguntas habituales sobre los archivos MP3.

* [¿Cuándo se rastrea e indexa un archivo MP3?](#section_538EA1682C9C47E3A62640BB25D84C36)
* [Qué tengo que hacer para rastrear e indexar...](#section_3CD794446E3545379C14E9F222118665)
* [¿Cómo se reconoce un archivo MP3?](#section_230E7336965A424F96C5CCF1D3C2D103)
* [¿Qué se indexa en un archivo MP3?](#section_E99D252B27CA4946AED3FCD3ABD8779D)
* [¿Un archivo MP3 cuenta como una página?](#section_9910BEB6617D4D2090558CDF6C65D16B)
* [Cómo puedo evitar la indexación de archivos MP3 individuales...](#section_C989DC1D3D3841B38F683A462195DC05)
* [¿Cómo evito que se indiquen los archivos MP3?](#section_305D2B28D1124776B6DC0C62A17827C6)
* [¿Por qué no puedo buscar los archivos MP3 chinos, japoneses o coreanos en mi sitio?](#section_06A48DA3F9E742CC93CC8B5CCD7382FA)

## ¿Cuándo se rastrea e indexa un archivo MP3? {#section_538EA1682C9C47E3A62640BB25D84C36}

Los archivos MP3 se rastrean e indexan de una de las dos maneras siguientes. La forma más común es desde una etiqueta href delimitadora en un archivo HTML:

`<a href="MP3-file-URL"></a>`

Una segunda forma es introducir la URL del archivo MP3 como punto de entrada de URL.

Consulte [Acerca de los puntos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

## ¿Qué tengo que hacer para rastrear e indexar los archivos MP3 en mi sitio? {#section_3CD794446E3545379C14E9F222118665}

Para activar el rastreo y la indexación de MP3 para su cuenta, en el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**. En la [!DNL Staged Content Types] página, seleccione **[!UICONTROL Text in MP3 Music Files]**.

Consulte [Acerca de los tipos](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)de contenido.

## ¿Cómo se reconoce un archivo MP3? {#section_230E7336965A424F96C5CCF1D3C2D103}

Un archivo MP3 se reconoce por su tipo MIME, &quot;audio/mpeg&quot;.

## ¿Qué se indexa en un archivo MP3? {#section_E99D252B27CA4946AED3FCD3ABD8779D}

Los archivos MP3, opcionalmente, almacenan una pequeña cantidad de información textual. Esa información puede incluir el nombre del álbum, nombre del artista, título de la canción, género de la canción, año de lanzamiento y un comentario. Esta información se almacena al final del archivo en lo que se denomina TAG. Los archivos MP3 que contienen información de TAG se indexan de la siguiente manera:

* El título de la canción se trata como el título de una página HTML.
* El comentario se trata como una descripción definida para una página HTML.
* El género se trata como una palabra clave definida para una página HTML.
* El nombre del artista, el nombre del álbum y el año de publicación se tratan como el cuerpo de un documento HTML.

## ¿Un archivo MP3 cuenta como una página? {#section_9910BEB6617D4D2090558CDF6C65D16B}

Sí, cada archivo MP3 rastreado e indexado en su sitio web se cuenta como una página.

## ¿Cómo puedo evitar la indexación de archivos MP3 individuales? {#section_C989DC1D3D3841B38F683A462195DC05}

Rodee las etiquetas delimitadoras que se vinculan a los archivos MP3 con `<nofollow>` y `</nofollow>` etiquetas. El robot de búsqueda no sigue los vínculos entre esas etiquetas.

Otro método es añadir las direcciones URL de los archivos MP3 como máscaras de exclusión.

Consulte [Acerca de las máscaras](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

Consulte [Acerca del script](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)de máscaras URL.

## ¿Cómo evito que se indiquen los archivos MP3? {#section_305D2B28D1124776B6DC0C62A17827C6}

La forma más sencilla de controlar la indexación de MP3 para su cuenta es anular la selección **[!UICONTROL Text in MP3 Music Files]** en la [!DNL Staged Content Types] página.

Consulte [Selección de tipos de contenido para rastrear e indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

También puede utilizar la función Máscaras URL para desactivar la indexación MP3 por extensión de archivo. Para ello, en el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Introduzca una de las siguientes máscaras:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Si su cuenta... </p> </th> 
   <th colname="col2" class="entry"> <p>Introduzca la siguiente máscara URL </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>No utiliza expresiones regulares </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> exclude *.mp3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utiliza expresiones regulares </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> excluir regexp ^.*\.mp3$ </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte Expresiones [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## ¿Por qué no puedo buscar los archivos MP3 chinos, japoneses o coreanos en mi sitio? {#section_06A48DA3F9E742CC93CC8B5CCD7382FA}

Para buscar archivos MP3 chinos, japoneses o coreanos, en el menú del producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]** > **[!UICONTROL Text in MP3 Music Files]**. A continuación, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]** y especifique el conjunto de caracteres utilizado para codificar los archivos MP3.

Consulte [Selección de tipos de contenido para rastrear e indexar](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

Consulte [Acerca de las inyecciones](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

## PDF {#reference_F127C4915A0D436DA34E5D75ABFBB21B}

Una página de preguntas más frecuentes que analiza la compatibilidad con la indexación y búsqueda de archivos PDF en un sitio web.

Las siguientes son preguntas habituales sobre los archivos PDF:

* [¿Qué se indexa en un archivo PDF?](#section_62BFCD7158B44F2BB3B1864224B50174)
* [¿Qué no se indexa en un archivo PDF?](#section_A14B353AE503408896BACBBF3F748FA0)
* [¿Cómo se cuentan los archivos PDF indexados?](#section_C35DE36A65D649BD8FF314E9EFD990A6)
* [¿Pueden los resultados de la búsqueda mostrar un icono PDF?](#section_829CE82CC3544502A13D27C4DB820189)
* [¿Pueden los resultados de la búsqueda vincularse a una página en particular en...](#section_A06E7F7017E6441E98209D288EE57BF6)
* [Cómo evito que los archivos PDF se indiquen...](#section_96671419A822486AAC654D8DAD819940)
* [¿Cómo es que no puedo buscar archivos PDF chinos, japoneses o coreanos en mi sitio web?](#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8)

## ¿Qué se indexa en un archivo PDF? {#section_62BFCD7158B44F2BB3B1864224B50174}

El contenido completo de los archivos PDF se indexan. Las siguientes partes de un archivo PDF están indizadas:

* Título
* Palabras clave
* Asunto (Descripción)
* Contenido basado en texto

## ¿Qué no se indexa en un archivo PDF? {#section_A14B353AE503408896BACBBF3F748FA0}

La tabla de contenido del PDF, los gráficos del archivo o cualquier texto que forme parte de un gráfico contenido no se indizan.

## ¿Cómo se cuentan los archivos PDF indexados? {#section_C35DE36A65D649BD8FF314E9EFD990A6}

Cada archivo PDF se cuenta como un solo documento, incluidos los archivos PDF que contienen varias páginas.

## ¿Pueden los resultados de la búsqueda mostrar un icono PDF? {#section_829CE82CC3544502A13D27C4DB820189}

Sí. Utilice la `<search-if-link-extension>` etiqueta de la plantilla para incluir un icono de PDF u otros gráficos o texto en los resultados de la búsqueda:

```
<search-results> 
  ... 
  <search-if-link-extension value=".pdf"> 
    <img src="/search/i/pdficon.gif"> 
  </search-if-link-extension> 
  ... 
</search-results>
```

Los iconos de PDF ayudan a los clientes a saber que un resultado de búsqueda se vincula a un archivo PDF que puede ser muy grande. El tamaño del archivo puede ser importante para los clientes que acceden al sitio web a través de un módem o en un dispositivo móvil.

## ¿Pueden los resultados de la búsqueda vincularse a una página concreta de un archivo PDF? {#section_A06E7F7017E6441E98209D288EE57BF6}

Sí. Con la etiqueta de plantilla de vínculos inteligentes ( `<search-smart-link>...</search-smart-link>`), los clientes pueden hacer clic para abrir la primera página PDF que contenga el resultado de la búsqueda.

Para utilizar vínculos inteligentes, reemplace las `<search-link>...</search-link>` etiquetas de la sección de resultados de búsqueda de la plantilla por `<search-smart-link>...</search-smart-link>` etiquetas. Cuando un cliente hace clic en un vínculo que generan las etiquetas de vínculos inteligentes, se dirige a la primera página PDF relevante para la consulta de búsqueda.

>[!NOTE]
>
>Para utilizar esta función, el cliente debe utilizar una versión reciente de Adobe Acrobat o Adobe Acrobat Reader, que debe incluir el complemento de resaltado y el complemento Controlador de ventana externa (EWH). Además, su explorador Web debe utilizar el complemento Adobe Acrobat para Netscape Navigator (puede utilizar cualquier explorador que acepte este complemento de Netscape Navigator) o el control Acrobat ActiveX para Internet Explorer 4.0 y posterior.

Consulte [Buscar etiquetas](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de plantilla.

## ¿Cómo puedo evitar que los archivos PDF se indiquen en mi sitio web? {#section_96671419A822486AAC654D8DAD819940}

Si no desea que el robot de búsqueda rastree e indexe archivos PDF, anule la selección del tipo de contenido **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

También puede optar por utilizar [!DNL URL Masks] para deshabilitar la indexación de PDF.

Consulte [Adición de máscaras URL para indexar o no partes de índice de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Para desactivar la indexación de PDF, introduzca una de las siguientes máscaras URL:

* `exclude *.pdf` (si no utiliza expresiones regulares)
* `exclude regexp ^.*\.pdf$` (si utiliza expresiones regulares)

Consulte Expresiones [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## ¿Cómo es que no puedo buscar archivos PDF chinos, japoneses o coreanos en mi sitio web? {#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8}

La búsqueda/comercialización de sitios obtiene UTF-8 de archivos PDF sin indicación de idioma. Si ha seleccionado el tipo de contenido **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), debe utilizar inyecciones de metadatos para especificar el idioma que se utiliza en el archivo PDF.

Consulte [Adición de definiciones](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE)de inyección de campo.

## Demasiadas páginas {#reference_48A748BC1ED14844ACAC2735C8388E8A}

Una página de preguntas más frecuentes que explica algunas de las razones por las que el indizador ha contabilizado más páginas de las que realmente tiene y cuál es la solución en cada caso.

Si está seguro de que su sitio web está por debajo del límite de páginas, pero el indizador le indica que se ha alcanzado el límite, debe revisar estas preguntas comunes y las respuestas para encontrar posibles soluciones.

* [¿Ha examinado los distintos registros de índice?](#section_C929BF9FDA6B4C9A9078C45AFE80EFE8)
* [¿Se están indexando los programas CGI en el sitio web?](#section_86ED8A641B3841EC80153B4F107548FD)
* [¿Su servidor tiene habilitada la exploración de directorios?](#section_073C88EEE74F4CA0AD2C7145D4810B22)
* [¿Hay foros o grupos de noticias en el sitio web?](#section_8DCB94F0850A41B9B2EA885F779E2F84)
* [¿Hay archivos PDF o de Microsoft Office en el sitio web?...](#section_455FC5438DF74E68AB9A31D359EAD4D9)
* [¿Tiene varios puntos de entrada de URL?](#section_8C54AFD7DF56472A9364D516482B534C)
* [¿Ha excedido los bytes internos o los límites de tiempo de...](#section_AE1BE61A58864FFE81F0BCEED2EBB15D)

## ¿Ha examinado los distintos registros de índice? {#section_C929BF9FDA6B4C9A9078C45AFE80EFE8}

El registro de índice contiene información detallada recopilada por el robot de búsqueda/comercialización del sitio al indizar el sitio web. El registro incluye una lista de todos los vínculos rastreados y los errores encontrados. Examinar el registro de índice es el mejor lugar para comenzar cuando intenta determinar qué páginas se indexan.

Consulte [Visualización del registro de índice completo de un activo o un ensayo...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

Consulte [Visualización del registro de índice incremental de un activo o un ensayo...](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

Consulte [Visualización del registro de índice incremental con secuencias de comandos de un archivo activo o...](../c-about-index-menu/c-about-scripted-index.md#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7).

Consulte [Visualización del registro de índice regenerado de un activo o un ensayo...](../c-about-index-menu/c-about-regenerate-index.md#task_61CE8F9E7BF84BA89A8D482B2106BB15).

Consulte [Visualización del registro de índice reclasificado de un sitio Web](../c-about-index-menu/c-about-re-rank-index.md#task_3C76107DFAC1495FACD3ABB0A688208D)activo o en etapas.

## ¿Se están indexando los programas CGI en el sitio web? {#section_86ED8A641B3841EC80153B4F107548FD}

Los programas CGI utilizan parámetros de URL que en ocasiones hacen que el indizador rastree varias URL &quot;falsas&quot;. Si la búsqueda o comercialización del sitio está leyendo los programas CGI y las direcciones URL siguientes con parámetros CGI en ellos, es probable que haya varios múltiplos de páginas rastreadas e indizadas que no sean útiles para el índice de búsqueda. Los parámetros CGI típicos aparecen en direcciones URL con `?` o `&` caracteres.

Puede ocultar que los programas CGI se indiquen mediante la función Máscaras URL. Puede enmascarar un prefijo URL o utilizar expresiones regulares para enmascarar las secuencias de comandos CGI.

Consulte [Acerca de las máscaras](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

Consulte [Acerca del script](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B)de máscaras URL.

Consulte Expresiones [regulares](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## ¿Su servidor tiene habilitada la exploración de directorios? {#section_073C88EEE74F4CA0AD2C7145D4810B22}

Cuando un servidor web tiene habilitada la exploración de directorios y no hay ningún archivo index.html presente en un directorio determinado, una visita a ese directorio puede mostrar la lista de archivos de ese directorio. Generalmente, hay vínculos en la parte superior de la página que permiten ordenar la lista de diferentes maneras haciendo clic en **[!UICONTROL Name]**, **[!UICONTROL Last modified]**, **[!UICONTROL Size]**, etc. Generalmente, aparecen en el registro de índice de búsqueda/comercialización del sitio como direcciones URL con caracteres como, por ejemplo, `?M=A` al final. El indizador de mercadotecnia/búsqueda del sitio los sigue como vínculos y esto puede llevar a indexar varias direcciones URL &quot;falsas&quot;.

Normalmente, un sitio web bien diseñado tiene archivos de índice ubicados en cada directorio o tiene la exploración de directorios deshabilitada para aquellos directorios que no tienen archivos de índice. Afortunadamente, existe una manera fácil de enmascarar estas direcciones URL &quot;falsas&quot; si no puede cambiar las páginas o deshabilitar las listas de directorios en el servidor.

Para realizar esta tarea, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Agregue una máscara para enmascarar cualquier dirección URL que contenga el carácter `?`. Puede realizar esta tarea introduciendo la siguiente máscara de expresión regular:

`exclude regexp ^.*\?.*$`

Después de crear la máscara, asegúrese de volver a indexar el sitio web.

Consulte [Ejecución de un índice completo de un sitio web activo o en un sitio web escalonado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Consulte [Ejecución de un índice incremental de un sitio Web activo o en un sitio Web en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## ¿Hay foros o grupos de noticias en el sitio web? {#section_8DCB94F0850A41B9B2EA885F779E2F84}

Si se rastrean foros o grupos de noticias en el sitio web, es posible que siga las direcciones URL de diferentes opciones de visualización u opciones de ordenación. Este comportamiento significa que la misma página se indiza varias veces.

Generalmente, los foros o grupos de noticias vienen con sus propios motores de búsqueda. En ese caso, puede usar [!DNL URL Masks] para enmascarar los foros desde la búsqueda o comercialización del sitio.

En el menú de producto, haga clic en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. En la [!DNL Staged URL Masks] página, enmascara los foros introduciendo sus direcciones URL como máscaras de URL de exclusión.

Consulte [Adición de máscaras URL para indexar o no partes de índice de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Después de crear las máscaras, asegúrese de volver a indexar el sitio web.

Consulte [Ejecución de un índice completo de un sitio web activo o en un sitio web escalonado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Consulte [Ejecución de un índice incremental de un sitio Web activo o en un sitio Web en etapas...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## ¿Hay archivos PDF o de Microsoft Office en el sitio web? {#section_455FC5438DF74E68AB9A31D359EAD4D9}

Si tiene archivos PDF o [!DNL Microsoft Office] archivos en el sitio web, puede que observe que el tamaño de índice de sólo unos pocos archivos cuenta muchas páginas. El motivo por el que se indexan más páginas que documentos es que cada página de un archivo PDF o de Microsoft Office se cuenta como una página independiente.

En el menú de producto, haga clic en **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**. En la [!DNL Full Index] página, seleccione **[!UICONTROL Count All Pages]** y, a continuación, haga clic en **[!UICONTROL Full Index Now]** para ver el recuento total de páginas. Si no desea indizar archivos PDF o archivos de Microsoft Office, puede desactivar este tipo de contenido en **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.

Consulte [Ejecución de un índice completo de un sitio web activo o en un sitio web escalonado...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Consulte [Acerca de los tipos](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)de contenido.

## ¿Tiene varios puntos de entrada de URL? {#section_8C54AFD7DF56472A9364D516482B534C}

El robot de búsqueda y comercialización del sitio comienza a rastrear en los puntos de entrada de URL especificados y sigue todos los vínculos encontrados a todo el contenido de ese dominio en particular. Si ha especificado muchos puntos de entrada de URL, es posible que se rastree un número significativo de páginas.

Utilice la `nofollow` etiqueta del protocolo de exclusión de robots en los encabezados de los documentos de puntos de entrada de los dominios adicionales de la siguiente manera:

```
<html> 
<head> 
<meta name="robots" content="nofollow"> 
</head>
```

El código de arriba indica al robot de búsqueda/comercialización del sitio que indexe el contenido de la página, pero no que siga los vínculos a páginas adicionales.

Puede obtener más información sobre los robots web y el Protocolo de exclusión de robots en:

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Si no tiene acceso al origen de las páginas en dominios adicionales, puede eliminar los puntos de entrada de varias direcciones URL. Esto le ayuda a limitar la actividad de indexación solo a los dominios cuyo contenido desee que puedan buscar los clientes.

Consulte [Acerca de los puntos de entrada](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)de URL.

## ¿Ha excedido los bytes internos o los límites de tiempo de la búsqueda o comercialización del sitio? {#section_AE1BE61A58864FFE81F0BCEED2EBB15D}

Compruebe si su cuenta ha alcanzado el límite en la pantalla &quot;Estado de índice completo&quot;. Si el estado informa de que el índice es mayor de lo permitido o que ha tardado más tiempo del permitido, el sitio web no se indexará completamente. Puede corregir este error para obtener una cobertura y un recuento adecuados de las páginas del sitio web.

Para proteger los servidores de mercadotecnia/búsqueda del sitio, existen límites internos de bytes y tiempo. Sólo cuando los archivos rastreados son muy grandes, o cuando el servidor al que la búsqueda o comercialización del sitio está tratando de llegar es lento se alcanzan estos límites.

Si ha alcanzado un límite de tiempo, asegúrese de que el servidor está en línea e intente de nuevo el índice más tarde. Si alcanza un límite de bytes, compruebe los archivos rastreados visualizando el registro de índice. ¿Son inusualmente grandes? Póngase en contacto con la asistencia técnica si ve cualquiera de estos mensajes.
