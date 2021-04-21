---
description: Search&amp;Notas de la versión de Promote 15.3.1.
solution: Target
title: Search&amp;Promote 15.3.1 Notas de la versión (24/03/2015)
topic-legacy: Release Notes,Site search and merchandising
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
exl-id: 2d254275-f777-45e5-a838-b6a35365a6dd
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 1%

---

# Notas de la versión 15.3.1 de Search&amp;Promote (24/03/2015){#search-promote-release-notes}

## Nuevas funciones y mejoras {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Búsqueda de números de modelos de producto : se ha agregado una nueva configuración de Lingüística que permite dividir los tokens de forma opcional en transiciones alfabético-numéricas. Esta funcionalidad permite hacer coincidir texto libre de forma más flexible en tokens de estilo de producto o parte.

   Consulte **[!UICONTROL Partial Alphanumeric Matching]** en [Configuración de la coincidencia de los términos de búsqueda con el contenido web...](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616).

* Capacidad añadida para exportar resultados de vistas de datos.

   Consulte [Acerca de las vistas de datos](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3).

* Rangos generados dinámicamente para características de agrupamiento de valor de faceta automática de atributos de rango.

   Actualmente, Adobe Systems requiere que proporcione contenido que identifique los valores de rango para hacerlo. Por ejemplo, para un precio de 10, genere una cadena de rango &quot;Entre 10 y 20 dólares&quot;). O bien, Adobe Systems requiere que utilice el filtrado con secuencias de comandos. Se han agregado nuevos atributos a una definición de campo de metadatos, solo para campos `Type=Number`. Las nuevas opciones asocian el campo numérico con un campo `Type=Text` y especifican la información de configuración que describe cómo se crea la descripción del rango.

   Consulte [Adición de un nuevo campo de metaetiqueta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Correcciones {#section_22D1AFC99F394D569898828A0D3C419D}

* El cuadro de diálogo de edición de raíl de faceta debe incluir facetas organizadas.
* Resultados de búsqueda principales vacíos para el modo de búsqueda &quot;incrustada&quot;, para una búsqueda que contenga caracteres japoneses.
* La conversión tika de archivos .docx de Word ahora rellena el atributo `title`.
* Se han corregido los mensajes erróneos de &quot;banner duplicado&quot; en el administrador **[!UICONTROL Banner]**.
* [!DNL Dynamic Media Classic] los banners ahora no son compatibles con los protocolos.
* El atributo de campo **[!UICONTROL Table Name]** a veces se ocultaba al editar campos definidos por el usuario en la interfaz de usuario de metadatos, incluso cuando **[!UICONTROL Dynamic Facets]** estaba habilitado para la cuenta.
* **[!UICONTROL Recent Searches]** ya no codifica de forma múltiple los caracteres que no sean ASCII.
* Los campos MDI se pueden rellenar sin recurrir al filtrado de secuencias de comandos.
* Codificación incorrecta en las sugerencias.
* el déclencheur &quot;otras facetas seleccionadas&quot; ahora funciona correctamente con reglas comerciales complejas.
