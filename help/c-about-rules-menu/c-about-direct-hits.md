---
description: Las visitas directas permiten redirigir a un cliente a una dirección URL especificada cuando el cliente busca un término coincidente. Este tipo de funcionalidad le permite mejorar la navegación de la búsqueda del sitio web.
solution: Target
title: Acerca de las visitas directas
topic: Rules,Site search and merchandising
uuid: 374d63c8-2b82-4165-b543-05b587757baa
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 1%

---


# Acerca de las visitas directas{#about-direct-hits}

Las visitas directas permiten redirigir a un cliente a una dirección URL especificada cuando el cliente busca un término coincidente. Este tipo de funcionalidad le permite mejorar la navegación de la búsqueda del sitio web.

## Uso de visitas directas {#concept_C5EE074A19FD4D5B8DD21DB575E35565}

Las visitas directas constan de dos elementos principales: la dirección URL del sitio web y uno o varios términos de búsqueda delimitados por comas. Las visitas directas se especifican de la siguiente manera:

```
    website_URL: term
    website_URL: term, term, term
```

Por ejemplo, supongamos que tiene un sitio web corporativo con una página que especifica todos los términos y condiciones. Cuando un cliente busca sus términos y condiciones, en lugar de mostrar los resultados, puede redirigir al cliente a la página de términos y condiciones.

```
    https://www.mycompany.com/policies.asp?article=terms: terms and conditions, terms, conditions, security
    https://www.mycompany.com/press/news.asp: press releases, press
```

Si el término de consulta no coincide con ninguna visita directa, los resultados de búsqueda se devuelven de la manera habitual.

## Configuración de visitas directas {#task_64DFB8C554874C699FCC0C2F26C3669F}

Puede especificar términos de búsqueda que redirijan un explorador web a un URI en lugar de devolver resultados de búsqueda.

<!-- 

t_configuring_direct_hits.xml

 -->

Se permiten líneas en blanco y líneas de comentarios que empiecen por un carácter &#39;#&#39; (hash).

**Para configurar las visitas directas**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. En el campo [!DNL Direct Hits], introduzca la dirección URL del sitio web y uno o varios términos de búsqueda delimitados por comas.
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Prueba de visitas directas {#task_1E2EA833BF90423AA0DD8C5BBFE77445}

Antes de insertar las reglas de visitas directas en directo, puede probar las visitas directas introduciendo un término.

<!-- 

t_testing_direct_hits.xml

 -->

Si prueba un término que no esté cubierto por una regla de visita directa, se muestra un mensaje que le informa. En este caso, si la regla de visitas directas se encuentra activa en el sitio web, los resultados de búsqueda se devolverán de la forma habitual. Si prueba un término que esté cubierto por una regla de visita directa, se muestra un mensaje que le permite saber que se ha producido una redirección a la dirección URL especificada.

**Para probar las visitas directas**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. En el campo [!DNL Test Direct Hits], introduzca un término de búsqueda y haga clic en **[!UICONTROL Test]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

