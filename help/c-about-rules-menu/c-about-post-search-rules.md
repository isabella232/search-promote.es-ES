---
description: Puede utilizar las reglas posteriores a la búsqueda para examinar los resultados de una búsqueda y determinar cómo afecta la búsqueda al contenido mostrado.
solution: Target
title: Acerca de las reglas posteriores a la búsqueda
topic: Rules,Site search and merchandising
uuid: 312d1e4a-f5b6-4629-8645-17e6f6c09fc4
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '2102'
ht-degree: 0%

---


# Acerca de las reglas posteriores a la búsqueda{#about-post-search-rules}

Puede utilizar las reglas posteriores a la búsqueda para examinar los resultados de una búsqueda y determinar cómo afecta la búsqueda al contenido mostrado.

## Uso de reglas de búsqueda posterior {#concept_AF6ADFCC0ADF4A788003964939917FDE}

Si una búsqueda no tiene resultados, una regla de búsqueda posterior puede realizar una búsqueda de un elemento similar. O bien, puede mostrar una página web que recomiende otros artículos a los clientes que busquen el artículo que no se ha encontrado.

Cada regla de búsqueda posterior consta de dos elementos principales: las acciones de la regla y sus condiciones opcionales. Puede especificar un número ilimitado de reglas y condiciones. El orden de estas reglas es importante porque el conjunto de reglas pasa de una regla a otra. Cuando coinciden las condiciones de una regla, se realizan todas las acciones asociadas.

Puede refinar el conjunto de resultados de búsqueda para un máximo de tres rondas de búsqueda. Después de esto, se usa lo que esté disponible actualmente. Este límite evita bucles infinitos y garantiza que el cliente reciba una respuesta eficiente. Cuantas más veces rehaga una búsqueda, más tardará en devolver los resultados de búsqueda. Si ninguna de las reglas coincidentes altera una de las búsquedas de la plantilla de presentación utilizada actualmente o cambia la plantilla, el conjunto de resultados de búsqueda se considera finalizado y se cierra después de la búsqueda.

El procesamiento posterior a la búsqueda se basa en los módulos de procesamiento anterior Limpieza de consultas y Procesamiento de búsqueda previa. Por lo tanto, cualquier variable personalizada configurada en esos módulos está disponible para usar en las reglas de procesamiento posteriores a la búsqueda. Del mismo modo, el procesamiento de búsqueda previa ha creado una instancia de todas las plantillas en las que cada búsqueda con nombre asociada a la plantilla de presentación tiene su propia copia local de los parámetros CGI. A su vez, puede personalizar cada búsqueda individualmente.

Consulte [Acerca de las reglas de limpieza de consultas](../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C).

Consulte [Acerca de las reglas de búsqueda previa](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

## Acerca de las condiciones de las reglas posteriores a la búsqueda {#section_C43EB77CC0AC43B8B9D38569264BF1B5}

Las condiciones son opcionales. Si especifica que se especifican acciones para cada consulta, entonces las acciones siempre se realizan. Puede basar las condiciones en cualquier parámetro de consulta CGI, cookie, resultado de búsqueda o variable personalizada que haya establecido una regla anterior. O bien, puede basarla en una condición del sistema como la plantilla seleccionada actualmente o si es la última búsqueda. Cuando genera una condición en los resultados de una búsqueda o un parámetro CGI, especifica la plantilla y el nombre de la búsqueda.

## Acerca de las acciones de reglas de búsqueda posterior {#section_0E15FE683A894ECAAA386267EEC7F7C5}

Se ejercen todas las acciones de una regla de búsqueda posterior que tengan condiciones coincidentes. Las acciones suelen consistir en una operación, los datos sobre los que realizar la operación y el valor que se va a utilizar. La acción más sencilla es cambiar qué plantilla de presentación utilizar en función de las condiciones de la regla de búsqueda posterior. Puede utilizar acciones más avanzadas para cambiar los parámetros de una búsqueda que tenga como resultado que la búsqueda se esté rehaciendo. Al realizar una operación en el parámetro de búsqueda de una plantilla, especifique una plantilla Presentación y una búsqueda.

## Reglas generales {#section_AEE923988CC748FF9DEF2233FBF333B5}

Al realizar operaciones en el parámetro de búsqueda de una plantilla, existen dos valores especiales, *dirigidos y *principal para la plantilla Presentación y la búsqueda con nombre, respectivamente. Utilice estos valores para generar reglas basadas en la búsqueda principal de la plantilla de destino actual. Estas construcciones permiten generar reglas genéricas en las que no es necesario preocuparse por cómo se llama la plantilla de objetivo actual o la búsqueda principal. Si esta pasada es la primera que pasa por el procesamiento posterior a la búsqueda, la plantilla de destino es la que el procesamiento de prebúsqueda la establezca.

## Redirecciones {#section_E5669A2F13C240F2968E31C75591CD6A}

Las visitas y redirecciones directas dentro de la Limpieza de consultas permiten redirigir a una dirección URL en función de los términos de búsqueda entrantes. Las redirecciones dentro de las reglas posteriores a la búsqueda amplían esta idea, excepto que le permite comprobar cuántos resultados devolvió la búsqueda antes de decidir si desea que se produzca una redirección. Con las reglas posteriores a la búsqueda, puede redirigir a una dirección URL, donde puede sustituir variables personalizadas o parámetros de consulta. O bien, puede redirigir a un campo dentro del primer resultado. Al redirigir al campo de un resultado, se define el campo en la plantilla Transporte y debe contener una dirección URL explícita válida; de lo contrario, se omite el redireccionamiento.

Al utilizar el mecanismo de redirección dentro de las reglas posteriores a la búsqueda , puede detectar cuándo una búsqueda devuelve un único resultado. En lugar de devolver un resultado de este tipo, puede redirigir a la página web asociada al resultado.

Consulte el siguiente ejemplo de redirección para ver un ejemplo del uso de redirecciones con reglas de búsqueda posterior.

## Última regla {#section_FC1E0050C9324278B171038E98F6C335}

Cuando se cumplen las condiciones de una regla que tiene la opción **[!UICONTROL Last Rule]** establecida, el módulo de procesamiento posterior a la búsqueda no realiza ninguna regla adicional después de la acción de la regla coincidente. Esta situación es útil cuando ha establecido acciones que hacen que una regla posterior coincida pero desea que se detenga el procesamiento. Y, para que esa regla posterior pueda coincidir potencialmente después de la siguiente ronda de búsqueda.

## Ejemplos {#section_DDB98383690941F9B44AD00FBA55BB56}

En el siguiente ejemplo, suponga que tiene dos plantillas de presentación. Una plantilla se utiliza para mostrar muchos resultados de búsqueda y la otra plantilla se utiliza para mostrar un solo resultado y una búsqueda adicional de accesorios relacionados con la búsqueda principal. Desea detectar cuándo tiene un único resultado y cambiar a la otra plantilla de presentación. Para realizar esta tarea, puede utilizar las siguientes reglas:

```
On condition: 
  targeted template is default 
  targeted template primary results equal 1 
  not last search 
Perform the following actions: 
  Set targeted template to product_spotlight
```

MegaElectronic es una gran tienda electrónica. Después de analizar sus datos de búsqueda, MegaElectronic advierte que muchos de sus clientes realizan una búsqueda de producto utilizando el número de pieza de un producto. En tales casos, MegaElectronic quiere redirigir a la página web asociada con el producto, si el cliente lo buscó directamente y sólo se encontró un producto.

Para lograr este resultado, puede utilizar una sola regla con tres condiciones. La primera condición comprueba que la búsqueda devuelta solo tiene un resultado. La segunda condición garantiza que el término de consulta coincida con el formato del número de pieza de MegaElectronic para los resultados que desean que provoquen la redirección. La tercera condición garantiza que el cliente no haya utilizado ninguna faceta para explorar en profundidad un resultado, dado que el número de pieza puede ser un número de pieza parcial y devolver más de un resultado. La acción redirige a un campo dentro del resultado.

```
On condition: 
  targeted template's primary results equal 1 
  query q matches regular expression ^\D\D\D-\d+ 
  no facet selected ^\D\D\D-\d+ 
Perform the following actions: 
  redirect to result field "loc" in template *targeted for search *primary
```

## Prácticas recomendadas {#section_1BF7DE1BD5664B3BAEC26AA829FDB0BA}

* Cualquier conjunto de reglas que déclencheur una nueva ronda de búsquedas siempre debe tener una cláusula condicional para comprobar que esta no es la última pasada a través del módulo. Si ya ha realizado el número máximo de búsquedas, no puede rehacer ninguna búsqueda.
* Si está en el último paso a través del módulo y los resultados siguen siendo deficientes, puede cambiar a una plantilla &quot;sin resultados&quot;.
* Debería basar el cambio de una plantilla de presentación en el resultado de una búsqueda que potencialmente tiene otros parámetros. Si desea seleccionar una plantilla basada únicamente en la consulta entrante, una regla de búsqueda previa es más eficaz.
* La extracción de datos de la consulta se realiza en el módulo Limpieza de consultas. Puede hacer referencia a las variables personalizadas en el procesamiento posterior a la búsqueda.
* Cuando realice redirecciones, compruebe siempre que el cliente no haya seleccionado ninguna faceta. La razón de esto es que es inconveniente cuando un cliente explora una faceta y de repente se lo quita de los resultados de búsqueda. Es posible que el cliente desee anular la selección de la faceta cuando vea que el resultado único no es la intención que estaba buscando.

## Adición de una nueva regla de búsqueda posterior {#task_52F6F9AAD65B45B5ACA1FF245DFFADD9}

Puede utilizar [!DNL Post-Search Rules] para seleccionar qué plantilla de presentación se utiliza para mostrar los resultados de búsqueda en función de la consulta entrante.

**Para agregar una nueva regla de búsqueda posterior**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. En la página [!DNL Post-Search Rules], haga clic en **[!UICONTROL Add New Rule]**.
1. En el campo [!DNL Name], escriba el nombre de la nueva regla de limpieza de consultas.
1. En la página [!DNL Add Post-Search Rule], utilice las listas desplegables y los campos de texto para crear la consulta.

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
      <td colname="col2"> <p>Una cookie HTTP. Los nombres y valores de las cookies deben tener codificación Uniform Resource Identifier . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable personalizada </p> </td> 
      <td colname="col2"> <p>Variable definida por el usuario. Puede agregar, eliminar o establecer un número ilimitado de variables personalizadas. </p> <p>Puede hacer referencia a cualquier variable personalizada que haya definido en Limpieza de consultas y en los módulos Reglas de búsqueda previa, dentro de Reglas de búsqueda posterior. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable de sistema </p> </td> 
      <td colname="col2"> <p>Variables de solo lectura establecidas por el sistema interno que puede comprobar. Se admiten las siguientes variables del sistema: </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostname  </span> <p>Nombre del host del servidor. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri  </span> <p>Identificador uniforme de recursos solicitado sin la cadena de consulta. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args  </span> <p>Toda la cadena de consulta. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> entorno </span> <p>"Stage" o "live" en función de si la consulta entrante se envió al entorno de ensayo o al entorno en directo. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>El localizador uniforme de recursos del que provino el cliente. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable de sistema </p> </td> 
      <td colname="col2"> <p>Variables de solo lectura que se pueden usar en condiciones para determinar el estado actual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Faceta de búsqueda de la plantilla </p> </td> 
      <td colname="col2"> <p>Una faceta que es local para una búsqueda con nombre asociada con una plantilla de presentación. Una faceta es esencialmente parámetros CGI especiales que se utilizan para indicar qué valor dentro de una faceta ha seleccionado un cliente. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetro de búsqueda de plantilla </p> </td> 
      <td colname="col2"> <p>Un parámetro CGI local para una búsqueda con nombre asociada a una plantilla de presentación. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Parámetro back-end de la plantilla </p> </td> 
      <td colname="col2"> <p>Los parámetros de consulta entrantes finalmente se traducen en parámetros back-end que se utilizan para realizar la búsqueda. </p> <p>Consulte <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Parámetros CGI de búsqueda back-end </a>. </p> <p>Los parámetros back-end no se muestran en los elementos de navegación. Como resultado, puede ocultar cualquier parámetro adicional que desee aplicar a una búsqueda de sus clientes. </p> <p>El parámetro es local para una búsqueda específica dentro de una plantilla de presentación. Las acciones sobre parámetros de servidor son enlaces tardíos; es decir, se aplican justo antes de que se envíe la búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Plantilla de destino </p> </td> 
      <td colname="col2"> <p>Instancia especial de una variable personalizada definida por el sistema que no se puede eliminar. Esta variable contiene la plantilla de presentación de destino actual. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Clasificación </p> </td> 
      <td colname="col2"> <p>Permite especificar la regla de clasificación que se utilizará en la búsqueda. Esta opción solo aparece cuando se han definido campos de clasificación y reglas de clasificación. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Última regla </p> </td> 
      <td colname="col2"> <p>Cuando se selecciona, el módulo de procesamiento posterior a la búsqueda no realiza ninguna regla adicional después de la acción de la regla coincidente. Esta acción es útil para cuando ha establecido acciones que hacen que una regla posterior coincida pero no desea que se ejecute la regla posterior. </p> </td> 
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

## Edición de una regla de búsqueda posterior {#task_ECB00334C0A74C87AF857DB3EB372119}

Puede editar las reglas post-búsqueda existentes que haya agregado a la página [!DNL Post-Search Rules].

**Para editar una regla de búsqueda posterior**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. En la página [!DNL Post-Search Rules], en la columna **[!UICONTROL Actions]** de la tabla, haga clic en **[!UICONTROL Edit]** para la regla asociada que desee editar.
1. En la página [!DNL Edit Post-Search Rule], utilice las listas desplegables y los campos de texto para crear la consulta.

   Consulte la tabla de opciones en [Adición de una nueva regla de búsqueda posterior](../c-about-rules-menu/c-about-post-search-rules.md#task_52F6F9AAD65B45B5ACA1FF245DFFADD9).
1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de una regla de búsqueda posterior {#task_0F4653AB20D54B769A4FA8D1491AB4CF}

Puede eliminar las reglas posteriores a la búsqueda que ya no necesite o use.

Al eliminar una regla, el orden en que se ejecutan las reglas restantes se ajusta automáticamente para tener en cuenta la eliminación.

**Para eliminar una regla posterior a la búsqueda**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. En la página [!DNL Post-Search Rules], en la columna **[!UICONTROL Actions]** de la tabla, haga clic en **[!UICONTROL Delete]** para la regla asociada que desee eliminar.
1. En el cuadro de diálogo [!DNL Confirmation], haga clic en **[!UICONTROL OK]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cambio del orden en que se ejecutan las reglas de búsqueda posterior {#task_40542FCD32234BBF881A81BF5477F78F}

Puede reordenar las reglas posteriores a la búsqueda para cambiar el orden en que se ejecutan en las plantillas de presentación.

Las reglas posteriores a la búsqueda se ejecutan en el orden en que se definieron. Cuanto más alto es el número de orden de una regla, más tarde se ejecuta en el proceso, superando a las reglas anteriores. Las reglas se reordenan introduciendo un nuevo número en la columna Orden de la tabla de la página [!DNL Post-Search Rules]. También puede utilizar la función de arrastrar y soltar en las reglas para cambiar su orden de ejecución.

**Cambiar el orden en que se ejecutan las reglas de búsqueda posterior**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. En la página [!DNL Post-Search Rules], realice una de las siguientes acciones:

   * Haga clic en el encabezado de columna **[!UICONTROL Order]** para ordenar las reglas en orden ascendente o descendente.
   * En la columna [!DNL Order], en el campo de texto situado a la izquierda del nombre de una regla de búsqueda previa, escriba el número de pedido que desea que se ejecute la regla.
   * Arrastre y suelte una fila de tabla en la posición en la que desee que se ejecute la regla. Todos los números de pedido se actualizan para reflejar el nuevo orden en que se ejecutan las reglas.

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
