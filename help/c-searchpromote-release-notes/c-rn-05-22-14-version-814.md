---
description: Search&amp;Notas de la versión de Promote 8.14.0.
solution: Target
title: Search&amp;Promote 8.14.0 Notas de la versión (22/05/2014)
topic-legacy: Release Notes,Site search and merchandising
uuid: 308d84a9-ec38-4fec-b146-e8a353e65be4
exl-id: fcc00d85-128e-4015-aa82-7d31606cb076
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 67%

---

# Notas de la versión 8.14.0 (22/05/2014){#search-promote-release-notes}

**Correcciones**

* Si [!DNL sqlite_open] falla, se retira el antiguo archivo de base de datos de sqlite y se crea uno nuevo desde cero.
* Los resultados de búsqueda de núcleo eran incoherentes cuando se repetía la misma búsqueda.
* Mejora de rendimiento de procesamiento de plantillas cuando se presentan muchos campos por resultado de búsqueda.
* Se agregaron notas a **[!UICONTROL Business Rule History]**.
* El rendimiento de los desencadenadores basados en resultados y la fase de generación de vista previa-índice de acciones, durante las operaciones de indexado, se degradaron de forma periódica con el tiempo.
* Se ha cambiado la opción **[!UICONTROL Reset SPIN cache]** de booleano no/siguiente ejecución a un triestado: no/always/next-run.
