---
title: Tabla de contenido
description: La tabla de contenido es un botón situado en la barra de control principal. Cuando se activa, aparece un panel desplegable con una lista de índices y etiquetas de página.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 9b61e269-201d-4083-9c47-0b73d55aa6ed
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 0%

---

# Tabla de contenido{#table-of-contents}

La tabla de contenido es un botón situado en la barra de control principal. Cuando se activa, aparece un panel desplegable con una lista de índices y etiquetas de página.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

En función de la configuración, la lista puede contener todas las páginas que están presentes en el catálogo o solo aquellas páginas que tienen etiquetas explícitas definidas. En sistemas de escritorio, si la lista es más larga que el espacio disponible en la pantalla, se muestra una barra de desplazamiento a la derecha.

La posición y el tamaño del botón de tabla de contenido en la interfaz de usuario del visor se controlan con el siguiente selector de clases CSS:

```
.s7ecatalogviewer .s7tableofcontents
```

**Propiedades CSS de la tabla de contenido**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen superior </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento desde la parte superior de la barra de control. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen restante </span> </p> </td> 
   <td colname="col2"> <p> Distancia al siguiente botón de la izquierda o al lado izquierdo de la barra de control, si es el primer botón de una fila. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> Ancho del botón de la tabla de contenido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> Altura del botón de tabla de contenido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

La información del objeto del botón se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: Para configurar un botón de tabla de contenido que se coloque a 4 píxeles de la parte inferior y a 43 píxeles de la izquierda de la barra de control principal. El tamaño es de 28 x 28 píxeles y se muestra una imagen diferente para cada uno de los cuatro estados de botón diferentes:

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
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo del panel desplegable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento interno entre los límites del panel y el contenido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p> Sombra paralela alrededor del panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>No se puede controlar el tamaño o la posición del panel desplegable desde CSS; el componente administra su diseño mediante programación.

Ejemplo: configuración de un panel desplegable con un fondo negro semitransparente, un margen de 5 píxeles alrededor del contenido y una sombra paralela:

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

El aspecto del elemento individual se controla con el siguiente selector de clase CSS:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**Propiedades CSS del elemento**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nombre de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del artículo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El elemento de lista desplegable es compatible con el selector de atributos `state`, que se puede utilizar para aplicar distintos aspectos a los estados de elemento seleccionado y desplazamiento.

Ejemplo: configuración de un elemento desplegable con una fuente Helvetica® de 14 píxeles y 19 píxeles de altura. Un elemento tiene un fondo gris oscuro al pasar el ratón por encima y un fondo gris claro al seleccionarlo:

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
   <td colname="col1"> <p> <span class="codeph"> de ancho mínimo </span> </p> </td> 
   <td colname="col2"> <p> Ancho mínimo del elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de ancho máximo </span> </p> </td> 
   <td colname="col2"> <p> Ancho máximo del elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno-derecho </span> </p> </td> 
   <td colname="col2"> <p> Distancia entre el índice de página y la etiqueta de página. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Es posible ocultar completamente el índice de página estableciendo `display:none` para la clase CSS `s7index`.

Ejemplo 1: Configurar un índice de página con una anchura mínima de 40 píxeles, una anchura máxima de 70 píxeles y un margen de 5 píxeles en el lado derecho:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Ejemplo 2 - ocultar índice de página:

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
   <td colname="col1"> <p> <span class="codeph"> de ancho mínimo </span> </p> </td> 
   <td colname="col2"> <p> Ancho mínimo del elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de ancho máximo </span> </p> </td> 
   <td colname="col2"> <p> Ancho máximo del elemento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Configuración de un índice de página con una anchura mínima de 40 píxeles y una anchura máxima de 240 píxeles:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

Si hay más elementos de los que pueden caber verticalmente en el panel desplegable y el sistema es un escritorio, el componente procesa una barra de desplazamiento vertical en el lado derecho del panel. El aspecto del área de la barra de desplazamiento se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**Propiedades CSS de la barra de desplazamiento**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> Ancho de la barra de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> principales </p> </td> 
   <td colname="col2"> <p> Desplazamiento vertical de la barra desde la parte superior del área del panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento vertical de la barra desde la parte inferior del área del panel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> derecho </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento horizontal de la barra desde el borde derecho del área del panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configure una barra de desplazamiento que tenga 28 píxeles de ancho y no tenga un margen para el área superior, derecha o inferior del panel:

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
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>El ancho de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>El color de fondo de la pista. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configure una pista de barras de desplazamiento que tenga 28 píxeles de ancho y un fondo gris semitransparente:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

El pulgar de la barra de desplazamiento se mueve verticalmente dentro del área de la pista de desplazamiento. Su posición vertical se controla mediante la lógica del componente. Sin embargo, la altura de la miniatura no cambia dinámicamente según la cantidad de contenido. Puede configurar la altura de la miniatura y otros aspectos con el siguiente selector de clase CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**Propiedades CSS de la miniatura de la barra de desplazamiento**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>La anchura del pulgar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>La altura del pulgar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno superior </span> </p> </td> 
   <td colname="col2"> <p> El margen vertical entre la parte superior de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno inferior </span> </p> </td> 
   <td colname="col2"> <p>El margen vertical entre la parte inferior de la pista. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de miniatura determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura admite el selector de atributos `state`, que se puede utilizar para aplicar distintas apariencias a los estados de la miniatura `up`, `down`, `over` y `disabled`.

Ejemplo: configure una miniatura de la barra de desplazamiento de 28 x 45 píxeles, con márgenes de 10 píxeles en la parte superior e inferior y con ilustraciones diferentes para cada estado:

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

No es posible colocar los botones de desplazamiento utilizando las propiedades CSS `top`, `left`, `bottom` y `right`; en su lugar, la lógica del visor los coloca automáticamente.

**Propiedades CSS del botón de desplazamiento hacia arriba y hacia abajo**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>La altura del botón. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El botón admite el selector de atributos `state`, que se puede utilizar para aplicar distintas máscaras a los estados de los botones `up`, `down`, `over` y `disabled`.

La información del objeto del botón se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: configurar botones de desplazamiento de 28 x 32 píxeles con ilustraciones diferentes para cada estado:

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
