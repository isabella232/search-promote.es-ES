---
description: 'null'
seo-description: 'null'
seo-title: Notas de revisión de Search&Promote 8.16.0 (18/9/2014)
solution: Target
title: Notas de revisión de Search&Promote 8.16.0 (18/9/2014)
topic: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 37%

---


# Notas de la versión de Search&amp;Promote 8.16.0 (18/9/2014){#search-promote-release-notes}

## Notas de la versión de Search&amp;Promote 8.16.0 (18/09/2014) {#topic_5BECD3F66C684987828F6AE65E62DA29}

## Nuevas funciones {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Almacenamiento en caché de los resultados de la búsqueda en Búsqueda guiada 3 (GS3): para configurar esta función personalizada para que pueda utilizarla en su cuenta, póngase en contacto con el administrador de cuentas técnico de Adobe.
* Actualizaciones verticales para campos modificados con frecuencia: ahora puede actualizar rápidamente todos los valores de un conjunto de campos de metadatos sin necesidad de volver a indexar completamente el contenido.

   Consulte la opción Campo de actualización vertical en la tabla en [Añadir un nuevo campo de etiqueta meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) y [Acerca de actualización vertical](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

   Esta función solo se puede utilizar en cuentas [!DNL Adobe Search&Promote] que utilicen el conector de índice. Si quiere configurar esta función personalizada para que pueda usarla en su cuenta, póngase en contacto con su administrador de cuenta técnica de Adobe.

## Correcciones y mejoras {#section_22D1AFC99F394D569898828A0D3C419D}

* Se corrigió el conector de índice analizando las fuentes XML que contenían la cadena `?>`.
* Se corrigieron las fuentes SFTP del conector de índice cuando se aplicaba el recuento mínimo de documento.
* La exportación de informes a Microsoft Excel ahora es compatible con UTF8.
* Búsqueda guiada: la compilación de facetas era lenta.
* Cargador de atributos: los datos agregados tenían claves duplicadas.
* Se corrigió el orden de ejecución erróneo de la regla comercial al publicar una regla individual.
* La búsqueda guiada estaba generando los vínculos Deshacer de facetas erróneas.
* Se agregó una nueva operación de control remoto (`sp_lines=N`) que permite comprobar el progreso y estado de un rastreo de índice en ejecución.

   Consulte [Acerca del control remoto para indización](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

* Se necesita enviar información de autenticación cuando la captura elimina información durante el aumento del conector de índice.
* El informe [!DNL Change Log] ahora identifica al usuario que inicia una operación de índice manual.

   Consulte [Visualización del registro de cambios](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

* Al exportar un [!DNL Terms Report], ya no está limitado a 500 o menos elementos en el informe.

   Consulte [Visualización del informe Términos o del informe Términos de búsqueda nulos...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* El ajuste Conector de índice **[!UICONTROL Strip HTML]** siempre se mostraba como marcado.
* Se experimentaron resultados de búsqueda incoherentes con la función **[!UICONTROL Common Phrases]**.
* La presentación de nombres de atributos se truncaban en los resúmenes de lista de reglas.
* Impulsar una regla comercial individual en vivo estaba impulsando todas las reglas comerciales en vivo.

