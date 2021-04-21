---
description: Utilice las reglas de limpieza de consultas para analizar y modificar la consulta entrante.
solution: Target
title: Acerca de las reglas de limpieza de consultas
topic-legacy: Rules,Site search and merchandising
uuid: 683af81f-f7c0-45f8-9212-e5e7cb82ccca
exl-id: 22ebca58-7687-4c8c-9ac1-bacb321065f3
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1596'
ht-degree: 1%

---

# Acerca de las reglas de limpieza de consultas{#about-query-cleaning-rules}

Utilice las reglas de limpieza de consultas para analizar y modificar la consulta entrante.

## Uso de reglas de limpieza de consultas {#concept_17F3CDDC3C8A4128AF092A82B777B86C}

Esta función se utiliza a menudo cuando desea modificar el comportamiento de búsqueda/comercialización del sitio. Por ejemplo, podría cambiar una búsqueda en blanco por una palabra clave popular en lugar de una búsqueda &quot;*&quot;, lo que promovería un producto popular. También puede utilizar reglas de limpieza de consultas para realizar una visita directa, donde puede redirigir a una dirección URL. Esto puede resultar especialmente útil cuando detecta que alguien está buscando un SKU de producto y desea omitir la búsqueda y redirigir a la página de ese producto. La limpieza de consultas también puede extraer la consulta y establecer variables personalizadas que se pueden utilizar en pasos posteriores del flujo de procesamiento. Las reglas de limpieza de consultas se ejecutan en secuencia para cada consulta. Para modificar el orden de las reglas, puede usar arrastrar y soltar. El orden real no cambia hasta que lo guarda.

Las reglas de limpieza de consultas de un módulo de limpieza de consultas se examinan para determinar si alguno de los parámetros de consulta debe modificarse o si se debe configurar alguna variable personalizada. Cada regla de limpieza de consultas consta de dos elementos principales: las acciones de la regla y las condiciones opcionales. Se puede especificar un número ilimitado de reglas y condiciones. El orden de estas reglas es importante, ya que la búsqueda/comercialización del sitio recorre en bucle el conjunto de reglas regla por regla. Cuando coinciden las condiciones de una regla, se realizan todas las acciones asociadas.

Una vez finalizada la limpieza de la consulta, se utilizan los parámetros CGI resultantes en adelante. Todas las variables personalizadas que se hayan configurado estarán disponibles para su uso en etapas posteriores del flujo de procesamiento. De forma predeterminada, el sistema elimina automáticamente los espacios en blanco iniciales y finales del término de consulta.

## Acerca de las condiciones de limpieza de consultas {#section_BF6F25F94FED4DDEA8600D921EA43A66}

Las condiciones son opcionales. Si decide que las acciones se especifican para cada consulta, las acciones siempre se realizan. Las condiciones se pueden basar en cualquier parámetro de consulta CGI, cookie existente o variable personalizada que haya establecido una regla anterior. Se considera una &quot;práctica recomendada&quot; que la primera regla de limpieza de consultas se ejecute para cada consulta, donde define e inicializa todas las variables personalizadas que planea utilizar.

## Acerca de las acciones de limpieza de consultas {#section_78F74A9B48DE484191CDA95F5B4E7154}

Se ejercen todas las acciones dentro de una regla de limpieza de consultas que tengan condiciones coincidentes. Las acciones suelen consistir en una operación, los datos sobre los que realizar la operación y el valor que se va a utilizar.

Consulte la tabla de opciones en [Adición de una regla de limpieza de consulta](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).

## Acerca de las redirecciones {#section_597481E6194440C0A7B9E6FC901A81C0}

La interfaz Direct-Hits permite definir un conjunto de redirecciones en función del término de consulta entrante. Las redirecciones dentro de la Limpieza de consultas amplían esta idea. Sin embargo, las redirecciones le ofrecen una granularidad más precisa sobre cuándo se realiza una redirección mediante condiciones específicas y le permiten redireccionar a una URL dinámica en lugar de a una URL estática. Cuando selecciona la acción de redireccionamiento, la fila se actualiza para tener un cuadro de texto donde especifique la dirección URL a la que desea redirigir. En la dirección URL, puede especificar variables o parámetros que desee sustituir mediante su inclusión entre corchetes dobles. Las variables personalizadas tienen mayor prioridad que los parámetros CGI en la sustitución.

## Ejemplos {#section_DB5047CC38FB4A57B15CAAF9848073E3}

Supongamos que tiene una tienda de ropa con un sitio web. Si el usuario hace clic en Buscar sin ningún término de búsqueda, quiere devolver una búsqueda contra los vaqueros, porque es por lo que es conocido internacionalmente. También desea analizar el término de consulta de un sexo para poder crear una regla de búsqueda previa más adelante, en función de la variable personalizada que utiliza una plantilla de presentación diferente para cada sexo.

```
On condition: 
  query q equal 
Perform the following actions: 
  Set query parameter q to value jeans 
 
On condition: 
  Query q matches regular expression wom[e|a]n[s]|girl[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value female 
 
On condition: 
  Query q matches regular expression men[s]|boy[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value male
```

MegaElectronic es una gran tienda electrónica. Al analizar sus datos de búsqueda, MegaElectronic ha notado que muchos de sus clientes expertos a menudo buscan un producto utilizando el SKU del producto, en lugar de devolver un resultado de búsqueda para el único producto, MegaElectronic desea redirigir a la página web asociada con ese SKU.

```
On condition: 
  query q matches regular expression ^\D\D\D-\d\d\d\d$ 
Perform the following actions: 
  redirect to https://www.megaelectronic.com/?sku={{q}}
```

## Adición de una regla de limpieza de consulta {#task_47F43988D3D9485F8AE1DFDA7E00BF54}

Puede definir reglas que limpien o editen la consulta de búsqueda entrante de un cliente.

Solo puede seleccionar plantillas que existan actualmente. Si no tiene plantillas, primero debe definirlas.

Consulte [Acerca de las plantillas](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Para agregar una regla de limpieza de consultas**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. En la página [!DNL Query Cleaning Rules], haga clic en **[!UICONTROL Add New Rule]**.
1. En el campo [!DNL Name], escriba el nombre de la nueva regla de limpieza de consultas.
1. En la página [!DNL Add Query Cleaning Rule], utilice las listas desplegables y los campos de texto para crear la consulta.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Cookie </p> </td> 
      <td colname="col2"> <p>Una cookie HTTP. Puede definir condiciones basadas en cookies asociadas con su dominio. O bien, puede establecer una cookie que se escriba con los resultados de búsqueda salientes. El nombre y los valores de las cookies deben tener codificación Uniform Resource Identifier . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable personalizada </p> </td> 
      <td colname="col2"> <p>Variable definida por el usuario. Agregue, elimine o establezca una cantidad ilimitada de variables definidas por el usuario. Aquí puede hacer referencia a cualquier variable definida por el usuario dentro de Reglas de búsqueda previa y Reglas de búsqueda posterior. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable de sistema </p> </td> 
      <td colname="col2"> <p>Variables de solo lectura establecidas por el sistema interno que puede comprobar. Se admiten las siguientes variables del sistema: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostname  </span> <p>Nombre del host del servidor. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri  </span> <p>El URI solicitado sin la cadena de consulta. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args  </span> <p>Toda la cadena de consulta. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> entorno </span> <p>"Etapa" o "Activo" dependiendo de si la consulta entrante se envió al entorno en escena o activo. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>Dirección URL de la que provino el cliente. </p> </li> 
          <li id="li_6FEE352DB7A842FCB2EBE1398AD03666"> <span class="uicontrol"> agente de usuario  </span> <p>La cadena "user-agent" del explorador del cliente. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetro de consulta </p> </td> 
      <td colname="col2"> <p>Parámetros CGI pasados a la consulta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetro de backend </p> </td> 
      <td colname="col2"> <p>Los parámetros de consulta entrantes finalmente se traducen en parámetros back-end que se utilizan para realizar la búsqueda. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parámetros CGI de búsqueda back-end </a>. </p> <p>Los parámetros back-end no se muestran en los elementos de navegación. Como resultado, puede ocultar cualquier parámetro adicional que desee aplicar a una búsqueda de sus clientes. Las acciones sobre parámetros de servidor son enlaces tardíos; es decir, se aplican justo antes de que se envíe la búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Faceta </p> </td> 
      <td colname="col2"> <p>Parámetros CGI especiales asociados a una faceta determinada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Clasificación </p> </td> 
      <td colname="col2"> <p>Permite especificar la regla de clasificación que se utilizará en la búsqueda. Esta opción solo aparece cuando tiene algunos campos de clasificación y reglas de clasificación definidos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tienda </p> </td> 
      <td colname="col2"> <p>El motor de búsqueda detecta automáticamente en qué almacén se encuentra el usuario en función del nombre de host o del parámetro de consulta <span class="codeph"> gs_store </span>, con prioridad este último. Puede crear condiciones fuera de la tienda. Solo en la limpieza de consultas, también puede utilizar una acción para anular el almacenamiento actual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Última regla </p> </td> 
      <td colname="col2"> <p>Cuando se cumplen las condiciones de una regla que tiene el último conjunto de reglas, el módulo de procesamiento de limpieza de consultas no realiza ninguna regla adicional después de la acción de la regla coincidente. Esto resulta útil cuando ha establecido acciones que harán que una regla posterior coincida pero no desea que la regla posterior se active. Tenga en cuenta que, si la acción de una regla es realizar una redirección, la redirección se realiza inmediatamente, por lo que básicamente actúa como si se estableciera la última regla. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Suspender </p> </td> 
      <td colname="col2"> <p>Desactiva la ejecución de la regla, pero no la elimina. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Add]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una regla de limpieza de consulta {#task_FA2FF1A7E2634350AD703485CBC27CB3}

Puede editar las reglas de limpieza de consultas existentes que haya agregado a la página Reglas de limpieza de consultas .

**Para editar una regla de limpieza de consultas**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. En la página [!DNL Query Cleaning Rules], en la columna **[!UICONTROL Actions]** de la tabla, haga clic en **[!UICONTROL Edit]** para la regla asociada que desee editar.
1. En la página [!DNL Edit Query Cleaning Rule], utilice las listas desplegables y los campos de texto para crear la consulta.

   Consulte la tabla de opciones en [Adición de una regla de limpieza de consulta](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una regla de limpieza de consulta {#task_C52D17226B824590B087CAB6970CBB01}

Puede eliminar las reglas de limpieza de consultas que ya no necesite o use.

Al eliminar una regla, el orden en que se ejecutan las reglas restantes se ajusta automáticamente para tener en cuenta la eliminación.

**Para eliminar una regla de limpieza de consultas**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. En la página [!DNL Query Cleaning Rules], en la columna **[!UICONTROL Actions]** de la tabla, haga clic en **[!UICONTROL Delete]** para la regla asociada que desee eliminar.
1. En el cuadro de diálogo [!DNL Confirmation], haga clic en **[!UICONTROL OK]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cambio del orden en que se ejecutan las reglas de limpieza de consultas {#task_C24012C45A4445468A7FD998017388CA}

Puede reordenar las reglas de limpieza de consultas para cambiar el orden en que se ejecutan en las plantillas de presentación.

Las reglas de limpieza de consultas se ejecutan en el orden en que se definieron. Cuanto más alto es el número de orden de una regla, más tarde se ejecuta en el proceso, superando a las reglas anteriores. Las reglas se reordenan introduciendo un nuevo número en la columna Orden de la tabla de la página [!DNL Query Cleaning Rules]. También puede utilizar la función de arrastrar y soltar en las reglas para cambiar su orden de ejecución.

**Cambio del orden en que se ejecutan las reglas de limpieza de consultas**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. En la página [!DNL Query Cleaning Rules], realice una de las siguientes acciones:

   * Haga clic en el encabezado de columna [!DNL Order] para ordenar las reglas en orden ascendente o descendente.
   * En la columna [!DNL Order], en el campo de texto situado a la izquierda del nombre de una regla de limpieza de consultas, escriba el número de pedido que desea que se ejecute la regla.
   * Arrastre y suelte una fila de tabla en la posición en la que desee que se ejecute la regla. Todos los números de pedido se actualizan para reflejar el nuevo orden en que se ejecutan las reglas.

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
