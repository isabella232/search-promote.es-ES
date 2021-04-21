---
description: Puede utilizar reglas comerciales para comercializar la búsqueda.
solution: Target
title: Acerca de las reglas comerciales
topic-legacy: Rules,Site search and merchandising
uuid: f2186f54-7a39-4f46-bb29-5115d5a17f07
exl-id: 6a52e0f5-29c2-4a48-b996-d217eeb52011
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '3115'
ht-degree: 1%

---

# Acerca de las reglas comerciales{#about-business-rules}

Puede utilizar reglas comerciales para comercializar la búsqueda.

## Uso de reglas comerciales {#concept_2A93D76216754D3D8412CDEA00BD26BD}

Por ejemplo, se puede configurar cuándo aparecen los banners o qué resultados aparecen y en qué orden. También puede configurar la posición de un elemento en su faceta y qué plantilla se utiliza para una búsqueda determinada. Las reglas se ejecutan en el orden en que se definieron; cuanto más alto es el número de orden de una regla, más tarde se ejecuta en el proceso, superando a las reglas anteriores. Puede arrastrar y soltar las reglas para cambiar su orden, o puede reordenarlas introduciendo un nuevo número en el cuadro de texto del orden de reglas.

Cada regla comercial está formada por déclencheur y acciones.

El déclencheur define cuándo se ejecuta la regla. Por ejemplo, cuando el término de consulta es &quot;hombre&quot; o cuando los resultados son principalmente sombreros. El déclencheur consiste en múltiples condiciones que tienen que ser todas, o cualquiera de ellas sea verdadera para que el déclencheur general sea verdadero. Puede especificar la prioridad cambiando el operador de déclencheur.

La acción define qué sucede cuando se cumple la condición de déclencheur. Por ejemplo, configurar el banner para que muestre o mueva un resultado determinado a la posición 1. La tabla de reglas muestra información resumida sobre la regla. Puede hacer clic en un nombre de regla para abrirla y ver información adicional.

La tabla de reglas muestra una lista de todas las reglas comerciales. De forma predeterminada, la tabla muestra las diez últimas reglas que se agregaron, en orden descendente. Puede hacer clic en los encabezados de columna de la tabla para ordenar las reglas en orden ascendente o descendente.

Las reglas comerciales pueden tener uno de los tres estados siguientes: Aprobado, suspendido o WIP (trabajo en curso)

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Estado de la regla comercial </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aprobado </p> </td> 
   <td colname="col2"> <p>Las reglas comerciales aprobadas se ejecutan en el entorno en directo y en el entorno de ensayo. Apruebe una regla comercial en el Creador de reglas avanzado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Suspendido </p> </td> 
   <td colname="col2"> <p>Las reglas comerciales suspendidas nunca se ejecutan en el entorno de ensayo o en el entorno de lanzamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>WIP </p> </td> 
   <td colname="col2"> <p>WIP (Work In Progress) son reglas comerciales que no se aprueban ni se suspenden. Es decir, es posible que siga trabajando en ellas o que desee probarlas primero antes de aprobarlas. Las reglas comerciales en estado de trabajo en curso se ejecutan solo en el entorno de ensayo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Las reglas comerciales se aprueban y se activan para que se ejecuten en su entorno de lanzamiento. Actualmente, solo puede insertar *todas* las reglas en vivo. Sin embargo, puede cambiar el estado de una regla para tener control sobre qué reglas se ejecutan y no se ejecutan en el entorno en directo.

De forma predeterminada, las reglas se ejecutan siempre que se cumplen sus déclencheur asociados. Sin embargo, si lo desea, puede programar una regla para que se ejecute en un intervalo de fecha y hora específico.

Además, de forma predeterminada, las reglas se ejecutan siempre que se cumplen sus déclencheur asociados para todas las tiendas. Si desea que la regla solo se aplique a ciertas tiendas, puede utilizar el panel Almacenes para seleccionar una o más tiendas a las que se aplica la regla.

## Adición de una nueva regla comercial {#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7}

Puede utilizar [!DNL Visual Rule Builder] o [!DNL Advanced Rule Builder] para agregar reglas comerciales que adapten la experiencia de búsqueda del cliente.

**Para agregar una nueva regla comercial**

Los siguientes pasos suponen que está utilizando el Generador de reglas visual.

1. Realice uno de los siguientes pasos:

   * En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**. En la página [!DNL Business Rules], haga clic en **[!UICONTROL Add New Rule]**.

   * En el menú del producto, haga clic en **[!UICONTROL Simulator]**. En la página **[!UICONTROL Simulator for Today]** , haga clic en **[!UICONTROL Add New Rule]** a la derecha del menú desplegable **[!UICONTROL Options]**.

      Si la opción **[!UICONTROL Add New Rule]** no está visible en la página, en el menú desplegable **[!UICONTROL Options]**, haga clic en **[!UICONTROL Simulate Staged]**.

      ![](assets/Simulator.png)

1. En el campo de texto **[!UICONTROL Name]**, escriba el nuevo nombre de la regla comercial.

   Aún no haga clic en **[!UICONTROL Save Rule]**.
1. (Opcional) Si administra un gran número de reglas comerciales, puede etiquetar reglas comerciales con etiquetas específicas. En el campo **[!UICONTROL Tags]**, introduzca una o más etiquetas de etiqueta, Use una coma, Tab o Enter como delimitador.

   En la página [!DNL Business Rules], utilice la función **[!UICONTROL Filter by tag]** para filtrar las reglas que coincidan con una etiqueta determinada. 1. En la página [!DNL Business Rule Builder], establezca los déclencheur y las acciones que desee utilizar.

   **opciones de déclencheur**

   Los déclencheur son las condiciones que deben cumplirse para que se ejecute una regla comercial. Cuando una regla comercial tiene varios déclencheur, puede configurar la respuesta de los déclencheur mediante uno de los tres métodos siguientes:

   * Una respuesta en la que todos los déclencheur deben ser verdaderos (la configuración predeterminada) como en el siguiente ejemplo:

      `if a AND b AND c then ...`

   * Una respuesta en la que cualquiera de los déclencheur debe ser verdadero como en el siguiente ejemplo:

      `if a OR b OR c then ...`

   * Respuesta en la que se especifica una combinación personalizada de déclencheur. Es decir, se combinan déclencheur individuales o &quot;condiciones&quot; con operadores `AND` y `OR`.

      También puede modificar la prioridad de evaluación añadiendo combinaciones de paréntesis de apertura y cierre, como en el siguiente ejemplo:

      `if (a OR b) AND c then ...`

      >[!NOTE]
      >
      >Si combina operadores `AND` con operadores `OR` en un conjunto de reglas comerciales personalizadas, asegúrese de especificar los paréntesis de forma adecuada para garantizar que los déclencheur se evalúen en el orden correcto.

      Esta característica particular de poder personalizar una combinación de déclencheur no está activada de forma predeterminada. Póngase en contacto con el soporte técnico para activar esta función para su uso.
   <table> 
      <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>opción déclencheur </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Coincidencias de palabras clave </p> </td> 
      <td colname="col2"> <p>El déclencheur es verdadero cuando el término de búsqueda coincide con la palabra clave que distingue entre mayúsculas y minúsculas dada. El déclencheur es verdadero tanto para la palabra clave como para todos sus sinónimos, tal como se definen en el diccionario de Lingüística. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Coincidencias de consultas </p> </td> 
      <td colname="col2"> <p> El déclencheur es verdadero cuando coinciden todos los parámetros de búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> El grupo de resultados es dominante </p> </td> 
      <td colname="col2"> <p> El déclencheur es verdadero cuando el grupo de resultados definido por la búsqueda dada domina el conjunto de resultados. </p> <p>De forma predeterminada, la dominación se establece en 50%. Esta configuración es una preferencia de comercialización que puede establecer. </p> <p> 
        <!--See <xref href="t_Configuring_Merchandising_preferences.xml#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A" type="task" format="dita" scope="local">Configuring Merchandising preferences</xref>. --> </p> <p>El grupo completo debe estar presente en el conjunto de resultados para que este déclencheur sea verdadero. El grupo de resultados es dinámico. Pueden cambiar después de las operaciones de índice, según los resultados que coincidan con los criterios de búsqueda originales. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>El grupo de resultados está presente </p> </td> 
      <td colname="col2"> <p> El déclencheur es verdadero cuando el grupo de resultados definido por la búsqueda dada está presente en el conjunto de resultados. El grupo completo debe estar presente en el conjunto de resultados para que se cumpla este déclencheur (los resultados pueden estar presentes en cualquier página). El grupo de resultados es dinámico y puede cambiar después de las operaciones de índice en función de los resultados que coincidan con los criterios de búsqueda originales. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Resultados presentes </p> </td> 
      <td colname="col2"> <p> El déclencheur es verdadero cuando el resultado individual se encuentra dentro del conjunto de resultados. El resultado puede estar en cualquier parte del conjunto de resultados, no tiene que estar en la página que el usuario está viendo en ese momento. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Opciones de acción**

   Cuando se cumplen los déclencheur de una regla comercial, se realizan las acciones asociadas a la regla. Aunque el Generador de reglas visual le permite crear las siguientes acciones, puede usar el Generador de reglas avanzado para crear tipos adicionales de acciones.

   Las acciones Eliminar elemento de faceta, Mostrar elemento de faceta, Mostrar faceta, Quitar faceta o Insertar elemento de faceta de la tabla siguiente requieren una faceta. La interfaz para elegir una faceta depende de cómo esté configurada la cuenta. Por ejemplo, una cuenta normal utiliza una lista desplegable para elegir facetas. Sin embargo, si la cuenta tiene facetas asignadas, aparece un cuadro de texto autocompletado donde puede introducir el nombre de cualquier faceta. El llenado automático sugiere facetas en una lista desplegable a medida que escribe el nombre de la faceta. Las sugerencias incluyen facetas definidas actualmente. Si su cuenta tiene un mapa de ranura, también sugiere facetas asignadas.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción Acciones </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Grupo push </p> </td> 
      <td colname="col2"> <p> Inserta el grupo de resultados de búsqueda definido por los criterios de búsqueda especificados en una posición específica. </p> <p>La inserción de un grupo de resultados de búsqueda no agrega el grupo de forma implícita. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Agregar grupo </p> </td> 
      <td colname="col2"> <p> Agregue el grupo de resultados de búsqueda definido por los criterios de búsqueda especificados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Quitar grupo </p> </td> 
      <td colname="col2"> <p> Elimine el grupo de resultados de búsqueda definido por los criterios de búsqueda especificados. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Insertar una sola </p> </td> 
      <td colname="col2"> <p> Inserta el resultado de búsqueda individual en la posición seleccionada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Agregar una sola </p> </td> 
      <td colname="col2"> <p> Agrega un resultado de búsqueda individual a la posición seleccionada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Eliminar una sola </p> </td> 
      <td colname="col2"> <p> Elimina un resultado de búsqueda individual del conjunto de resultados de búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Eliminar todos los resultados </p> </td> 
      <td colname="col2"> <p>Elimina todos los resultados del conjunto de resultados de búsqueda. </p> <p> 
        <!-- Bug #3331637 The option is meant to be used in conjunction with other rule actions in order to create "canned landing pages" where we want to create a page's content solely by rule actions, and need to completely discard the "natural" results of the search. Given that the other options don't have any kind of "here's how/why you might use this", I don't see much point in breaking that precedent here.--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Seleccionar un banner diferente </p> </td> 
      <td colname="col2"> <p> Cambia el banner en el área del banner seleccionado. </p> <p>Esta opción está disponible al hacer clic con el botón derecho en un banner del área de visualización de la página web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Agregar comandos de banner </p> </td> 
      <td colname="col2"> <p>Solo se aplica a las plantillas de Dynamic Media Classic de Adobe. </p> <p>Permite cambiar los parámetros predeterminados que se utilizan en la plantilla de banner. </p> <p>Consulte la tabla de opciones en <a scope="local" href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita"> Adición de un banner con Adobe Dynamic Media Classic </a>. </p> <p>Consulte también <a href="../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9" type="task" format="dita" scope="local"> Edición de un banner con Adobe Dynamic Media Classic </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Quitar banner </p> </td> 
      <td colname="col2"> <p> Quita el banner del área del banner seleccionada; no se muestra ningún banner a menos que otra regla que configure un banner anule esta regla. </p> <p>Esta opción está disponible al hacer clic con el botón derecho en un banner del área de visualización de la página web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Elemento de faceta push </p> </td> 
      <td colname="col2"> <p> Inserta un elemento dentro de una faceta en la posición seleccionada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Quitar zona </p> </td> 
      <td colname="col2"> <p> Quita una zona de la página de resultados de la búsqueda. </p> <p>Consulte también la acción Quitar faceta a continuación. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mostrar zona </p> </td> 
      <td colname="col2"> <p> Muestra una zona en la página de resultados de la búsqueda. </p> <p>Consulte también la acción Mostrar faceta a continuación. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Quitar elemento de faceta </p> </td> 
      <td colname="col2"> <p> Quita un elemento de faceta de una faceta. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mostrar elemento de faceta </p> </td> 
      <td colname="col2"> <p> Muestra un elemento de faceta específico. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mostrar faceta </p> </td> 
      <td colname="col2"> <p> Muestra una faceta específica. Se prefiere esta acción sobre la acción Mostrar zona . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Quitar faceta </p> </td> 
      <td colname="col2"> <p> Quita una faceta específica. Se prefiere esta acción sobre la acción Eliminar zona. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Según el panel del generador de reglas que esté activo (desplegado), también puede hacer lo siguiente para establecer déclencheur y acciones.

   * Cuando se despliegue el panel **[!UICONTROL Triggers]** : en el área de plantilla de presentación de la página Generador de reglas comerciales , haga clic con el botón secundario en cualquier resultado de búsqueda o faceta de búsqueda y, a continuación, haga clic en **[!UICONTROL Add "result present" trigger]**.

      En el panel Déclencheur, haga clic en la &quot;X&quot; situada a la izquierda de un déclencheur para eliminarla de la lista de déclencheur.

   * Cuando se despliegue el panel **[!UICONTROL Actions]** : en el área de plantilla de presentación de la página Generador de reglas comerciales , haga clic con el botón derecho en un resultado de búsqueda. Haga clic en **[!UICONTROL Add Result]**, **[!UICONTROL Remove Result]**, **[!UICONTROL Push to bottom]** o **[!UICONTROL Push to #`<n>`]** (donde `<n>` es un número).


1. (Opcional) En cualquier panel del Generador de reglas comerciales ( [!DNL Triggers], [!DNL Actions] o [!DNL Schedule]), realice una de las siguientes acciones:

   * En el área de la plantilla de presentación del área de la página Generador de reglas comerciales , haga clic con el botón secundario en un banner y, a continuación, haga clic en **[!UICONTROL Select different banner]**. En la página **[!UICONTROL Pick Banner]**, haga clic **[!UICONTROL Pick this banner]** debajo de la miniatura del banner para agregarla a la plantilla de presentación. Solo los banners que coincidan con el tamaño y el área del banner original en la plantilla de presentación están disponibles para que usted pueda seleccionarlos.

      La acción agregar banner se agrega al panel [!DNL Actions].

   * En el área de la plantilla de presentación de la página [!DNL Business Rule Builder], haga clic con el botón secundario en un banner de plantilla de Dynamic Media Classic de Adobe cuyos parámetros desee cambiar y, a continuación, haga clic en **[!UICONTROL Add banner commands]**. En el cuadro de diálogo [!DNL Change Parameters], defina las opciones de parámetro que desee.

      Consulte la tabla de opciones en [Adición de un banner con Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

      Haga clic **[!UICONTROL Save]**.

      Los cambios del parámetro se añaden al panel [!DNL Actions] .

      Consulte también [Edición de un banner con Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   * En el área de la plantilla de presentación de la página Generador de reglas comerciales , haga clic con el botón secundario en un banner que desee eliminar de la página y, a continuación, haga clic en **[!UICONTROL Remove banner]**. La acción quitar banner se agrega al panel Acciones.

1. (Opcional) En el panel **[!UICONTROL Schedule]**, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Run Indefinitely]** para que la regla se ejecute siempre que se cumplan sus déclencheur asociados. Esta opción es la predeterminada.
   * Haga clic en **[!UICONTROL Fixed Schedule]** y, a continuación, especifique la fecha y la hora de inicio y la fecha y hora de finalización para que la regla se ejecute siempre que se cumpla su déclencheur asociado.

1. Haga clic **[!UICONTROL Save Rule]**.
1. (Opcional) En la página [!DNL Business Rules], realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Edición de una regla empresarial {#task_375CFA75D1D94D9E92A35DE1228E5087}

Puede usar el Generador de reglas visual o el Generador de reglas avanzado para editar las reglas comerciales que haya agregado.

**Para editar una nueva regla comercial**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. En la página [!DNL Business Rules], realice una de las siguientes acciones:

   * En la columna [!DNL Name], haga clic en el nombre de una regla comercial que desee cambiar.

      La regla de negocio se abre en la interfaz predeterminada que se especifica en **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL My Preferences]**.

   * En la lista desplegable, junto al nombre de una regla comercial que desea editar, haga clic en **[!UICONTROL Edit in advanced mode]** o **[!UICONTROL Edit in visual mode]**.

1. En el campo de texto [!DNL Name], escriba el nuevo nombre de la regla comercial.

   Aún no haga clic en **[!UICONTROL Save Rule]**. 1. En la página [!DNL Business Rule Builder], establezca los déclencheur y las acciones que desee utilizar.

   Consulte la tabla de opciones en [Adición de una nueva regla comercial](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).
1. (Opcional) En cualquier panel **[!UICONTROL Business Rule Builder]** ( [!DNL Triggers], [!DNL Actions] o [!DNL Schedule], realice una de las siguientes acciones:

   * En el área de la plantilla de presentación de la página [!DNL Business Rule Builder], haga clic con el botón secundario en un banner y, a continuación, haga clic en **[!UICONTROL Select different banner]**. En [!DNL Pick Banner page], haga clic en **[!UICONTROL Pick this banner]** debajo de la miniatura del banner para agregarla a la plantilla de presentación. Solo los banners que coincidan con el tamaño y el área del banner original en la plantilla de presentación están disponibles para que usted pueda seleccionarlos.

      La acción agregar banner se agrega al panel [!DNL Actions].

   * En el área de la plantilla de presentación de la página [!DNL Business Rule Builder], haga clic con el botón secundario en un banner de plantilla de Dynamic Media Classic de Adobe cuyos parámetros desee cambiar y, a continuación, haga clic en **[!UICONTROL Add banner commands]**. En el cuadro de diálogo [!DNL Change Parameters], defina las opciones de parámetro que desee.

      Consulte la tabla de opciones en [Adición de un banner con Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

      Haga clic **[!UICONTROL Save]**.

      Los cambios del parámetro se añaden al panel [!DNL Actions] .

      Consulte también [Edición de un banner con Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   * En el área de la plantilla de presentación de la página [!DNL Business Rule Builder], haga clic con el botón secundario en un banner que desee eliminar de la página y, a continuación, haga clic en **[!UICONTROL Remove banner]**. La acción quitar banner se agrega al panel [!DNL Actions].

1. (Opcional) En el panel [!DNL Schedule], realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Run Indefinitely]** para que la regla se ejecute siempre que se cumplan sus déclencheur asociados. Esta opción es la predeterminada.
   * Haga clic en **[!UICONTROL Fixed Schedule]** y, a continuación, especifique la fecha y la hora de inicio y la fecha y hora de finalización para que la regla se ejecute siempre que se cumpla su déclencheur asociado.

1. Haga clic **[!UICONTROL Save Rule]**.

   La página [!DNL Business Rule Builder] se cierra y volverá a la página **[!UICONTROL Business Rule]**. Las reglas aparecen en la tabla . Haga clic en el encabezado de columna **[!UICONTROL Modified]** para ordenar las reglas por fecha de edición. 1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copia de una regla empresarial {#task_89F1879C71A54EE9B7454439302C03EC}

Puede copiar una regla comercial existente para utilizarla como base para una nueva regla comercial que desee crear.

**Para copiar una regla comercial**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. En la página **[!UICONTROL Business Rules]**, en la lista desplegable junto al nombre de una regla comercial que desea copiar, haga clic en **[!UICONTROL Copy rule]**.
1. Edite la regla comercial copiada como de costumbre.

   Consulte [Edición de una regla comercial](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

## Aprobación de reglas comerciales {#task_BD569D18BF664272B8692294C162E2C1}

Puede activar las reglas comerciales que tengan un estado de WIP (Work In Progress) o suspendido.

**Para aprobar reglas comerciales**

1. En el menú del producto, haga clic en **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. En la página [!DNL Business Rules], utilizando el encabezado de columna de estado en la columna [!DNL Status] de la tabla de reglas comerciales, ordene las reglas que tengan un estado de **[!UICONTROL WIP]** o **[!UICONTROL suspended]**.

   Utilice el encabezado de columna de la casilla de verificación que hay en la parte izquierda de la tabla para comprobar todas las reglas que se muestran actualmente en la página o para marcar solo las que tienen un estado de **[!UICONTROL WIP]** o **[!UICONTROL suspended]**. 1. En la barra de menús situada cerca de la parte superior de la página, haga clic en **[!UICONTROL Approve]**.
1. En el cuadro de diálogo **[!UICONTROL Confirm Action]**, haga clic en **[!UICONTROL OK]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suspender las reglas comerciales {#task_364E1FFB905141C08E306C8F1794A20E}

Puede suspender las reglas de negocio que tengan un estado de WIP (Work In Progress) o aprobado.

Cuando suspendió una regla, está indicando en la interfaz de usuario que la ha vuelto temporalmente inactiva y que está aplazando cualquier trabajo en ella por otro tiempo. Sin embargo, aún puede editar una regla suspendida.

**Para suspender reglas comerciales**

1. En el menú del producto, haga clic en **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. En la página [!DNL Business Rules], utilizando el estado en la columna Estado de la tabla de reglas comerciales, en la columna del extremo izquierdo de la tabla, compruebe las reglas que tienen un estado de **[!UICONTROL WIP]** o **[!UICONTROL approved]**.
1. En la barra de menús situada cerca de la parte superior de la página, haga clic en **[!UICONTROL Suspend]**.
1. En el cuadro de diálogo **[!UICONTROL Confirm Action]**, haga clic en **[!UICONTROL OK]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Reanudar reglas comerciales {#task_E67D678C765B436EA2A3D6ADD7A49ABA}

Puede reanudar las reglas comerciales para reactivar una regla suspendida. Después de reanudar la regla de negocio, su estado se establece en WIP (Work In Progress).

**Para reanudar las reglas comerciales**

1. En el menú del producto, haga clic en **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. En la página [!DNL Business Rules], utilizando el estado en la columna Estado de la tabla de reglas comerciales, en la columna del extremo izquierdo de la tabla, compruebe las reglas que tienen el estado **[!UICONTROL suspended]**.
1. En la barra de menús situada cerca de la parte superior de la página, haga clic en **[!UICONTROL Resume]**.
1. En el cuadro de diálogo [!DNL Confirm Action], haga clic en **[!UICONTROL OK]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Cambio del orden en que se ejecutan las reglas comerciales {#task_FE3B1C17307F49B49050C2EC5A063991}

Puede reordenar las reglas comerciales para cambiar el orden en que se ejecutan en las plantillas de presentación.

Las reglas comerciales se ejecutan en el orden en que se definieron; cuanto más alto es el número de orden de una regla, más tarde se ejecuta en el proceso, superando a las reglas anteriores. Las reglas se reordenan introduciendo un nuevo número en la columna Orden de la tabla de la página [!DNL Business Rules]. También puede utilizar la función de arrastrar y soltar en las reglas para cambiar su orden de ejecución.

**Para cambiar el orden en que se ejecutan las reglas comerciales**

1. En el menú del producto, haga clic en **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. En la página [!DNL Business Rules], en la tabla, realice una de las siguientes acciones:

   * Haga clic en el encabezado de columna **[!UICONTROL Order]** para ordenar las reglas en orden ascendente o descendente.
   * En la columna **[!UICONTROL Order]**, en el campo de texto situado a la izquierda del nombre de una regla de negocio, escriba el número de pedido que desea que se ejecute la regla.
   * Arrastre y suelte una fila de tabla en la posición en la que desee que se ejecute la regla. Todos los números de pedido se actualizan para reflejar el nuevo orden en que se ejecutan las reglas.

1. Haga clic **[!UICONTROL Save Changes]**.

   Las reglas comerciales ahora se ejecutarán en el orden especificado. La excepción es si se ha especificado una regla comercial de redireccionamiento. Si la regla de negocio de redireccionamiento se activa o se activa, el procesamiento de reglas comerciales se detiene para permitir la redirección.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Eliminación de reglas comerciales {#task_AE37B42412044541BCC6D46CF8793DFF}

Puede eliminar las reglas comerciales cuyo estado sea WIP, suspendido o aprobado mediante el menú desplegable Acciones masivas .

**Para eliminar reglas comerciales**

1. En el menú del producto, haga clic en **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. En la página [!DNL Business Rules], realice una de las siguientes acciones:

   * Utilice el encabezado de columna de la casilla de verificación para comprobar todas las reglas que se muestran actualmente en la página.
   * Compruebe solo las reglas comerciales que desee eliminar, en función del estado de la columna Estado de la tabla.

1. En la lista desplegable [!DNL Bulk Actions], haga clic en **[!UICONTROL Delete]**.
1. En el cuadro de diálogo [!DNL Confirm Action], haga clic en **[!UICONTROL OK]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
