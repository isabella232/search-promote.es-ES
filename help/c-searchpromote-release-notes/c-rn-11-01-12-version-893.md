---
description: Search&amp;Notas de la versión de Promote 8.9.3.
solution: Target
title: Search&amp;Promote 8.9.3 Notas de la versión (01/11/2012)
topic: Release Notes,Site search and merchandising
uuid: 7bc7bcb6-f47f-4e05-94e5-a22a13a187b7
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 79%

---


# Notas de la versión de Search&amp;Promote 8.9.3 (01/11/2012){#search-promote-release-notes}

## Notas de la versión de Search&amp;Promote 8.9.3 (01/11/2012) {#concept_85F5B4B4C40C43FEA3AD63E6EA5593CF}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nuevas funciones y mejoras </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Barra de faceta </p> </td> 
   <td colname="col2"> <p> 
     <!--3309390--> Se agregó la nueva opción <span class="uicontrol">Barra de faceta</span> para ayudar a otorgar más control sobre el ordenamiento de familias de facetas y nombres de facetas (por recuento, alfabético). </p> <p>Consulte <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">Acerca de Barra de faceta</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Facetas anidadas </p> </td> 
   <td colname="col2"> <p> Se agregó asistencia técnica para ordenamiento alternado de facetas anidadas. </p> <p>Consulte <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">Acerca de Barra de faceta</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Campo Notas en las reglas de clasificación </p> </td> 
   <td colname="col2"> <p> 
     <!--3063772--> Se agregó un campo multilínea <span class="wintitle">Notas</span> al cuadro de diálogo <span class="wintitle">Agregar métrica de clasificación</span> y el cuadro de diálogo <span class="wintitle">Editar métrica de clasificación</span> para reglas de clasificación y definiciones de grupos de reglas. </p> <p>Las notas de reglas de clasificación se muestran en la página <span class="wintitle">Definir reglas de clasificación</span>. Las notas de grupos de reglas aparecen al editar la definición. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" format="dita" scope="local">Acerca de reglas de clasificación</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reglas comerciales </p> </td> 
   <td colname="col2"> <p> 
     <!--3331637--> Se mejoró la asistencia técnica de páginas de aterrizaje mediante la eliminación de resultados naturales en una regla comercial con la nueva opción <span class="uicontrol">Eliminar todos los resultados</span>. </p> <p>Use esta nueva opción en conjunto con otras acciones de reglas comerciales para crear "páginas de aterrizaje pregrabadas". Es decir, cree el contenido de una página mediante acciones de reglas comerciales exclusivamente y descarte los resultados "naturales" de la búsqueda. </p> <p>Consulte <a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" format="dita" scope="local">Adición de una nueva regla comercial</a> o <a href="../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087" format="dita" scope="local">Edición de una regla comercial</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Titulares y reglas comerciales </p> </td> 
   <td colname="col2"> <p> Se agregó una opción de asistencia técnica donde puede optar condicionalmente por no usar titulares de inserción en directo cuando la regla comercial que hace referencia al titular se inserta en directo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* Las reglas comerciales funcionaban de manera inconsistente cuando había un índice [!DNL Stage].
* Las reglas de clasificación automática ahora se aplican a páginas de aterrizaje pregrabadas.

   Consulte la tabla de opciones en [Adición de una regla de clasificación](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

* [!DNL promosearch.cgi] no devolvía promociones.

   Consulte [Acerca de las búsquedas](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

* A veces las reglas de inserción que hacían referencia a muchos titulares fallaban.

   Consulte [Acerca de los titulares](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA).

* **[!UICONTROL Did You Mean]** el almacenamiento en caché de consultas de búsqueda ahora está deshabilitado.

   Consulte [Acerca de ¿quiso decir?](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E).

