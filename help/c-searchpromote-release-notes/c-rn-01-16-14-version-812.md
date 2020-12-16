---
description: 'null'
seo-description: 'null'
seo-title: Notas de revisión de Search&Promote 8.12.0 (16/01/2014)
solution: Target
title: Notas de revisión de Search&Promote 8.12.0 (16/01/2014)
topic: Release Notes,Site search and merchandising
uuid: 4db10eb4-11bf-4483-a7f2-87981d9c7a50
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 74%

---


# Notas de la versión de Search&amp;Promote 8.12.0 (16/01/2014){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nuevas funciones y mejoras </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Se han agregado diccionarios de lematización </p> </td> 
   <td colname="col2"> <p> </p> <p> Se han agregado diccionarios de lematización para los idiomas indonesio y turco. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" format="dita" scope="local"> Acerca de los diccionarios</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Exportación de informes </p> </td> 
   <td colname="col2"> <p> 
     <!--3683368-->Ahora puede exportar datos a CSV desde los siguientes informes: 
     <ul id="ul_93B619DBB3444F64BD6D7F9E969AB1E1"> 
      <li id="li_96DDE1A196834845A0FA319903C5934B"> <p>Informe Términos </p> </li> 
      <li id="li_4F1A19DE98C84F8CAD963EEA2B38ED7A"> <p>Informe Términos de búsqueda nulos </p> </li> 
      <li id="li_A7716C62C4D44CD69D411C3FEE246D96"> <p>Informe de solicitud de búsqueda </p> </li> 
     </ul> </p> <p>Consulte <a href="../c-about-reports-menu/c-about-reports-menu.md#concept_5F901459C7AB461BAB30B305957EB00C" format="dita" scope="local"> Acerca del menú Informes</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>No asociar </p> </td> 
   <td colname="col2"> <p>Ahora puede controlar qué dos palabras no se deben asociar en los resultados de búsqueda, por ejemplo, "camisa" y "camiseta". </p> <p> <p>Nota: Esta característica no está activada de forma predeterminada. Póngase en contacto con el servicio de atención al cliente de Adobe para activar la característica en Search&amp;Promote y poderla utilizar. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* No se podía agregar resultados en una zona Recomendados que se encontrara fuera de los criterios de cuadros seleccionados.
* No se podían guardar reglas basadas en resultados para una cuenta con HTTPS (solo búsqueda).
* La configuración de la regla comercial para &quot;no es un teléfono móvil&quot; no funcionaba.

   Consulte [Acerca de las reglas comerciales](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Realizar una búsqueda de filtro de inventario no producía resultados.
* El orden del cuadro Tamaño no se actualizaba.
* Se ha añadido la opción para añadir una definición de regla &quot;personalizada&quot; en la página Limpieza de consultas.

   Consulte [Acerca de las reglas de limpieza de Consultas](../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C).

* El informe Términos repetía entradas si no había datos suficientes.

   Consulte [Visualización del informe Términos o del informe Términos de búsqueda nulos...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* La aplicación de una sola regla comercial funcionaba en el modo Provisional, pero producía errores en el modo Activo.
* Las ediciones de autocompletar para las listas de inclusión o exclusión no se guardaban en el historial y, por lo tanto, no se podían revertir.

   Consulte [Acerca de Autocompletar](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578).

