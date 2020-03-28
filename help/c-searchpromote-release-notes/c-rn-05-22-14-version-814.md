---
description: 'null'
seo-description: 'null'
seo-title: Notas de revisión de Search&Promote 8.14.0 (22/05/2014)
solution: Target
title: Notas de revisión de Search&Promote 8.14.0 (22/05/2014)
topic: Release Notes,Site search and merchandising
uuid: 308d84a9-ec38-4fec-b146-e8a353e65be4
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5

---


# Search&amp;Promote 8.14.0 Release Notes (05/22/2014){#search-promote-release-notes}

**Correcciones**

* Si [!DNL sqlite_open] falla, se retira el antiguo archivo de base de datos de sqlite y se crea uno nuevo desde cero.
* Los resultados de búsqueda de núcleo eran incoherentes cuando se repetía la misma búsqueda.
* Mejora de rendimiento de procesamiento de plantillas cuando se presentan muchos campos por resultado de búsqueda.
* Notas Añadidas a **[!UICONTROL Business Rule History]**.
* El rendimiento de los desencadenadores basados en resultados y la fase de generación de vista previa-índice de acciones, durante las operaciones de indexado, se degradaron de forma periódica con el tiempo.
* Changed **[!UICONTROL Reset SPIN cache]** option from boolean no/next-run to a tri-state: no/always/next-run.

