---
description: Puede anular la expansión de los resultados de la consulta de búsqueda.
seo-description: Puede anular la expansión de los resultados de la consulta de búsqueda.
seo-title: Acerca de las anulaciones de expansión de consultas
solution: Target
title: Acerca de las anulaciones de expansión de consultas
topic: Linguistics,Site search and merchandising
uuid: dfe18004-b8fd-4889-b01c-72a3b0c82b9c
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Acerca de las anulaciones de expansión de consultas{#about-query-expansion-overrides}

Puede anular la expansión de los resultados de la consulta de búsqueda.

## Uso de anulaciones de expansión de consultas {#concept_6895B469B0E044299E93361BFA06B554}

Al configurar una anulación de expansión de consulta, se crea un conjunto de &quot;reglas&quot;. Cada regla dice, esencialmente, &quot;No se expanda `<this>` en `<that>` el momento de la búsqueda&quot;, donde `<this>` es una simple palabra o frase de texto y `<that>` es una palabra o frase de texto o una clasificación.

>[!NOTE]
>
>Esta función no está habilitada de forma predeterminada en Search&amp;Promote. Póngase en contacto con la asistencia técnica para activar la función para su uso. Una vez habilitada la función Anulaciones de expansión de consultas, debe &quot;activarla&quot; en la interfaz de usuario.

**Funcionamiento de la anulación de expansión de consultas**

Cuando se especifica un valor de Texto y Término en la página Ampliación de consulta anula Agregar, el código actúa en el emparejamiento específico. Cuando se especifica un tipo de clasificación como un término, como Diccionarios o Formularios de palabras alternativos, el valor No expandir no se convierte en ningún formulario creado por la clasificación indicada.

Por ejemplo, supongamos que tiene la siguiente definición:

`Do Not Expand = "dog"`

`Type = Text`

`Term = "dogs"`

Una consulta de búsqueda de &quot;perro&quot;, que se expande para incluir &quot;perro&quot; y &quot;perros&quot; a través de Alternate Word Forms, no incluiría &quot;perros&quot;.

Sin embargo, si la definición era la siguiente:

`Do Not Expand = "dog"`

`Type = Alternate Word Forms`

La consulta no incluye &quot;perros&quot; ni &quot;perros&quot; (los formularios de palabras alternativos disponibles para &quot;perros&quot;).

Puede especificar varios términos, varias clasificaciones o ambos. Sin embargo, si selecciona Todos como Tipo, cualquier lista de varios términos se contrae con una sola entrada &quot;Todos&quot;.

Si las entradas de texto y clasificación se mezclan en cualquier regla, se reorganizan en la interfaz de usuario para mostrar primero los valores de texto. Sin embargo, esto no implica ni afecta el orden de evaluación en el momento de la búsqueda.

Los términos de texto se validan para eliminar referencias sin sentido. Es decir, compara el término con el valor No expandir y elimina el término si hay una coincidencia. Además, se eliminan los valores duplicados de Término, ya sea texto o clasificación.

Si agrega una nueva regla con un valor No expandir que replique una definición anterior, los términos de la nueva definición se agregan al original.

## Configuración de las anulaciones de expansión de consultas {#task_A087354A509D4997BA275186C224160E}

Definición y adición de una anulación de expansión de consulta en Search&amp;Promote.

<!-- 

t_configuring_query_expansion_overrides.xml

 -->

>[!NOTE]
Esta función no está habilitada de forma predeterminada en Search&amp;Promote. Póngase en contacto con la asistencia técnica para activar la función para su uso. Una vez habilitada la función Anulaciones de expansión de consultas, debe &quot;activarla&quot; en la interfaz de usuario. Los primeros pasos a continuación describen cómo hacerlo.

**Para configurar las anulaciones de expansión de consultas**

1. En Search&amp;Promote, haga clic en **Configuración** > **Usuario** > **Ver funciones**.
1. En la página Ver roles, en la columna Acciones de la tabla, haga clic en **Editar** a la derecha de la función a la que desea dar acceso a Anulaciones de expansión de consultas en el menú Lingüística.
1. En la página Editar rol, expanda el árbol Lingüística.
1. Seleccione Anulaciones **de expansión de consultas** y, a continuación, haga clic en **Guardar cambios**.
1. Haga clic en **Lingüística** > Anulaciones **de expansión de consultas**.
1. Haga clic en **Agregar anulaciones** de expansión de consulta.
1. En la página Anulaciones de expansión de consultas Agregar, configure las opciones que desee.

   <!-- 
   
   r_query_expansion_override_definitions.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Opción </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>No expandir </p> </td> 
      <td colname="col2"> <p>Especifica la palabra o frase que no desea expandir. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tipo  </p> </td> 
      <td colname="col2"> <p>Seleccione <b>Texto</b> para especificar un emparejamiento de palabras o frases específico. O bien, seleccione una clasificación para especificar que la palabra o frase No expandir no se convierta mediante la clasificación seleccionada. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Término </p> </td> 
      <td colname="col2"> <p>Solo está disponible si ha seleccionado <b>Texto</b> como Tipo. Especifica la palabra o frase que se va a excluir de la expansión de búsqueda. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Acción </p> </td> 
      <td colname="col2"> <p> Haga clic en <b>+</b> o <b>-</b> para agregar o eliminar términos, respectivamente, a la definición. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cuando haya terminado, haga clic en **Agregar**.

   En la página Anulaciones de expansión de consultas, puede editar o eliminar las definiciones que ha agregado.
1. Para obtener una vista previa de los resultados de las adiciones, haga clic en **volver a generar el índice** del sitio escalonado en el cuadro azul para volver a generar rápidamente el índice del sitio Web escalonado.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **Activo**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)

   * Haga clic en **Push Live**.

      Consulte [Activación de la configuración del escenario](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

