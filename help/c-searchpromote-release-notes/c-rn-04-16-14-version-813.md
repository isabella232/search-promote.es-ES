---
description: Search&amp;Notas de la versión de Promote 8.13.0.
solution: Target
title: Search&amp;Promote 8.13.0 Notas de la versión (16/04/2014)
topic: Notas de la versión, búsqueda de sitios y comercialización
uuid: b3524992-ff00-4a7c-a404-078242456734
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 56%

---


# Notas de la versión de Search&amp;Promote 8.13.0 (16/04/2014){#search-promote-release-notes}

| Nueva función y mejora | Descripción |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facetas dinámicas con compatibilidad para coincidencias de tablas completas | Algunos clientes tenían muchos atributos de &quot;nivel SKU&quot; que querían seleccionar y mostrar mediante Facetas dinámicas. Si es su caso, ahora tiene la opción de relacionar cada campo de faceta dinámica con al menos un nombre de tabla en una configuración de cuenta estática. Esas relaciones de tablas pueden aplicarse posteriormente, en el momento de las búsquedas, para cualquier campo de faceta dinámica involucrado en la búsqueda. Consulte [Acerca de los hechos dinámicos](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899). |

**Correcciones**

* Se ha cambiado el campo de descripción de la vista de datos para que utilice la etiqueta `<search-display-field>` en lugar de `<search-description>`.
* Se agregó una función al conector de índice para convertir la concatenación de dos o más campos en clave principal.
* Se cambió el script AttributeLoader-Regen-Enabled `attributeloader-regen.pl` a valores sin codificación HTML.
* Se hizo coincidir el tratamiento de espacios en blanco de índice-tiempo y búsqueda-tiempo para consultas de &quot;búsqueda por intervalo&quot;.
* Al agregar una regla comercial en ocasiones se producía un error cuando Facetas dinámicas estaba habilitado.

   Consulte [Acerca de las reglas comerciales](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Un error de Javascript impedía añadir o editar una definición en **Settings** > **SPIN** > **IndexConnector**.
* Después de guardar una regla de negocio, parecía que cuando la hora se seleccionaba durante la creación de la regla de negocio, la zona horaria GMT era por defecto. Parecía que solo después de guardarla se activaba la zona horaria de la cuenta.

   Consulte [Acerca de las reglas comerciales](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* La clasificación de reglas comerciales de ensayo no estaba funcionando correctamente.

   Consulte [Acerca de las reglas comerciales](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Se mejoraron los informes del rendimiento de búsqueda para facilitarle la posibilidad de programar informes para enviar por correo electrónico.
* La programación fija de la regla comercial cambiaba automáticamente a Daylight Saving Time.

   Consulte [Acerca de las reglas comerciales](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Si se definieron un gran número de campos de facetas dinámicas, los usuarios experimentaron tiempos de respuesta de búsqueda de núcleo lentos.
* Ocurrían errores de índice de intervalo falso.
* Se ha interrumpido el acceso a Dynamic Media Classic en centros de datos no norteamericanos.
* La función de validación SPIN XPath devolvía un falso positivo.

* Después de habilitar/deshabilitar SPIN, se redirigía al usuario a la página de inicio de sesión de centro del miembro.

