---
description: Search&amp;Notas de la versión de Promote 8.16.0.
solution: Target
title: Search&amp;Promote 8.16.0 Notas de la versión (18/09/2014)
topic-legacy: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
exl-id: 929d6f97-4939-4e37-aded-6a746757b960
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 37%

---

# Notas de la versión 8.16.0 de Search&amp;Promote (18/9/2014){#search-promote-release-notes}

## Notas de la versión 8.16.0 de Search&amp;Promote (18/9/2014) {#topic_5BECD3F66C684987828F6AE65E62DA29}

## Nuevas funciones {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Almacenamiento en caché de los resultados de búsqueda en Búsqueda guiada 3 (GS3): Para configurar esta función personalizada para que pueda usarla en su cuenta, póngase en contacto con el administrador técnico de cuentas de Adobe.
* Actualizaciones verticales para campos modificados con frecuencia : ahora puede actualizar rápidamente todos los valores de un conjunto de campos de metadatos sin necesidad de volver a indexar completamente el contenido.

   Consulte la opción Campo de actualización vertical en la tabla en [Añadir un nuevo campo de metaetiqueta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) y [Acerca de la actualización vertical](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

   Esta función solo se puede usar en cuentas [!DNL Adobe Search&Promote] que utilicen el conector de índice. Si quiere configurar esta función personalizada para que pueda usarla en su cuenta, póngase en contacto con su administrador de cuenta técnica de Adobe.

## Correcciones y mejoras {#section_22D1AFC99F394D569898828A0D3C419D}

* Se corrigió el conector de índice analizando fuentes XML que contenían la cadena `?>`.
* Se corrigieron las fuentes SFTP del conector de índice cuando se aplicaba el recuento mínimo de documento.
* La exportación de informes a Microsoft Excel ahora es compatible con UTF8.
* Búsqueda guiada: la compilación de facetas era lenta.
* Cargador de atributos: los datos agregados tenían claves duplicadas.
* Se corrigió el orden de ejecución erróneo de la regla comercial al publicar una regla individual.
* La búsqueda guiada estaba generando los vínculos Deshacer de facetas erróneas.
* Se agregó una nueva operación de control remoto (`sp_lines=N`) que permite comprobar el progreso y estado de un rastreo de índice en ejecución.

   Consulte [Acerca del control remoto para la indexación](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

* Se necesita enviar información de autenticación cuando la captura elimina información durante el aumento del conector de índice.
* El informe [!DNL Change Log] ahora identifica al usuario que inicia una operación de índice manual.

   Consulte [Visualización del registro de cambios](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

* Al exportar un [!DNL Terms Report], ya no está limitado a 500 o menos elementos en el informe.

   Consulte [Visualización del informe Términos o del informe Términos de búsqueda nulos...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* La configuración del conector de índice **[!UICONTROL Strip HTML]** siempre se mostraba como activada.
* Se experimentaron resultados de búsqueda incoherentes con la función **[!UICONTROL Common Phrases]**.
* La presentación de nombres de atributos se truncaban en los resúmenes de lista de reglas.
* La aplicación de una regla comercial individual estaba publicando todas las reglas comerciales.
