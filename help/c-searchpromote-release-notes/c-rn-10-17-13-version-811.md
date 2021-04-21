---
description: Search&amp;Notas de la versión de Promote 8.11.0.
solution: Target
title: Search&amp;Promote 8.11.0 Notas de la versión (29/10/2013)
topic-legacy: Release Notes,Site search and merchandising
uuid: 973f9608-a5c7-4571-ae2b-6f1fa05bc862
exl-id: b417b275-7b04-4855-9e2a-9de0faa262cc
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 58%

---

# Notas de la versión de Search&amp;Promote 8.11.0 (29/10/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nueva función </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Descomponedor para danés </p> </td> 
   <td colname="col2"> <p> Ahora se proporciona un mecanismo que permite a <span class="keyword"> Search&amp;Promote de Adobe</span> acceder a los servicios de detección de idioma (danés), descomposición, derivación y segmentación proporcionados por Adobe. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Mejoras y correcciones**

* Se han realizado mejoras en las capacidades de coincidencia de tablas [!DNL Search&Promote] existentes. Las mejoras ofrecen más compatibilidad con los requisitos de los clientes asociados con las relaciones cada vez más complejas entre SKU y los datos de producto.

   >[!NOTE]
   >
   >Esta función no está activada de forma predeterminada. Póngase en contacto con el servicio de atención al cliente de Adobe para activar la característica en Search&amp;Promote y poderla utilizar.

* Se ha agregado una opción que permite que la búsqueda guiada ordene las facetas mediante la configuración de idioma de la cuenta.

   >[!NOTE]
   Esta función no está activada de forma predeterminada. Póngase en contacto con el servicio de atención al cliente de Adobe para activar la característica en Search&amp;Promote y poderla utilizar.

* Se ha agregado una opción para aumentar el número de valores de facetas que un usuario puede especificar para las facetas multiselección.

   >[!NOTE]
   Esta función no está activada de forma predeterminada. Póngase en contacto con el servicio de atención al cliente de Adobe para activar la característica en Search&amp;Promote y poderla utilizar.

* Se ha agregado la opción de casilla de verificación **[!UICONTROL Only allow searches that use HTTPS]** a **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Restrictions]**.

   Consulte [Acerca de las restricciones](../c-about-settings-menu/c-about-searching-menu.md#concept_B5B527E04EBF4E9AB5956EEF881DDBF1).

* Se ha añadido una opción a **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]** > **[!UICONTROL Create Feed]** > **[!UICONTROL Generic Feed]** para conservar los caracteres de tabulación en el panel [!DNL File Submission] del asistente.

   Consulte [Creación de una fuente](../c-about-settings-menu/c-about-searching-menu.md#task_63179C1FC359497483CD6CE13FD1C250).

* Se ha aumentado el tamaño de los datos que se aceptan en cada uno de los campos superiores e inferiores para el nuevo formulario de definición de facetas de 80 a 1000 caracteres.

   Consulte [Acerca de las facetas](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

* Los parámetros de depuración de búsqueda guiada ahora informan correctamente de los números de reglas comerciales.
* Las reglas comerciales se aplican ahora en el entorno Live.
* La búsqueda por proximidad ya funciona al buscar por longitud/latitud para las cuentas configuradas con Idioma = &quot;Danés (Dinamarca)&quot;.
* Los desencadenantes basados en resultados sin programación asignada ahora se desencadenan.
* Ahora se generan informes de resultados coherentes al utilizar la opción **[!UICONTROL Ignore Apostrophes]** en **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**.

   Consulte [Acerca de las palabras y el idioma](../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79).

* La interfaz de usuario de listas de palabras de compleción automática ya funciona con números altos de facetas.
