---
description: Search&amp;Notas de la versión de Promote 8.9.4.
solution: Target
title: Search&amp;Promote 8.9.4 Notas de la versión (17/01/2013)
topic: Notas de la versión, búsqueda de sitios y comercialización
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 33%

---


# Notas de la versión 8.9.4 de Search&amp;Promote (17/01/2013){#search-promote-release-notes}

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
   <td colname="col2"> <p> Se ha añadido la capacidad de crear notas en línea al crear reglas de limpieza de consultas, reglas Pre-Search y reglas Post-Search. El campo de notas permite documentar y explicar las reglas. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local"> Acerca de las reglas de limpieza de consultas</a>. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local"> Acerca de las reglas de búsqueda previa</a>. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local"> Acerca de las reglas posteriores a la búsqueda</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Búsqueda guiada </p> </td> 
   <td colname="col2"> <p> Se han agregado etiquetas de Búsqueda guiada para indicar el tiempo total que duró una búsqueda. </p> <p> <span class="codeph"> &lt;guided-search-time&gt;</span> : identifica cuánto tiempo tardó la búsqueda. El valor de tiempo de búsqueda devuelto se especifica en ms. </p> <p> <span class="codeph"> &lt;guided-fall-through-searches&gt;</span> - Devuelve el recuento de las búsquedas principales que se utilizan para crear la página de resultados de búsqueda. </p> <p> <span class="codeph"> &lt;guided-if-fall-through-search&gt;</span> - Comprueba si el recuento de búsquedas principales es bueno a 1. </p> <p>Consulte también Idioma diverso en <a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local"> etiquetas de plantilla de presentación</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* El Informe de términos ahora ignora el carácter de asterisco.

   Consulte [Visualización del informe Términos o del informe Términos de búsqueda nulos...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Abra **[!UICONTROL Reports > Null Search Terms Report]**, seleccione un intervalo de tiempo y luego vea el informe. Haga clic sobre una palabra del informe para abrir la búsqueda y luego haga clic sobre Ver informe otra vez. El recuento de búsqueda de la palabra clave en que ha hecho clic se duplicaba. Ahora esto está corregido. 

   Consulte [Visualización del informe Términos o del informe Términos de búsqueda nulos...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Se ha realizado una optimización del rendimiento para cuando se insertan reglas comerciales en vivo.

   Consulte [Acerca de las reglas comerciales](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* La capacidad de eliminación en [!DNL Breadcrumbs] no siempre funcionaba. 

   Consulte [Acerca de las rutas de exploración](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

* A menos que se utilizara la regeneración, la función de reclasificación no permitía que ninguna regla de clasificación modificada tuviera efecto en los resultados de búsqueda.

   Consulte [Acerca de reglas de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

   Consulte [Acerca del Índice de reclasificación](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692).

