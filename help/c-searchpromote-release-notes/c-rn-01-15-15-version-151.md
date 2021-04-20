---
description: Search&amp;Notas de la versión de Promote 15.1.1.
solution: Target
title: Search&amp;Promote 15.1.1 Notas de la versión (15/01/2015)
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 16%

---


# Notas de la versión 15.1.1 de Search&amp;Promote (15/01/2015){#search-promote-release-notes}

## Nueva función {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Anteriormente, en las reglas de búsqueda guiada, siempre se aplicaban ámbitos de la lingüística como la lematización, los sinónimos, etc., a las palabras clave. Ahora puede desactivar esta expansión para que la palabra clave se utilice tal como es.

   Cuando desee aplicar condiciones de déclencheur a una regla de negocio, en [!DNL Advanced Rule Builder], debajo de **[!UICONTROL If any/all of the following conditions are met]**, en la primera lista desplegable, seleccione **[!UICONTROL keyword]** y, a continuación, seleccione el nuevo operador **[!UICONTROL equal exact]** en la segunda lista desplegable.

   Consulte [Acerca de las reglas comerciales](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Correcciones y mejoras {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] y ya  [!DNL Advanced Rule Builder] no trunca el valor del campo MDI (Merchandising Document ID).
* No se han corregido los errores de indexación relacionados con RBTA.
* La edición de una regla comercial existente que tiene el estado &quot;aprobada&quot; ahora anula el estado &quot;aprobado&quot;. Debe utilizar [!DNL Advanced Rule Builder] para volver a comprobar la opción **[!UICONTROL Approved]** y luego guardar la regla como de costumbre. Si no vuelve a aprobar una regla editada, el estado de la regla se establece automáticamente a WIP (Work In Progress) en la página [!DNL Business Rules].
* Ahora hay disponible una nueva opción **[!UICONTROL Advanced Search]** en la página [!DNL Business Rules] para mejorar el filtrado de reglas.
* Se ha agregado la condición **[!UICONTROL contains word]** a los déclencheur de reglas en [!DNL Query Cleaning], [!DNL Pre-Search Rules], [!DNL Post Search Rules] y [!DNL Business Rules] para permitirle especificar fácilmente separaciones de palabras.
* Se han realizado mejoras en las notas de reglas comerciales, como cuando se ve una regla, ahora se puede recuperar el historial de notas para esa regla. Además, las notas ahora están registradas en **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**.
* Las consultas con valores `sp_i` distintos de cero ya no se ejecutan mediante el redirector [!DNL Adobe Analytics] .

   Consulte la fila 15 de la tabla en [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

