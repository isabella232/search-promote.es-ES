---
description: 'null'
seo-description: 'null'
seo-title: Search&amp;Promote 8.9.4 Notas de la versión (17/01/2013)
solution: Target
title: Search&amp;Promote 8.9.4 Notas de la versión (17/01/2013)
topic: Release Notes,Site search and merchandising
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.9.4 Release Notes (01/17/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nuevas funciones y mejoras </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Reglas </p> </td> 
   <td colname="col2"> <p> Se ha añadido la capacidad de crear notas en línea al crear reglas de limpieza de consultas, reglas Pre-Search y reglas Post-Search. El campo de notas permite documentar y explicar las reglas. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local"> Acerca de las reglas</a>de limpieza de consultas. </p> <p>See <a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local"> About Pre-Search Rules</a>. </p> <p>See <a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local"> About Post-Search Rules</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Búsqueda guiada </p> </td> 
   <td colname="col2"> <p> Se agregaron etiquetas de Búsqueda guiada para indicar el tiempo total que tardó una búsqueda. </p> <p> <span class="codeph"> &lt;guided-search-time&gt;</span> : identifica cuánto tardó la búsqueda. El valor de tiempo de búsqueda devuelto se especifica en ms. </p> <p> <span class="codeph"> &lt;guided-fall-through-searches&gt;</span> : devuelve el recuento de búsquedas principales que se utilizan para generar la página de resultados de búsqueda. </p> <p> <span class="codeph"> &lt;guided-if-fall-through-search&gt;</span> : prueba si el recuento de búsquedas principales es bueno a 1. </p> <p>Consulte también Idioma diverso en las etiquetas <a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local"> de plantilla de</a>presentación. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* El Informe de términos ahora ignora el carácter de asterisco.

   Consulte [Visualización del informe Términos o del informe Términos de búsqueda nulos...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Abra Informes > Informe de términos de búsqueda nulos, seleccione un intervalo de tiempo y luego vea el informe. Haga clic sobre una palabra del informe para abrir la búsqueda y luego haga clic sobre Ver informe otra vez. El recuento de búsqueda de la palabra clave en que ha hecho clic se duplicaba. Ahora esto está corregido. 

   Consulte [Visualización del informe Términos o del informe Términos de búsqueda nulos...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Se ha hecho una optimización del rendimiento para cuando se pulsa Activar reglas de negocios.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* La capacidad de eliminación en Breadcrumbs no siempre funcionaba. 

   Consulte [Acerca de las rutas de exploración](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

* A menos que se utilizara Regenerar, la función Volver a clasificar no permitía que ninguna regla de clasificación modificada tuviera efecto en los resultados de búsqueda.

   Consulte [Acerca de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

   Consulte [Acerca del índice](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692)de reclasificación.

