---
description: 'null'
seo-description: 'null'
seo-title: Notas de revisión de Search&Promote 8.13.0 (16/04/2014)
solution: Target
title: Notas de revisión de Search&Promote 8.13.0 (16/04/2014)
topic: Release Notes,Site search and merchandising
uuid: b3524992-ff00-4a7c-a404-078242456734
translation-type: tm+mt
source-git-commit: 9d5ac055d665b39d09b28063179d74a389d7f830

---


# Search&amp;Promote 8.13.0 Release Notes (04/16/2014){#search-promote-release-notes}

| Nuevas funciones y mejoras | Descripción |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facetas dinámicas con compatibilidad para coincidencias de tablas completas | Algunos clientes tenían muchos atributos de &quot;nivel SKU&quot; que querían seleccionar y mostrar mediante Facetas dinámicas. Si es su caso, ahora tiene la opción de relacionar cada campo de faceta dinámica con al menos un nombre de tabla en una configuración de cuenta estática. Esas relaciones de tablas pueden aplicarse posteriormente, en el momento de las búsquedas, para cualquier campo de faceta dinámica involucrado en la búsqueda. Consulte [Acerca de los hechos](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)dinámicos. |

**Correcciones**

* Changed the data view description field to use the tag `<search-display-field>` instead of the `<search-description>`.
* Se agregó una función al conector de índice para convertir la concatenación de dos o más campos en clave principal.
* Se cambió el script AttributeLoader-Regen-Enabled `attributeloader-regen.pl` a valores sin codificación HTML.
* Se hizo coincidir el tratamiento de espacios en blanco de índice-tiempo y búsqueda-tiempo para consultas de &quot;búsqueda por intervalo&quot;.
* Al agregar una regla comercial en ocasiones se producía un error cuando Facetas dinámicas estaba habilitado.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* A Javascript error prevented adding or editing a definition in **Settings** > **SPIN** > **IndexConnector**.
* Después de guardar una regla comercial, parecía que cuando se seleccionaba la hora durante la creación de la regla comercial, se establecía de forma predeterminada en la zona horaria GMT. Parecía que solo después de guardarla se activaba la zona horaria de la cuenta.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* La clasificación de reglas comerciales de ensayo no estaba funcionando correctamente.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Se mejoraron los informes del rendimiento de búsqueda para facilitarle la posibilidad de programar informes para enviar por correo electrónico.
* La programación fija de la regla comercial cambiaba automáticamente a Daylight Saving Time.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Si se definía un gran número de campos de facetas dinámicas, los usuarios experimentaban tiempos de respuesta de búsqueda de núcleo lentos.
* Ocurrían errores de índice de intervalo falso.
* El acceso a Dynamic Media Classic en los centros de datos no norteamericanos estaba dañado.
* La función de validación SPIN XPath devolvía un falso positivo.

* Después de habilitar/deshabilitar SPIN, se redirigía al usuario a la página de inicio de sesión de centro del miembro.

