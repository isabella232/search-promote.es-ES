---
description: 'null'
seo-description: 'null'
seo-title: Notas de revisión de Search&Promote 15.1.1 (15/01/2015)
solution: Target
title: Notas de revisión de Search&Promote 15.1.1 (15/01/2015)
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 17%

---


# Notas de la versión de Search&amp;Promote 15.1.1 (15/01/2015){#search-promote-release-notes}

## Nueva función {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Anteriormente, en las reglas de búsqueda guiada, siempre se aplicaban ámbitos de la lingüística como la lematización, los sinónimos, etc., a las palabras clave. Ahora puede desactivar esta expansión para que la palabra clave se utilice tal como es.

   Cuando desee aplicar condiciones de activación a una regla comercial, en la [!DNL Advanced Rule Builder], después de **[!UICONTROL If any/all of the following conditions are met]**, en la primera lista desplegable, seleccione **[!UICONTROL keyword]** y, a continuación, seleccione el nuevo operador **[!UICONTROL equal exact]** en la segunda lista desplegable.

   Consulte [Acerca de las reglas comerciales](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Correcciones y mejoras {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] y  [!DNL Advanced Rule Builder] ya no trunca el valor del campo MDI (ID de Documento de comercialización).
* No se han corregido los errores de indexación relacionados con RBTA.
* Editar una regla comercial existente que tenga el estado &quot;aprobado&quot; ahora anula el estado &quot;aprobado&quot;. Debe utilizar [!DNL Advanced Rule Builder] para volver a comprobar la opción **[!UICONTROL Approved]** y luego guardar la regla como de costumbre. Si no vuelve a aprobar una regla editada, el estado de la regla se establece automáticamente en WIP (trabajo en curso) en la página [!DNL Business Rules].
* Ahora hay una nueva opción **[!UICONTROL Advanced Search]** disponible en la página [!DNL Business Rules] para mejorar el filtrado de reglas.
* Se añadió la condición **[!UICONTROL contains word]** a los activadores de reglas en [!DNL Query Cleaning], [!DNL Pre-Search Rules], [!DNL Post Search Rules] y [!DNL Business Rules] para permitirle especificar fácilmente los saltos de palabras.
* Las mejoras realizadas en las notas de reglas comerciales, como cuando se vista una regla, ahora puede recuperar el historial de notas de esa regla. Además, las notas ahora inician sesión en **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**.
* Las consultas con valores `sp_i` distintos de cero ya no se ejecutan mediante el redirector [!DNL Adobe Analytics].

   Consulte la fila 15 de la tabla en [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

