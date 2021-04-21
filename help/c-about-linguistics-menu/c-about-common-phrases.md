---
description: Puede definir frases comunes que se utilizan en el sitio web para que, cuando un cliente introduzca una consulta de búsqueda, no necesite escribir comillas alrededor de ninguna de las frases que haya definido.
solution: Target
title: Acerca de las frases comunes
topic-legacy: Linguistics,Site search and merchandising
uuid: 0f980a22-d826-4476-97de-0e9c14549bc8
exl-id: 72305fcd-8f9a-4ce2-b416-aa1b58486312
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 1%

---

# Acerca de las frases comunes{#about-common-phrases}

Puede definir frases comunes que se utilizan en el sitio web para que, cuando un cliente introduzca una consulta de búsqueda, no necesite escribir comillas alrededor de ninguna de las frases que haya definido.

## Uso de frases comunes {#concept_4946E53586DF492EAEB1B7F757FD440F}

>[!NOTE]
>
>La función Frase común no aparece en la interfaz de usuario porque no está activada de forma predeterminada. Póngase en contacto con el soporte técnico para activar esta función para su uso.

Las frases comunes son una colección de frases de varias palabras que se reconocen durante la búsqueda de un cliente. Trata las frases como un grupo combinado de palabras en lugar de palabras individuales. Cuando un cliente introduce una consulta de búsqueda en su sitio web, puede identificar frases rodeando los términos con comillas dobles, como &quot;Océano Pacífico&quot;. Sin embargo, cuando se agregan grupos de frases comunes, los pasos de cotización se realizan automáticamente para el cliente, ya que encuentra frases coincidentes en la consulta de búsqueda.

Por ejemplo, supongamos que un cliente del sitio web introduce la siguiente consulta de búsqueda:

`hotels near the pacific ocean`

Sin la adición de comillas alrededor de `pacific ocean`, la búsqueda del cliente devuelve resultados para hoteles cerca de cualquier océano en el mundo, que no es lo que el cliente pretendía.

Sin embargo, cuando agrega la frase común &quot;Océano Pacífico&quot;, su consulta de búsqueda se convierte automáticamente en la siguiente:

`hotels near the "pacific ocean"`

El uso de frases comunes no impide que sus clientes usen explícitamente comillas alrededor de frases de palabras. En su lugar, simplemente agrega comillas, cuando esas frases definidas se encuentran en su consulta de búsqueda.

Esta expansión de consulta de búsqueda se aplica a los parámetros CGI de búsqueda back-end `sp_q` y `sp_q_#`,

Consulte las filas de la tabla 25, 26 y 32 en [Parámetros CGI de búsqueda back-end](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

## Adición de un grupo de frases comunes {#task_35C84FABCD9042C5B48C5C788B752871}

Puede agregar Grupos de frases comunes para garantizar que las consultas de búsqueda devuelvan de forma precisa páginas web que tengan todas las palabras, en el orden y la proximidad exactos, que escribió un cliente.

A medida que agrega Grupos de frases comunes, puede usar la función Buscar en la página principal del Grupo de frases comunes. La función Buscar permite buscar una frase existente y averiguar en qué grupo reside.

Consulte [Búsqueda de grupos que contienen palabras específicas en una frase](../c-about-linguistics-menu/c-about-common-phrases.md#task_20714969274740A7BB4DC71E705EA15E).

**Para agregar un grupo de frases comunes**

1. En el menú del producto, haga clic en **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. En la página [!DNL Common Phrases Groups], haga clic en **Agregar grupo de frases**.
1. En la página [!DNL Add Common Phrase Group], configure las opciones que desee y agregue todas las frases que conforman el grupo.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nombre del grupo </p> </td> 
      <td colname="col2"> <p>Requerido. </p> <p>Nombre exclusivo del grupo de frases comunes. </p> <p>Si edita un grupo de frases comunes más adelante, tenga en cuenta que no puede cambiar el nombre del grupo. Para cambiar el nombre del grupo, utilice la función <span class="uicontrol"> Cambiar nombre</span>. </p> <p>Consulte <a href="../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB" format="dita" scope="local"> Cambio del nombre de un grupo de frases comunes</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Notas </p> </td> 
      <td colname="col2"> <p>Opcional. </p> <p>Agregue información relacionada con el grupo de frases comunes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Frases </p> </td> 
      <td colname="col2"> <p>Requerido. </p> <p>Permite especificar una frase de hasta cinco palabras. Para ajustar la configuración máxima de palabras, póngase en contacto con el soporte técnico. </p> <p>Cada frase que escriba debe ser única dentro de cualquier grupo de frases comunes. </p> <p>Utilice los iconos más (+) y menos (-) de la columna Acción para añadir la frase introducida o para eliminar una frase. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic en **Agregar**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Prueba de una frase común {#task_A0C344E051CA45A9A0588242F9DA675D}

Si ha seleccionado campos de metadatos para asociarlos a un grupo de frases, puede probar la expansión de una frase en particular.

Al probar la expansión de una frase, se busca una frase exacta en los campos de metadatos asociados al grupo de frases. La frase se busca como si estuviera entre comillas. Todos los demás campos de metadatos buscan únicamente las palabras de la frase, sin comillas. Por ejemplo, supongamos que ha probado la frase `audi TT`. Los resultados devueltos podrían aparecer de la siguiente manera:

`title|body|field3:"Audi TT" url|desc|keys|target|alt:Audi TT`

**Para probar una frase común**

1. En el menú del producto, haga clic en **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. En la página [!DNL Common Phrases Groups], en el campo de texto **Probar frase que contiene**, introduzca la frase cuya expansión de metadatos desee probar.
1. Haga clic **[!UICONTROL Test]**.

   Los resultados de la expansión se muestran en el cuadro de texto.
1. (Opcional) Arrastre la esquina inferior derecha del cuadro de texto para expandir la zona de visualización.

## Búsqueda de grupos que contienen palabras específicas en una frase {#task_20714969274740A7BB4DC71E705EA15E}

Puede utilizar [!DNL Find] para buscar palabras específicas en una frase entre todos los grupos existentes que haya agregado.

Cuando utiliza Buscar, localiza lo siguiente:

* Donde se encuentra exactamente la misma frase entre todos los grupos.
* Cualquiera de las palabras de la frase entre todos los grupos, independientemente del orden de palabras y la proximidad de la frase.

Consulte también [Edición de un grupo de frases comunes](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61).

**Buscar grupos que contienen palabras concretas en una frase**

1. En el menú del producto, haga clic en **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. En la página [!DNL Common Phrases Groups], en el campo de texto **[!UICONTROL Find groups with phrases that contain]** introduzca una frase.
1. Haga clic **[!UICONTROL Find]**.

   Los resultados se muestran en el cuadro de texto.
1. (Opcional) Realice una o más de las siguientes acciones:

   * Arrastre la esquina inferior derecha del cuadro de texto para expandir la zona de visualización.
   * En la ventana de resultados, haga clic en una frase hipervinculada para abrir la página Editar grupo de frases comunes del grupo asociado.

## Edición de un grupo de frases comunes {#task_5CAC3A133C5342EEAFE55A7EABCBCD61}

Puede editar los campos, notas y frases existentes de un grupo de frases comunes que haya agregado. Sin embargo, para editar el nombre del grupo, debe utilizar la función [!DNL Rename].

Consulte también [Cambio del nombre de un grupo de frases comunes](../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB).

**Para editar un grupo de frases comunes**

1. En el menú del producto, haga clic en **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. En la página [!DNL Common Phrases Groups], haga clic en **[!UICONTROL Edit]** a la derecha del nombre de un grupo.
1. En la página [!DNL Edit Common Phrase Group], configure las opciones que desee.

   Consulte la tabla de opciones en [Añadir un grupo de frases comunes](../c-about-linguistics-menu/c-about-common-phrases.md#task_35C84FABCD9042C5B48C5C788B752871).
1. Haga clic en **Guardar cambios**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cambio del nombre de un grupo de frases comunes {#task_168E07C59C0F40989D43E7010EFF22EB}

Puede cambiar el nombre de un grupo de frases comunes existente. Sin embargo, si desea cambiar los campos, notas y frases existentes de un grupo de frases común, debe utilizar la función [!DNL Edit].

Consulte [Edición de un grupo de frases comunes](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61) .

**Cambio del nombre de un grupo de frases comunes**

1. En el menú del producto, haga clic en **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. En la página [!DNL Common Phrases Groups], haga clic en **[!UICONTROL Rename]** a la derecha del nombre de un grupo.
1. En la página [!DNL Rename Common Phrase Group], en el campo de texto **[!UICONTROL Group Name]**, introduzca el nuevo nombre del grupo.
1. Haga clic en **Cambiar nombre**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de un grupo de frases común {#task_4106D282A2ED4A27B09EE5A8CAAEDA36}

Puede eliminar cualquier grupo de frases comunes que haya agregado. Si elimina un grupo por error, puede usar [!DNL History] para restaurar el grupo.

Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

**Eliminación de un grupo de frases comunes**

1. En el menú del producto, haga clic en **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. En la página [!DNL Common Phrases Groups], haga clic en **[!UICONTROL Delete]** a la derecha del nombre de un grupo.
1. En la página [!DNL Delete Common Phrase Group], haga clic en **[!UICONTROL Delete]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
