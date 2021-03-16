---
description: Puede utilizar la actualización vertical para actualizar rápidamente partes del índice sin tener que procesar grandes cantidades de datos.
solution: Target
subtopic: Vertical Update
title: Acerca de la actualización vertical
topic: Índice,Búsqueda de sitios y comercialización
uuid: ded09e89-5a52-4e8c-a6f7-3e25b4191183
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---


# Acerca de la actualización vertical{#about-vertical-update}

Puede utilizar la actualización vertical para actualizar rápidamente partes del índice sin tener que procesar grandes cantidades de datos.

## Uso de la actualización vertical {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

Un índice vertical tarda solo segundos en funcionar y es útil en sitios web de comercio electrónico de gran capacidad que pueden tardar muchas horas en indexarse de forma completa o incremental.

Cuando se genera un índice vertical, se muestra la información de estado, como la hora de inicio, el tiempo transcurrido y los errores durante el proceso de indexación.

Puede detener o reiniciar el proceso de indexación vertical en cualquier momento.

Aunque el nuevo índice vertical actualiza el sitio web activo, los clientes pueden seguir buscando en el sitio con el índice actual.

>[!NOTE]
>
>Esta función no está habilitada en [!DNL Adobe Search&Promote] de forma predeterminada. Póngase en contacto con el soporte técnico para activar la función para su uso.

Las actualizaciones verticales están diseñadas específicamente para utilizarse en cuentas de [!DNL Adobe Search&Promote] estilo eCommerce que utilicen IndexConnector para proporcionar el contenido para el índice de búsqueda. El caso de uso típico es uno en el que el índice [!DNL Adobe Search&Promote] representa un catálogo de productos en el que se pueden realizar búsquedas y existe la necesidad de poder actualizar rápidamente los valores que cambian con frecuencia, como inventario disponible, disponibilidad y/o precio. Una actualización vertical es algo similar a un índice incremental, excepto que solo actualiza partes de cada documento, mientras que un índice incremental reemplaza documentos completos con nuevas versiones.

El término &quot;Actualización vertical&quot; hace referencia a la noción de que un índice [!DNL Adobe Search&Promote] puede aparecer como una tabla en columnas, con cada columna correspondiente a una definición de campo de metadatos [!DNL Adobe Search&Promote] y cada fila correspondiente a un documento. El proceso de actualización vertical reemplaza una o más columnas sin necesidad de modificar el contenido de las otras columnas.

Cuando la fuente principal del contenido, una fuente IndexConnector, contiene todos los elementos de datos necesarios para crear el índice, la fuente Vertical Update es un subconjunto de la fuente principal, que utiliza el mismo &quot;esquema&quot; de IndexConnector para definir los elementos de datos, pero que contiene *solo* los elementos de datos que deben actualizarse.

Como mínimo, la fuente de actualización vertical debe contener el elemento &quot;clave principal&quot; (tal y como se identifica con la casilla de verificación **Clave principal** en la configuración de IndexConnector) y al menos un elemento de datos que se va a actualizar.

Por ejemplo, una fuente IndexConnector principal puede tener el aspecto siguiente (pero normalmente con muchos elementos de datos más):

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <title><![CDATA[Title for product 123]]></title>
  <description><![CDATA[Description for product 123.]]></description>
  <price>3.99</price>
  <link><![CDATA[https://www.somewhere.com/products/123]]></link>
  <image><![CDATA[https://www.somewher.com/images/products/123.jpg]]></image>
  <label><![CDATA[PROD123]]></label>
  <inventory>100</inventory>
  <brand><![CDATA[brand123]]></brand>
  ...
</product>
<product>
...
</product>
</products>
```

Un requisito es poder actualizar rápidamente solo los valores `<price>` y `<inventory>`, ya que estos valores pueden cambiar rápidamente en el sitio del cliente. Una fuente de actualización vertical podría tener el siguiente aspecto:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <price>3.50</price>
  <inventory>90</inventory>
</product>
<product>
...
</product>
</products>
```

Esta información se almacena generalmente en un archivo independiente en el servidor del cliente, y la configuración &quot;Ruta de archivo vertical&quot; de IndexConnector apunta a este archivo. El proceso de actualización vertical lee este nuevo contenido y actualiza el índice [!DNL Adobe Search&Promote] existente, actualizando solo los valores de `<price>` y `<inventory>`, en este caso. Las búsquedas posteriores devuelven el contenido recién actualizado.

>[!NOTE]
En este ejemplo, los campos de metadatos `<price>` y `<inventory>` deberán haberse definido con la opción **Campo de actualización vertical** activada.

Consulte también [Acerca del control remoto para la indexación](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F) y [Añadir un nuevo campo de metaetiqueta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Configuración de una actualización vertical de un sitio web provisional {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

Puede configurar qué fuentes de conector de índice desea incluir en la actualización vertical especificando direcciones URL.

**Para configurar una actualización vertical de un sitio web provisional**

1. En el menú del producto, haga clic en **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Configuration]**.
1. En la página **[!UICONTROL Vertical Update Configuration]**, en el campo Actualizar direcciones URL , especifique las direcciones URL de las páginas que desea indexar.

   El robot de búsqueda solo actualiza los documentos identificados en los orígenes especificados del conector de índice.

   Este campo debe contener direcciones URL del conector de índice solo como en el siguiente ejemplo:

   `index:product_catalog`.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Visualización del registro de actualización vertical de un sitio web activo o provisional {#task_E668E1F1240C476DAA1CA783DC728232}

Cuando se completa una actualización vertical activa o una actualización vertical escalonada, puede ver su registro asociado para solucionar cualquier error que se pueda haber producido.

No puede exportar archivos de registro de actualización vertical ni guardarlos. El archivo de registro permanece disponible para su visualización hasta que se produzca el siguiente índice.

**Para ver el registro de actualización vertical de un sitio web activo o provisional**

1. En el menú del producto, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Live Log]**.

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Staged Log]**.

1. En la página de registro, en la parte superior o inferior, realice una de las acciones siguientes:

   * Utilice las opciones de navegación **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** o **[!UICONTROL Go to line]** para desplazarse por el registro.

   * Utilice las opciones de visualización **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** o **[!UICONTROL Show]** para restringir lo que ve.

