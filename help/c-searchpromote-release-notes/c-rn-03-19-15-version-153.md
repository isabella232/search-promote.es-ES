---
description: 'null'
seo-description: 'null'
seo-title: Notas de revisión de Search&Promote 15.3.1 (24/03/2015)
solution: Target
title: Notas de revisión de Search&Promote 15.3.1 (24/03/2015)
topic: Release Notes,Site search and merchandising
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 15.3.1 Release Notes (03/24/2015){#search-promote-release-notes}

## Nuevas funciones y mejoras {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Búsqueda de números de modelo de producto: se ha agregado una nueva configuración de Lingüística que permite dividir los tokens de forma opcional en transiciones alfabético-numéricas. Esta funcionalidad permite una coincidencia de texto libre más flexible en tokens de estilo de producto o parte.

   Consulte **[!UICONTROL Partial Alphanumeric Matching]** en [Configuración de la correspondencia entre los términos de búsqueda y el contenido web...](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616).

* Se ha agregado la capacidad de exportar los resultados de la vista de datos.

   Consulte [Acerca de las vistas](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)de datos.

* Rangos generados dinámicamente para atributos de rango con funciones de bloque de valor de faceta automática.

   Adobe Systems actualmente requiere que proporcione los valores de intervalo de identificación de contenido para realizar esto. Por ejemplo, para un precio de 10, genere una cadena de rango &quot;Entre $10 y $20&quot;). O bien, Adobe Systems requiere que utilice el filtrado por secuencias de comandos. Se han agregado nuevos atributos a una definición de campo de metadatos, solo para `Type=Number` campos. Las nuevas opciones asocian el campo numérico con un `Type=Text` campo y especifican la información de configuración que describe cómo se genera la descripción del rango.

   Consulte [Adición de un nuevo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de etiqueta meta.

## Correcciones {#section_22D1AFC99F394D569898828A0D3C419D}

* El cuadro de diálogo de edición de carril de facetas debe incluir facetas escalonadas.
* Resultados de búsqueda principales vacíos para el modo de búsqueda &quot;incrustado&quot;, para una búsqueda que contenga caracteres japoneses.
* La conversión tika de archivos .docx de Word ahora rellena el `title` atributo.
* Se corrigieron mensajes erróneos de &quot;pancarta duplicada&quot; en el **[!UICONTROL Banner]** administrador.
* Los letreros de Dynamic Media Classic ahora no son compatibles con los protocolos.
* El atributo **[!UICONTROL Table Name]** field se ocultaba a veces al editar campos definidos por el usuario en la interfaz de usuario de metadatos, incluso cuando **[!UICONTROL Dynamic Facets]** estaba habilitado para la cuenta.
* **[!UICONTROL Recent Searches]** ya no codifica de forma múltiple los caracteres que no sean ASCII.
* Los campos MDI se pueden rellenar sin tener que recurrir al filtrado por secuencias de comandos.
* Codificación incorrecta en las sugerencias.
* El activador &quot;otra faceta seleccionada&quot; funciona ahora correctamente con reglas comerciales complejas.

