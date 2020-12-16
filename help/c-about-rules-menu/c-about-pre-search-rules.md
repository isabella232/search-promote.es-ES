---
description: Utilice las reglas de búsqueda previa para analizar la consulta entrante y determinar qué plantilla de presentación utilizar. Las reglas de búsqueda previa se ejecutan de forma secuencial para cada consulta. Para alterar el orden de las reglas, puede utilizar la función de arrastrar y soltar. El orden real no cambia hasta que lo guarda.
seo-description: Utilice las reglas de búsqueda previa para analizar la consulta entrante y determinar qué plantilla de presentación utilizar. Las reglas de búsqueda previa se ejecutan de forma secuencial para cada consulta. Para alterar el orden de las reglas, puede utilizar la función de arrastrar y soltar. El orden real no cambia hasta que lo guarda.
seo-title: Acerca de las reglas de búsqueda previa
solution: Target
title: Acerca de las reglas de búsqueda previa
topic: Rules,Site search and merchandising
uuid: e75f9d9e-e8ca-4184-bf79-b1fdadb5c0fe
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d
workflow-type: tm+mt
source-wordcount: '1709'
ht-degree: 1%

---


# Acerca de las reglas de búsqueda previa{#about-pre-search-rules}

Utilice las reglas de búsqueda previa para analizar la consulta entrante y determinar qué plantilla de presentación utilizar. Las reglas de búsqueda previa se ejecutan de forma secuencial para cada consulta. Para alterar el orden de las reglas, puede utilizar la función de arrastrar y soltar. El orden real no cambia hasta que lo guarda.

## Uso de las reglas de búsqueda previa {#concept_5BF84BB6FACB4645BA9CB7496A01CD1F}

Las reglas de búsqueda previa suelen utilizarse para seleccionar qué plantilla de presentación muestra los resultados en función de la consulta entrante. Se pueden utilizar funciones más avanzadas para modificar la consulta que se utiliza para una búsqueda que se realiza para una plantilla de presentación. Puede agregar, eliminar o cambiar el valor de los parámetros de consulta según sea necesario. Por cada consulta entrante, un módulo de procesamiento previo a la búsqueda examina las reglas de búsqueda previa para determinar si se modifica la consulta y qué plantilla de presentación se utiliza. Cada regla de búsqueda previa consta de dos elementos principales: las acciones de la regla y las condiciones opcionales. Puede especificar un número ilimitado de reglas y condiciones. El orden de estas reglas es importante, ya que el conjunto de reglas se crea en bucle mediante regla por regla. Cuando se cumplen las condiciones de una regla, se realizan todas las acciones asociadas.

En el módulo de procesamiento previo a la búsqueda, se crean instancias de todas las plantillas definidas y sus búsquedas con nombre asociadas, donde cada búsqueda recibe una copia local de los parámetros cgi. Como resultado, puede personalizar una búsqueda agregando, eliminando o alterando uno de los parámetros cgi que utiliza la búsqueda sin alterar ninguna otra búsqueda con nombre que utilice la plantilla o afectando a cualquiera de las otras plantillas. Como resultado, si tiene una plantilla de presentación que muestra más de un conjunto de resultados, puede personalizar cada búsqueda individualmente. Si desea realizar cambios en los parámetros CGI globales antes de copiarlos en cada búsqueda de cada plantilla, utilice el módulo Limpieza de Consultas.

## Condiciones de reglas de búsqueda previa {#section_B5568ADEB28546A280720309498B045D}

Las condiciones son opcionales. Si elige que se especifiquen acciones para cada consulta, las acciones siempre se realizan. Se considera una práctica recomendada que la primera regla se ejecute para cada consulta, donde se selecciona la plantilla de presentación predeterminada. De este modo, puede estar seguro de que, independientemente de cuál sea la consulta entrante, ha seleccionado una plantilla de presentación del peor escenario para utilizarla. Las condiciones se pueden basar en cualquier parámetro de consulta CGI, cookie o variable personalizada que haya establecido una regla anterior o una variable del sistema.

## Acciones de reglas de búsqueda previa {#section_3B8E19D287554C1C969F5B8D81226981}

Se ejercen todas las acciones dentro de una regla de búsqueda previa que tenga condiciones coincidentes. Las acciones suelen consistir en una operación, los datos en los que realizar la operación y el valor que se va a utilizar. La acción más sencilla es especificar qué plantilla de presentación se utilizará cuando la consulta coincida con las condiciones de la regla de búsqueda previa. A continuación, establezca la plantilla de destino en el nombre de la plantilla de presentación. Se pueden utilizar acciones más complicadas para cambiar la búsqueda que se utiliza para una plantilla determinada mediante la realización de una operación en el parámetro de búsqueda de una plantilla. Al realizar una operación en el parámetro de búsqueda de una plantilla, se especifica una plantilla de presentación y una búsqueda.

## Reglas genéricas {#section_885ECB9DBF0C4D539C14F82BCAA35B4E}

Al realizar operaciones en el parámetro de búsqueda de una plantilla, existen dos valores especiales: *dirigido y *principal para la plantilla de presentación y la búsqueda con nombre respectivamente. Con estos valores, puede generar reglas basadas en la búsqueda principal de la plantilla de destino actual. Estas construcciones permiten generar reglas genéricas en las que no tiene que preocuparse por cómo se llama la plantilla de objetivo actual o la búsqueda principal. Obviamente, una regla de búsqueda previa anterior define cuál es la plantilla de objetivo actual. De lo contrario, se selecciona una plantilla de presentación inicial para usted, lo que produce resultados no deseados.

## Ejemplos {#section_EA153A151987454EA44A4A6862466DF6}

Establezca la plantilla predeterminada en guided.tmpl, cuando el usuario pasa un parámetro cgi llamado lang, establecido en un idioma conocido, utilice la plantilla de ese idioma.

```
    On condition: 
      Every Query 
    Perform the following actions: 
      Set targeted template to guided 
 
    On condition: 
      Query lang matches regular expression fr 
    Perform the following actions: 
      Set targeted template to guided_french 
 
    On condition: 
      Query lang matches regular expression de 
    Perform the following actions: 
      Set targeted template to guided_german
```

## Prácticas recomendadas {#section_31EBAE5E54174DEE8986CBB636746A98}

* La primera regla selecciona una plantilla predeterminada para cada consulta.
* La extracción de datos de la consulta se realiza dentro de las reglas de limpieza de consultas. Puede hacer referencia a ellos en el procesamiento de la búsqueda previa.
* Añada cualquier variable personalizada nueva que haya introducido en las reglas de búsqueda previa a una regla de búsqueda previa que se ejecute para cada consulta antes de que cualquier otra regla de búsqueda previa haga referencia a ellas.

## Añadir una nueva regla de búsqueda previa {#task_182B95918462490D8BDA7F16A81CAC11}

Puede utilizar [!DNL Pre-Search Rules] para seleccionar qué plantilla de presentación se utiliza para mostrar los resultados de búsqueda en función de la consulta entrante.

**Para agregar una nueva regla de búsqueda previa**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. En la página [!DNL Pre-Search Rules], haga clic en **[!UICONTROL Add New Rule]**.
1. En el campo [!DNL Name], escriba el nombre de la nueva regla de limpieza de consultas.
1. En la página [!DNL Add Pre-Search Rule], utilice las listas desplegables y los campos de texto para crear la consulta.

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
      <td colname="col2"> <p>Una cookie HTTP. El nombre y los valores de las cookies deben estar codificados con el identificador uniforme de recursos. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable personalizada </p> </td> 
      <td colname="col2"> <p>Variable definida por el usuario. Añada, elimine o establezca una cantidad ilimitada de variables definidas por el usuario. </p> <p>Puede hacer referencia a cualquier variable que haya definido en el módulo Limpieza de Consultas dentro de las reglas de búsqueda previa. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable de sistema </p> </td> 
      <td colname="col2"> <p>Variables de sólo lectura establecidas por el sistema interno que puede comprobar. Se admiten las siguientes variables de sistema: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostname  </span> <p>Nombre del host del servidor. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri  </span> <p>El URI solicitado sin la cadena de consulta. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args  </span> <p>Toda la cadena de consulta. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> entorno </span> <p>"Escenario" o "activo" en función de si la consulta entrante se ha enviado a su entorno de ensayo o activo. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>Dirección URL de la que proviene el cliente. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Faceta </p> </td> 
      <td colname="col2"> <p>Parámetros CGI especiales de la colección global asociados a una faceta en particular. Todos los parámetros CGI se copian en cada búsqueda con nombre dentro de una plantilla después de la limpieza de Consultas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetro de consulta </p> </td> 
      <td colname="col2"> <p>Parámetro CGI en la colección global. Estos parámetros se copian en cada búsqueda con nombre dentro de una plantilla después de la limpieza de Consultas. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetro de búsqueda de plantilla </p> </td> 
      <td colname="col2"> <p>Parámetro CGI local para una búsqueda con nombre asociada a una plantilla de presentación. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetro back-end de la plantilla </p> </td> 
      <td colname="col2"> <p>Los parámetros de consulta entrantes finalmente se traducen en parámetros de back-end que se utilizan para realizar la búsqueda. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parámetros CGI de búsqueda back-end </a>. </p> <p>Los parámetros back-end no se muestran en los elementos de navegación. Como resultado, puede ocultar cualquier parámetro adicional que desee aplicar a una búsqueda de sus clientes. El parámetro es local para una búsqueda específica dentro de una plantilla de presentación. Las acciones en los parámetros back-end son de enlace tardío; es decir, se aplican justo antes de que se envíe la búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Plantilla de objetivo </p> </td> 
      <td colname="col2"> <p>Instancia especial de una variable personalizada definida por el sistema que no se puede eliminar. Esta variable contiene la plantilla de presentación de destino actual. Puede leer o establecer esta variable especificando la variable personalizada "target_template". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Clasificación </p> </td> 
      <td colname="col2"> <p>Permite especificar la regla de clasificación que se utilizará en la búsqueda. Esta opción solo aparece cuando se han definido campos de clasificación y reglas de clasificación. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tienda </p> </td> 
      <td colname="col2"> <p>El motor de búsqueda detecta automáticamente en qué almacén se encuentra el cliente en función del nombre de host o del parámetro de consulta <span class="codeph"> gs_store </span>, con prioridad para este último. Puede crear condiciones fuera de la tienda. Solo en la limpieza de consultas, también puede utilizar una acción para cancelar la compra de la tienda actual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Última regla </p> </td> 
      <td colname="col2"> <p>Cuando se selecciona, el módulo de procesamiento de búsqueda previa no realiza ninguna regla adicional después de la acción de la regla de coincidencia. Esta acción resulta útil cuando se han establecido acciones que hacen que una regla posterior coincida pero no se desea que se ejecute la regla posterior. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Suspender </p> </td> 
      <td colname="col2"> <p>Desactiva la ejecución de la regla pero no la elimina. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Add]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una regla de búsqueda previa {#task_25F77050C5DA42B29DFD1C9718FB8C64}

Puede editar las reglas de búsqueda previa existentes que haya agregado a la página [!DNL Pre-Search Rules].

**Para editar una regla de búsqueda previa**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. En la página [!DNL Pre-Search Rules], en la columna **[!UICONTROL Actions]** de la tabla, haga clic en **[!UICONTROL Edit]** para la regla asociada que desee editar.
1. En la página [!DNL Edit Pre-Search Rule], utilice las listas desplegables y los campos de texto para crear la consulta.

   Consulte la tabla de opciones en [Añadir una nueva regla de búsqueda previa](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una regla de búsqueda previa {#task_128B6A79CA6C451C991AEDAD58F51743}

Puede eliminar las reglas de búsqueda previa que ya no necesite ni use.

Al eliminar una regla, el orden en que se ejecutan las reglas restantes se ajusta automáticamente para tener en cuenta la eliminación.

**Para eliminar una regla de búsqueda previa**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. En la página [!DNL Pre-Search Rules], en la columna **[!UICONTROL Actions]** de la tabla, haga clic en **[!UICONTROL Delete]** para la regla asociada que desee eliminar.
1. En el cuadro de diálogo [!DNL Confirmation], haga clic en **[!UICONTROL OK]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cambiar el orden en que se ejecutan las reglas de búsqueda previa {#task_C18817276A3C459089C97448076365D1}

Puede reordenar las reglas de búsqueda previa para cambiar el orden en que se ejecutan en las plantillas de presentación.

Las reglas de búsqueda previa se ejecutan en el orden en que se definieron. Cuanto mayor sea el número de orden de una regla, más tarde se ejecutará en el proceso, superando las reglas anteriores. Las reglas se reordenan introduciendo un nuevo número en la columna Orden de la tabla de la página [!DNL Pre-Search Rules]. También puede utilizar la función de arrastrar y soltar en las reglas para cambiar el orden de ejecución.

**Para cambiar el orden en que se ejecutan las reglas de búsqueda previa**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. En la página [!DNL Pre-Search Rules], realice una de las siguientes acciones:

   * Haga clic en el encabezado de columna **[!UICONTROL Order]** para ordenar las reglas en orden ascendente o descendente.
   * En la columna **[!UICONTROL Order]**, en el campo de texto a la izquierda del nombre de una regla de búsqueda previa, escriba el número de pedido que desea que se ejecute la regla.
   * Arrastre y suelte una fila de tabla en la posición en la que desee que se ejecute la regla. Todos los números de pedido se actualizan para reflejar el nuevo orden en que se ejecutan las reglas.

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración dinámica](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

