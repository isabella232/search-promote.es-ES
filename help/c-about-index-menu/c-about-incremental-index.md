---
description: Puede usar el Índice incremental para indexar "partes" de su sitio web activo o provisional, como una colección de páginas modificadas con frecuencia.
solution: Target
subtopic: Incremental Index
title: Acerca del índice incremental
topic: Índice,Búsqueda de sitios y comercialización
uuid: b1ee9b08-dcbe-4ffe-b0b4-d379daaac9b5
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 1%

---


# Acerca del índice incremental{#about-incremental-index}

Puede usar el Índice incremental para indexar &quot;partes&quot; de su sitio web activo o provisional, como una colección de páginas modificadas con frecuencia.

## Uso del índice incremental {#concept_A7770F0552D14C47B3DDB65DB78FFFEE}

Un índice incremental tarda solo segundos en funcionar y es útil en sitios web de gran capacidad que pueden tardar muchas horas en indexarse por completo.

Cuando se genera un índice incremental, se muestra la información de estado, como la hora de inicio, el tiempo transcurrido y los errores durante el proceso de indexación. También se muestra información sobre el estado del último índice.

Puede detener o reiniciar el proceso de indexación incremental en cualquier momento.

Mientras el nuevo índice incremental se crea para el sitio web activo, los clientes pueden seguir buscando en el sitio utilizando el último índice incremental.

## Configuración del índice incremental de un sitio web escalonado {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

Puede configurar qué páginas del sitio web desea incluir en el índice incremental especificando las direcciones URL del sitio web y las máscaras de URL.

**Para configurar un índice incremental de un sitio web escalonado**

1. En el menú del producto, haga clic en **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Configuration]**.
1. En la página **[!UICONTROL Incremental Index Configuration]**, utilice los distintos campos para especificar qué páginas desea indexar.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Campo </p> </th> 
      <th colname="col2" class="entry"> <p>Descripción </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Agregar o actualizar direcciones URL </p> </td> 
      <td colname="col2"> <p>Especifique las direcciones URL. </p> <p>El robot de búsqueda solo indexa los documentos especificados que han cambiado desde la última vez que indexó. </p> <p>Además, el robot de búsqueda sigue los vínculos que están contenidos dentro de los documentos especificados e indexa solamente aquellos documentos que han cambiado. </p> <p>Este campo debe contener únicamente direcciones URL del documento y no máscaras, como en el siguiente ejemplo: </p> <p> 
        <code>
          https://www.mydomain.com/products/new.html 
        </code> </p> <p>Puede utilizar las siguientes palabras clave con la dirección URL: </p> <p> 
        <ul id="ul_62D1082ACBD547D092B10D72C56A3A1E"> 
          <li id="li_32C2B21DE75C4459908384CC44822F7D"> 
          <code>
            noindex 
          </code> <p>Si no desea indexar el texto de la página que coincida con una dirección URL especificada, pero desea seguir los vínculos de la página, agregue 
            <code>
              noindex 
            </code> después de la dirección URL, como en el siguiente ejemplo: </p> <p> 
            <code>
              https://www.mydomain.com/products/new.html noindex 
            </code> </p> <p>Asegúrese de separar 
            <code>
              noindex 
            </code> desde la dirección URL con un espacio; una coma no es un separador válido. </p> </li> 
          <li id="li_33AB62B669084BF7B976F4308715E435"> 
          <code>
            nofollow 
          </code> <p>Si desea indexar el texto de la página que coincida con la dirección URL especificada, pero no desea seguir los vínculos de la página, agregue 
            <code>
              nofollow 
            </code> después de la dirección URL, como en el siguiente ejemplo: </p> <p> 
            <code>
              https://www.mydomain.com/products/new.html nofollow 
            </code> </p> <p> Asegúrese de separar 
            <code>
              nofollow 
            </code> desde la dirección URL con un espacio; una coma no es un separador válido. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Buscar y actualizar máscaras de URL </p> </td> 
      <td colname="col2"> <p>Especifique máscaras de URL simples: ruta completa, ruta parcial o rutas que utilizan comodines o expresiones regulares. </p> <p>El robot de búsqueda encuentra todos los documentos e índices coincidentes solamente aquellos documentos que han cambiado desde la última vez que indexó. </p> <p>Además, el robot de búsqueda sigue los vínculos que están contenidos dentro de los documentos coincidentes e indexa solamente las páginas que han cambiado. Por ejemplo: </p> <p> 
      <code>
        https://www.mydomain.com/products/household/*.html 
      </code> </p> <p>También puede utilizar expresiones regulares como en el siguiente ejemplo: </p> <p> 
      <code>
        regexp ^https://www\.mydomain\.com/products/household/.*\.html$ 
      </code> </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expresiones regulares</a>. </p> <p>También puede utilizar las palabras clave 
      <code>
        nofollow 
      </code> y 
      <code>
        noindex 
      </code> tal como se describe en <span class="uicontrol"> Agregar o actualizar direcciones URL </span> más arriba. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir y excluir máscaras de URL </p> </td> 
      <td colname="col2"> <p>Especifique máscaras de URL de inclusión o exclusión simples: ruta completa, ruta parcial o rutas que utilizan comodines o expresiones regulares. </p> <p>El robot de búsqueda encuentra e indexa ("incluir") o ignora ("excluir") documentos según el tipo de máscara especificada. </p> <p> Al indexar un sitio, se siguen las indicaciones en orden de aparición. Por ejemplo, la siguiente lista de máscaras: </p> <p> 
      <code>
        include https://www.mydomain.com/products/household/lightbulbs*.html 
      </code> </p> <p> 
      <code>
        exclude https://www.mydomain.com/products/ 
      </code> </p> <p>indexa las páginas 
      <code>
        lightbulbs1.html 
      </code> y 
      <code>
        lightbulbs2.html 
      </code>. Sin embargo, no indexa ninguna otra página que aparezca bajo el directorio de productos. </p> <p>Una máscara de URL que aparece primero siempre tiene prioridad sobre una que aparece más adelante en la lista. Además, si el robot de búsqueda encuentra un documento que coincide con una máscara de inclusión y una máscara de exclusión, la máscara que aparece en primer lugar tiene prioridad. </p> <p>También puede utilizar las palabras clave 
      <code>
        nofollow 
      </code> y 
      <code>
        noindex 
      </code> tal como se describe en <span class="uicontrol"> Agregar o actualizar direcciones URL </span> más arriba. </p> <p>Consulte <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> Acerca de las máscaras de URL</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Incluir y Excluir máscaras de fecha </p> </td> 
      <td colname="col2"> <p>Especifique máscaras de fechas simples de incluir o excluir: ruta completa, ruta parcial o rutas que utilizan comodines o expresiones regulares. </p> <p>El robot de búsqueda encuentra e indexa ("incluir") o ignora ("excluir") documentos en función de la dirección URL y la fecha de los documentos. </p> <p>Puede utilizar los siguientes tipos de máscaras de fecha: </p> <p> 
      <ul id="ul_8958ED54C8EF405AA259236595ED3ABA"> 
      <li id="li_0A7841767E004F088CA6FA42E99B9F32"> 
      <code>
        include-days NNN 
      </code> <p>El robot de búsqueda indexa todos los documentos que coinciden con la máscara de URL especificada y que son NNN días o más antiguos. </p> <p>Puede seguir la máscara de URL con una o más de las siguientes palabras clave: 
        <ul id="ul_22A38D5F38B344ABB02B16EB1865813B"> 
        <li id="li_B89CC37DC2A1428185E86FFCB9DDB193">noseguir </li> 
        <li id="li_C2579B3A338D4AF987C3F518806734B0">noindex </li> 
        <li id="li_0527BF7103F34B83AC3E684069B899F7">server-date </li> 
        </ul> </p> <p>Por ejemplo, la siguiente máscara incluye todos los documentos de la carpeta /archive/support que tengan 0 días o más: </p> <p> 
        <code>
          include-days 0 https://www.mydomain.com/archive/support/ 
        </code> </p> </li> 
      <li id="li_7663ABED40DD4E159F746E4F92BB6407"> 
      <code>
        include-date YYYY-MM-DD 
      </code> <p>El robot de búsqueda indexa todos los documentos que coinciden con la máscara de dirección URL especificada y que son tan antiguos o antiguos como la fecha AAAA-MM-DD. </p> <p>Puede seguir la máscara de URL con una o más de las siguientes palabras clave: </p> <p> 
        <ul id="ul_57BF37A413BB4A4D962863DACE56F395"> 
        <li id="li_88CAB9AB583B4754A5C53478BD1108FF">noseguir </li> 
        <li id="li_999E1CD34FDE4A1B9C332B4AA8C2887D">noindex </li> 
        <li id="li_05646FACF3524D2A9E201A23770E357F"> server-date </li> 
        </ul> </p> <p>El siguiente ejemplo de máscara incluye todos los documentos de la carpeta /archive/ con fecha del 25 de julio de 2011 o anterior a esta: </p> <p> 
        <code>
          include-date 2011-07-25 https://www.mydomain.com/archive/ 
        </code> </p> </li> 
      <li id="li_172692DEDA8744B3AA492701D24C2D80"> 
      <code>
        exclude-days NNN 
      </code> <p>Deshabilite la indexación de todos los documentos que coincidan con la máscara de URL especificada y que tengan NNN días o más de antigüedad. </p> <p>Opcionalmente, puede seguir la máscara de URL por palabra clave 
        <code>
          server-date 
        </code>. </p> <p>El siguiente ejemplo de máscara excluye de su índice todos los archivos PDF que tengan 90 días o más de antigüedad: </p> <p> 
        <code>
          exclude-days 90 *.pdf 
        </code> </p> </li> 
      <li id="li_26078517744D4AECBE1351008926CBAE"> 
      <code>
        exclude-date YYYY-MM-DD 
      </code> <p>Deshabilite la indexación de todos los documentos que coincidan con la máscara de URL especificada y que tengan la antigüedad o la antigüedad anterior a la fecha AAAA-MM-DD. </p> <p>Opcionalmente, puede seguir la máscara de URL por palabra clave 
        <code>
          server-date 
        </code>. </p> <p>El siguiente ejemplo de máscara excluye todos los documentos de la carpeta /archive/ con fecha del 23 de abril de 2004 o anterior: </p> <p> 
        <code>
          exclude-date 2004-04-23 https://www.mydomain.com/archive/ 
        </code> </p> </li> 
      </ul> </p> <p>Consulte <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_F4F1F58A646F4A86B8650EC46FDCEF66" type="concept" format="dita" scope="local"> Acerca de las máscaras de fecha</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Eliminar direcciones URL </p> </td> 
      <td colname="col2"> <p>Especifique las direcciones URL. </p> <p>El robot de búsqueda encuentra y elimina los documentos especificados de su índice de búsqueda. Si una página especificada ya está en el índice de búsqueda, el robot la eliminará antes de agregar o actualizar cualquier otra página. </p> <p>Este campo solo debe contener direcciones URL del documento y no máscaras. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Buscar y eliminar máscaras de URL </p> </td> 
      <td colname="col2"> <p>Especifique máscaras de URL simples: ruta completa, ruta parcial o que usan comodines o expresiones regulares. </p> <p>Si la máscara de URL especificada coincide con páginas en el índice de búsqueda, el robot de búsqueda elimina las páginas antes de agregar o actualizar cualquier otra página. Por ejemplo: </p> <p> 
      <code>
        https://www.mydomain.com/products/1998/household/* 
      </code> </p> <p>También puede utilizar expresiones regulares como en el siguiente ejemplo: </p> <p> 
      <code>
        regexp ^https://www\.mydomain\.com/products/199[567]/.*$ 
      </code> </p> <p>Consulte <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expresiones regulares</a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Haga clic **[!UICONTROL Save Changes]**.
1. (Opcional) Realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL History]** para revertir cualquier cambio que haya realizado.

      Consulte [Uso de la opción Historial](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Haga clic **[!UICONTROL Live]**.

      Consulte [Visualización de la configuración de lanzamiento](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Haga clic **[!UICONTROL Push Live]**.

      Consulte [Inserción de la configuración del escenario en directo](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuración de la programación de índice incremental para un sitio web activo {#task_2A46BA189ECC4317A9D5C6E99A336F33}

Puede seleccionar la frecuencia del índice incremental y el tiempo base que se utiliza para rastrear y actualizar su índice incremental.

La hora seleccionada es local según la zona horaria configurada en Configuración de la cuenta.

Consulte [Configuración de la cuenta](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Los servidores web suelen estar programados para su mantenimiento a mitad de la noche. Si el servidor está inactivo durante una hora de índice programada, el proceso de indexación fallará. Asegúrese de seleccionar una hora del día en la que el servidor web esté disponible.

La programación de índices solo se aplica a su índice activo; no puede programar índices por etapas.

**Configuración de la programación de índice incremental de un sitio web activo**

1. En el menú del producto, haga clic en **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Schedule]**.
1. En la página **[!UICONTROL Incremental Index Schedule]**, en la lista desplegable **[!UICONTROL Incrementally Index]**, seleccione la frecuencia de indexación en horas o minutos.
1. En la lista desplegable **[!UICONTROL Base Time]**, seleccione la hora de inicio en la que desea volver a generar un nuevo índice incremental.
1. Haga clic **[!UICONTROL Save Changes]**.

## Ejecución de un índice incremental de un sitio web activo o por etapas {#task_9BFB6157F3884B2FAECB7E0E9CA318CB}

Puede usar el Índice incremental para indexar &quot;partes&quot; de su sitio web activo o provisional, como una colección de páginas modificadas con frecuencia.

**Ejecutar un índice incremental de un sitio web activo o provisional**

1. En el menú del producto, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Index]**.

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Index]**.

1. Haga clic **[!UICONTROL Incremental Index Now]**.
1. (Opcional) Si se produjeron errores de indexación, haga clic en **[!UICONTROL View Errors]** para ver el registro asociado.

## Visualización del registro de índice incremental de un sitio web activo o por etapas {#task_E668E1F1240C476DAA1CA783DC728232}

Cuando se completa un índice incremental activo o un índice incremental escalonado, puede ver su registro asociado para solucionar cualquier error que se haya producido.


No puede exportar registros ni guardarlos. El registro permanece disponible para su visualización hasta que se produzca el nuevo índice.

**Para ver el registro de índice incremental de un sitio web activo o provisional**

1. En el menú del producto, realice una de las siguientes acciones:

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Log]**.

   * Haga clic en **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Log]**.

1. En la página de registro, en la parte superior o inferior, realice una de las acciones siguientes:

   * Utilice las opciones de navegación **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** o **[!UICONTROL Go to line]** para desplazarse por el registro.

   * Utilice las opciones de visualización **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** o **[!UICONTROL Show]** para restringir lo que ve.

