---
description: Search&amp;Notas de la versión de Promote 8.9.
solution: Target
title: Search&amp;Notas de la versión de Promote 8.9 (19/07/2012)
topic-legacy: Release Notes,Site search and merchandising
uuid: 3853c75d-19ed-4e36-9e81-dcbffe5f5b0c
exl-id: d61bf0ee-60a9-4c89-8381-5514ba85cb99
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 66%

---

# Notas de la versión de Search&amp;Promote 8.9 (19/07/2012){#search-promote-release-notes}

**Nuevas funciones**

* Mejoras de la administración de metadatos - Definición dinámica de metadatos desde las fuentes de los clientes

   Cree un esquema para volver a configurar dinámicamente su cuenta Search&amp;Promote basada en definiciones de metadatos proporcionados por el cliente.
* Indexación de mejoras de rendimiento - Index Loader

   Index Loader es una forma completamente nueva de importar contenido XML directamente al índice Search&amp;Promote. Es una subdivisión de la funcionalidad de conexión del índice existente que está diseñada para importar rápidamente nuestros archivos de fuentes estándar XML.

**Correcciones y mejoras**

* Se ha añadido asistencia para cambiar la opción ordenar mediante una regla comercial.
* En la etiqueta del sistema de ayuda `<search-description>` se muestra el cuerpo cuando la metaetiqueta de la descripción está vacía.
* Se ha añadido la capacidad de hacer un seguimiento de visitas de tablas aplicables para los resultados que se añadieron mediante acciones basadas en resultados.
* Se ha añadido asistencia para enviar parámetros de consulta a través de anuncios
* Al arrastrar, se puede omitir en algunos casos una operación final mirror_account.
* Las direcciones URL de Adobe Analytics no incluyen argumentos CGI y el código de Search&amp;Promote que realiza búsquedas de Adobe Analytics necesitaba eliminar de forma similar argumentos CGI de claves URL.
* Las reglas de reescritura desaparecieron de forma intermitente de la interfaz de usuario tras insertarlas para que se mantuvieran activas.
* Las cuentas de Search&amp;Promote con la configuración ¿Quiso decir? que se configuraron para realizar sugerencias debido a resultados bajos pueden tener resultados intermitentes.
* La salida de la prueba de la regla de reescritura no tenía saltos de línea.
* Las página de reglas de búsqueda URL y la página de reglas almacenadas de listas arrastradas URL apuntaban hacia la página de historial equivocada.
* Al hacer clic en Editar en algunos banners no se mostró la página Editar.
* La nueva clasificación del código de actualización podría realizarse de un modo extraordinariamente lento.
* Al eliminar o insertar un elemento de aspecto no funcionó si el nombre del aspecto utilizaba mayúsculas y minúsculas a la vez.
