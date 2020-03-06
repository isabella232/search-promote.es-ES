---
description: 'null'
seo-description: 'null'
seo-title: Notas de revisión de Search&Promote 8.16.0 (18/9/2014)
solution: Target
title: Notas de revisión de Search&Promote 8.16.0 (18/9/2014)
topic: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.16.0 Release Notes (9/18/2014){#search-promote-release-notes}

## Search&amp;Promote 8.16.0 Release Notes (9/18/2014) {#topic_5BECD3F66C684987828F6AE65E62DA29}

## New features {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Almacenamiento en caché de los resultados de la búsqueda en Búsqueda guiada 3 (GS3): para configurar esta función personalizada para que pueda utilizarla en su cuenta, póngase en contacto con el administrador de cuentas técnicas de Adobe.
* Actualizaciones verticales para campos modificados con frecuencia: ahora puede actualizar rápidamente todos los valores de un conjunto de campos de metadatos sin necesidad de volver a indexar completamente el contenido.

   Consulte la opción Campo de actualización vertical de la tabla en [Adición de un nuevo campo](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) de etiqueta meta y [Acerca de actualización](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)vertical.

   This feature can only be used on [!DNL Adobe Search&Promote] accounts that use Index Connector. Si quiere configurar esta función personalizada para que pueda usarla en su cuenta, póngase en contacto con su administrador de cuenta técnica de Adobe.

## Fixes and enhancements {#section_22D1AFC99F394D569898828A0D3C419D}

* Corrected the Index Connector parsing of XML feeds that contained `?>` string.
* Se corrigieron las fuentes SFTP del conector de índice cuando se aplicaba el recuento mínimo de documento.
* La exportación de informes a Microsoft Excel ahora es compatible con UTF8.
* Búsqueda guiada: la compilación de facetas era lenta.
* Cargador de atributos: los datos agregados tenían claves duplicadas.
* Se corrigió el orden de ejecución erróneo de la regla comercial al publicar una regla individual.
* La búsqueda guiada estaba generando los vínculos Deshacer de facetas erróneas.
* Se agregó una nueva operación de control remoto (`sp_lines=N`) que permite comprobar el progreso y estado de un rastreo de índice en ejecución.

   Consulte [Acerca del control remoto para indización](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

* Se necesita enviar información de autenticación cuando la captura elimina información durante el aumento del conector de índice.
* The [!DNL Change Log] report now identifies the user who initiates a manual index operation.

   See [Viewing the Change Log](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

* When you export a [!DNL Terms Report], you are no longer limited to 500 or less items in the report.

   Consulte [Visualización del informe Términos o del informe Términos de búsqueda nulos...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* The Index Connector **[!UICONTROL Strip HTML]** setting was always displaying as checked.
* Inconsistent search results were experienced with the **[!UICONTROL Common Phrases]** feature.
* La presentación de nombres de atributos se truncaban en los resúmenes de lista de reglas.
* La publicación de una regla comercial individual estaba publicando todas las reglas comerciales.

