---
description: La tabla de contenido es un botón ubicado en la barra de control principal. Cuando se activa, aparece un panel desplegable con una lista de índices y etiquetas de página.
seo-description: La tabla de contenido es un botón ubicado en la barra de control principal. Cuando se activa, aparece un panel desplegable con una lista de índices y etiquetas de página.
seo-title: Tabla de contenido
solution: Experience Manager
title: Tabla de contenido
topic: Dynamic media
uuid: e5da89b4-fd3f-41ab-bc55-d43c2999d4b7
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 2%

---


# Tabla de contenido{#table-of-contents}

La tabla de contenido es un botón ubicado en la barra de control principal. Cuando se activa, aparece un panel desplegable con una lista de índices y etiquetas de página.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

En función de la configuración, la lista puede contener todas las páginas que están presentes en el catálogo o solo aquellas que tienen etiquetas explícitas definidas. En los sistemas de escritorio, si la lista es más larga que el espacio de pantalla disponible, se muestra una barra de desplazamiento a la derecha.

La posición y el tamaño del botón de la tabla de contenido en la interfaz de usuario del visor se controlan con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7tableofcontents
```

**Propiedades CSS de la tabla de contenido**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento desde la parte superior de la barra de control. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Distancia al botón siguiente de la izquierda o del lado izquierdo de la barra de control si éste es el primer botón de una fila. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho del botón de la tabla de contenido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altura del botón de la tabla de contenido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes apariencias a distintos estados de botones.

La información de objeto del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: configure un botón de tabla de contenido situado 4 píxeles desde la parte inferior y 43 píxeles desde la parte izquierda de la barra de control principal; el tamaño es de 28 x 28 píxeles y se muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes:

```
.s7ecatalogviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

El aspecto del panel desplegable se controla con el siguiente selector de clase CSS:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**Propiedades CSS del panel desplegable**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo del panel desplegable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento interno entre los límites del panel y el contenido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-Shadow  </span> </p> </td> 
   <td colname="col2"> <p> Sombra paralela alrededor del panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>No es posible controlar el tamaño o la posición del panel desplegable desde CSS; el componente gestiona su diseño mediante programación.

Ejemplo: configure un panel desplegable con un fondo negro semitransparente, un margen de 5 píxeles alrededor del contenido y una sombra paralela:

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

El aspecto individual del elemento se controla con el siguiente selector de clase CSS:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**Propiedades CSS del elemento**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nombre de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El elemento de lista desplegable es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes apariencias a los estados del elemento seleccionado y al pasar el ratón por encima.

Ejemplo: configure un elemento desplegable con una fuente Helvetica de 14 píxeles y 19 píxeles de alto. Un elemento tiene un fondo gris oscuro al pasar el ratón por encima y un fondo gris claro al seleccionarlo:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

Un elemento que muestra el índice de página se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**Propiedades CSS del índice de página**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width  </span> </p> </td> 
   <td colname="col2"> <p> Ancho mínimo del elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width  </span> </p> </td> 
   <td colname="col2"> <p> Ancho máximo del elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno-derecha  </span> </p> </td> 
   <td colname="col2"> <p> Distancia entre el índice de página y la etiqueta de página. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Es posible ocultar el índice de página por completo configurando `display:none` para la clase CSS `s7index`.

Ejemplo 1: configure un índice de página con una anchura mínima de 40 píxeles, una anchura máxima de 70 píxeles y un margen de 5 píxeles en el lado derecho:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Ejemplo 2: Ocultar índice de página:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

La etiqueta de página se controla con el siguiente selector de clase CSS:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

**Propiedades CSS de la etiqueta de página**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width  </span> </p> </td> 
   <td colname="col2"> <p> Ancho mínimo del elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width  </span> </p> </td> 
   <td colname="col2"> <p> Ancho máximo del elemento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configure un índice de página con una anchura mínima de 40 píxeles y una anchura máxima de 240 píxeles:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

Si hay más elementos que se pueden ajustar verticalmente en el panel desplegable y el sistema es un escritorio, el componente procesa una barra de desplazamiento vertical en el lado derecho del panel. El aspecto del área de la barra de desplazamiento se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**Propiedades CSS de la barra de desplazamiento**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Ancho de la barra de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento de la barra de desplazamiento vertical desde la parte superior del área del panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento de la barra de desplazamiento vertical desde la parte inferior del área del panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecha </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento de la barra de desplazamiento horizontal desde el borde derecho del área del panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configure una barra de desplazamiento con una anchura de 28 píxeles y sin un margen para el área superior, derecha o inferior del panel:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

La pista de la barra de desplazamiento es el área entre los botones de desplazamiento superior e inferior. El componente establece automáticamente la posición y la altura de la pista. El seguimiento se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**Propiedades CSS de la pista de desplazamiento**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo de la pista. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configure una pista de barra de desplazamiento con una anchura de 28 píxeles y un fondo gris semitransparente:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

El pulgar de la barra de desplazamiento se mueve verticalmente dentro del área de la pista de desplazamiento. Su posición vertical está controlada por la lógica del componente. Sin embargo, la altura de la miniatura no cambia dinámicamente según la cantidad de contenido. Puede configurar la altura de la miniatura y otros aspectos con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**Propiedades CSS de la miniatura de la barra de desplazamiento**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>La anchura del pulgar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>La altura del pulgar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top  </span> </p> </td> 
   <td colname="col2"> <p> El margen vertical entre la parte superior de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno-inferior  </span> </p> </td> 
   <td colname="col2"> <p>El margen vertical entre la parte inferior de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de miniatura determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb admite el selector de atributos `state`, que se puede utilizar para aplicar diferentes apariencias a los estados de posición `up`, `down`, `over` y `disabled`.

Ejemplo: configure una miniatura de la barra de desplazamiento de 28 x 45 píxeles, tenga márgenes de 10 píxeles en la parte superior e inferior y tenga una ilustración diferente para cada estado:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

El aspecto de los botones de desplazamiento superior e inferior se controla con los siguientes selectores de clase CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

No es posible colocar los botones de desplazamiento mediante las propiedades CSS `top`, `left`, `bottom` y `right`; en su lugar, la lógica del visor los coloca automáticamente.

**Propiedades CSS del botón de desplazamiento hacia arriba y hacia abajo**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Button admite el selector de atributos `state`, que se puede utilizar para aplicar diferentes apariencias a los estados de botón `up`, `down`, `over` y `disabled`.

La información de objeto del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: configure botones de desplazamiento de 28 x 32 píxeles con diferentes ilustraciones para cada estado:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```

