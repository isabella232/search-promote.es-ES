---
description: 'null'
seo-description: 'null'
seo-title: Notas de revisión de Search&Promote 8.14.0 (22/05/2014)
solution: Target
title: Notas de revisión de Search&Promote 8.14.0 (22/05/2014)
topic: Release Notes,Site search and merchandising
uuid: 308d84a9-ec38-4fec-b146-e8a353e65be4
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.14.0 Release Notes (05/22/2014){#search-promote-release-notes}

**Correcciones**

* Si [!DNL sqlite_open] falla, se retira el antiguo archivo de base de datos de sqlite y se crea uno nuevo desde cero.
* Los resultados de búsqueda de núcleo eran incoherentes cuando se repetía la misma búsqueda.
* Mejora de rendimiento de procesamiento de plantillas cuando se presentan muchos campos por resultado de búsqueda.
* Se añadieron notas al Historial de reglas empresariales.
* El rendimiento de los desencadenadores basados en resultados y la fase de generación de vista previa-índice de acciones, durante las operaciones de indexado, se degradaron de forma periódica con el tiempo.
* La opción **Restablecer caché de SPIN** se cambió de booleano no/siguiente ejecución a un triestado: no/siempre/siguiente ejecución.

