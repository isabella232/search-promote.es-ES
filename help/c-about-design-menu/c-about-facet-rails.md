---
description: Utilice el carril de facetas para reordenar grupos de facetas en una página web.
seo-description: Utilice el carril de facetas para reordenar grupos de facetas en una página web.
seo-title: Acerca del carril de faceta
solution: Target
subtopic: Navigation
title: Acerca del carril de faceta
topic: Design,Site search and merchandising
uuid: 6da2bd67-8c20-4955-9836-bc8ba88546c5
translation-type: tm+mt
source-git-commit: 6b3aa733b0dfaace956f0ffc25f433fefd21e15f

---


# Acerca del carril de faceta{#about-facet-rail}

Utilice el carril de facetas para reordenar grupos de facetas en una página web.

## Uso del carril de faceta {#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB}

Una faceta es una propiedad o característica. Es una manera de clasificar generalmente los resultados de búsqueda. Por ejemplo, fabricante, precio y color podrían considerarse un grupo de facetas. Cada faceta puede tener varias restricciones o valores. Por ejemplo, si tiene color como faceta, los &quot;valores de faceta&quot; pueden ser rojo, naranja, amarillo, verde, azul, añil y violeta.

Consulte [Acerca de las facetas](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Utilice el carril de facetas para reordenar estos grupos de facetas en una página web. Por ejemplo, supongamos que tiene una sección de resultados de búsqueda en la parte izquierda de una página web. La sección enumeraba, de arriba abajo, una faceta Categoría, una faceta Marca, una faceta Precio y una faceta Más popular. Al utilizar un carril de facetas, puede, por ejemplo, hacer que la faceta Más popular aparezca encima o debajo de la faceta Categoría.

El grupo de facetas que desea reordenar juntos pertenece a una etiqueta de carril de facetas. Una faceta solo puede pertenecer a un carril de faceta. El carril de facetas es una etiqueta de plantilla de presentación e incluye una sola representación de una faceta. Todas las facetas que pertenecen a este carril comparten esa representación de faceta única.

Consulte [Acerca de las plantillas](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5) y facetas en las etiquetas [de plantilla](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)de presentación.

## Configuración de un carril de facetas {#task_561A8FF1CAD1402B9DD33E276BBC6A0E}

Puede agregar un carril de facetas para personalizar la capa de presentación. Las barras de facetas proporcionan a los clientes una búsqueda guiada que les permite explorar en profundidad los resultados de búsqueda en función del orden de las facetas en la página web.

<!-- 

t_configuring_facet_rail.xml

-->

Los cambios que realice en los carriles de faceta se pueden revertir con la función Historial.

**Para configurar un carril de faceta**

1. Antes de configurar un carril de facetas, asegúrese de que ya ha agregado una faceta y, como parte de esa tarea, especificó un nombre de carril de facetas.

   Consulte [Adición de una nueva faceta](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. En el menú de producto, haga clic en **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facet Rail.]**
1. En la [!DNL Facet Rail] página, seleccione las facetas que desee incluir en el carril de facetas y, a continuación, defina la **[!UICONTROL Sort Facets Method]** opción en la lista desplegable.

   <!-- 
   r_facet_rail_options.xml
   -->

   | Función/Opción | Descripción |
   |--- |--- |
   | Barra de faceta Nombre | Identifica el nombre del carril de facetas.  Puede crear el nombre del carril de facetas en el momento de agregar la faceta.  Consulte [Adición de una nueva faceta](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B) |
   | Facetas incluidas | Lista de facetas posibles que puede seleccionar para agregar al carril de facetas.  Si decide ordenar facetas mediante `Custom`, el orden en que selecciona las facetas aquí determina el orden en que aparecen en el cuadro de `Custom Facet Order` texto. |
   | Ordenar facetas (método) | Elija una de las tres opciones siguientes en la lista desplegable:<ul><li>`Alpha` Las facetas se ordenan alfabéticamente con respecto a sus nombres, incluidos los caracteres de puntuación.</li><li>`Alpha (not case sensitive)` Las facetas se ordenan en orden alfabético con respecto a sus nombres, omitiendo las mayúsculas y minúsculas de los caracteres alfabéticos e incluyendo los caracteres de puntuación. </li><li>`Alpha (alphanumeric only)` Las facetas se ordenan alfabéticamente con respecto a sus nombres, omitiendo los caracteres de puntuación. </li><li>`Alpha (not case sensitive, alphanumeric only)` Las facetas se ordenan en orden alfabético con respecto a sus nombres, omitiendo las mayúsculas y minúsculas de los caracteres alfabéticos y omitiendo los caracteres de puntuación. </li><li>`Count` Las facetas se ordenan según el recuento. </li><li>`Custom` Abre el cuadro de `Custom Facet Order` texto que permite definir el orden de las facetas introduciendo el nombre exacto de cada faceta. Las etiquetas de facetas que se dejen fuera se eliminarán de la `Custom Facet Order` lista.</li></ul> |
   | Orden de faceta personalizado | Esta opción solo está disponible si seleccionó `Custom` en la lista `Sort Facets Method` desplegable.  Permite enumerar nombres de facetas, uno por línea o todos en una línea y separados por comas. Si las etiquetas de facetas están definidas, se muestran en la `Facets Included` lista, entre paréntesis.  No incluya etiquetas de facetas en el cuadro de `Custom Facet Order` texto.  Al seleccionar o anular la selección de facetas en la `Facets Included` lista, el cuadro de texto `Custom Facet Order` se actualiza automáticamente. |

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) En la [!DNL Facet Rail] página, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historial.

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)de lanzamiento.

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Edite la plantilla Presentación haciendo lo siguiente:.

   * Cree una &quot;plantilla de faceta&quot; en la plantilla de presentación.
   * Rodee la &quot;plantilla de faceta&quot; con las `<guided-facet-rail>` etiquetas.

      Consulte Facetas en etiquetas [de plantilla de](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)presentación.

      Ejemplo:

      ```
      <guided-facet-rail>
        <guided-facet>
          <guided-facet-display-name/>
          ...
          </guided-facet>
        </guided-facet-rail>
      ```

      Estas etiquetas extraen una sección de la plantilla de presentación para convertirse en un patrón repetible para cada faceta del carril de facetas. Cada faceta que pertenece al carril de facetas utiliza esta sección tallada para evaluar su salida. Solo puede aparecer una `<guided-facet-rail>` etiqueta en la plantilla de presentación final.

      Las etiquetas siguientes no necesitan el `gsname` atributo dentro `<guided-facet-rail>` porque el valor se determina dinámicamente en el momento de la búsqueda y se sustituye correctamente:

      `<guided-facet>`
      `<guided-facet-display-name>`
      `<guided-facet-total-count>`
      `<guided-facet-undo-link>`
      `<guided-facet-undo-path>`
      `<guided-facet-behavior>`

   * Guarde la plantilla de presentación y colóquela en directo.

      Consulte [Edición de una presentación o una plantilla](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transporte.
