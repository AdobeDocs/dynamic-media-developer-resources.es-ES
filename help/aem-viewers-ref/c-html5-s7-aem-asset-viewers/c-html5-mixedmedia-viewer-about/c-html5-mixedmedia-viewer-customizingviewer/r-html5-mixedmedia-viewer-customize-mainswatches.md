---
description: Las muestras principales constan de una fila de imágenes en miniatura con botones de desplazamiento opcionales en los lados izquierdo y derecho. Los botones de desplazamiento solo están visibles en el escritorio si todas las miniaturas no se ajustan al ancho del contenedor. En los dispositivos móviles, o si las miniaturas pueden ajustarse al ancho del contenedor, no se muestran los botones de desplazamiento.
seo-description: Las muestras principales constan de una fila de imágenes en miniatura con botones de desplazamiento opcionales en los lados izquierdo y derecho. Los botones de desplazamiento solo están visibles en el escritorio si todas las miniaturas no se ajustan al ancho del contenedor. En los dispositivos móviles, o si las miniaturas pueden ajustarse al ancho del contenedor, no se muestran los botones de desplazamiento.
seo-title: Muestras principales
solution: Experience Manager
title: Muestras principales
topic: Dynamic media
uuid: a968372d-3d11-45d7-b17f-50ec998f5e88
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Muestras principales{#main-swatches}

Las muestras principales constan de una fila de imágenes en miniatura con botones de desplazamiento opcionales en los lados izquierdo y derecho. Los botones de desplazamiento solo están visibles en el escritorio si todas las miniaturas no se ajustan al ancho del contenedor. En los dispositivos móviles, o si las miniaturas pueden ajustarse al ancho del contenedor, no se muestran los botones de desplazamiento.

El aspecto del contenedor de muestras se controla con el selector de clase CSS:

```
.s7mixedmediaviewer .s7swatches
```

**Propiedades CSS de las muestras**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>La altura de las muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Las muestras verticales se desplazan en relación con el contenedor del visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar muestras con una altura de 100 píxeles.

```
.s7mixedmediviewer .s7swatches { 
 height: 100px;  
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El espaciado entre las miniaturas de muestra se controla con el siguiente selector de clase CSS:

`.s7mixedmediaviewer .s7swatches .s7thumbcell`

<table id="table_ECE063DB98154E099FB024F66FF877D7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> El tamaño de los márgenes horizontal y vertical alrededor de cada miniatura. El espaciado de miniaturas real es igual a la suma de los márgenes izquierdo y derecho definidos para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo**

Para definir el espaciado en diez píxeles tanto vertical como horizontalmente.

```
.s7mixedmediaviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

El aspecto de la miniatura individual se controla con el siguiente selector de clase CSS:

`.s7mixedmediaviewer .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde de la miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura admite el selector de `state` atributos, que se puede utilizar para aplicar diferentes apariencias a distintos estados de miniaturas. En particular, `state="selected"` corresponde a la miniatura de la imagen que se muestra actualmente en la vista principal, `state="default"` corresponde al resto de las miniaturas y `state="over"` se utiliza al pasar el ratón por encima.

Ejemplo: para configurar miniaturas de 56 x 56 píxeles, tenga un borde predeterminado de color gris claro y un borde seleccionado de color gris oscuro.

```
.s7mixedmediaviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7mixedmediaviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7mixedviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

El tipo de recurso se muestra como un icono superpuesto sobre la imagen en miniatura y se controla con el siguiente selector de clase CSS:

`.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay`

<table id="table_460FC57D12CC4B52B3782F4DFAC3A194"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura de la superposición de icono. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de la superposición de icono. </p> </td> 
  </tr> 
 </tbody> 
</table>

La superposición admite el selector de `type` atributos con los siguientes valores posibles: `image` (para imágenes únicas), `swatchset` (para conjuntos de muestras), `spinset` (para conjuntos de giros) y `video` (para vídeos únicos o conjuntos de vídeos adaptables).

Ejemplo: para configurar superposiciones de icono para conjuntos de giros, conjuntos de muestras y vídeos:

```
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="swatchset"] { 
 background-image: url(images/v2/ThumbOverlaySwatchSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="spinset"] { 
 background-image: url(images/v2/ThumbOverlaySpinSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="video"] { 
 background-image: url(images/v2/ThumbOverlayVideo.png);  
}
```

El aspecto de los botones de desplazamiento izquierdo y derecho se controla con los siguientes selectores de clase CSS:

`.s7mixedmediaviewer .s7swatches .s7scrollleftbutton`

`.s7mixedmediaviewer .s7swatches .s7scrollrightbutton`

No es posible colocar botones de desplazamiento mediante propiedades CSS `top`, `left``bottom`y `right` . En su lugar, la lógica del visor las coloca automáticamente.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho del botón de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de `state` atributos, que se puede utilizar para aplicar diferentes apariencias a diferentes estados de botón: `up`, `down`, `over`y `disabled`.

La información del objeto de botón se puede localizar. Consulte [Localización de los elementos](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) de la interfaz de usuario para obtener más información.

Ejemplo: para configurar botones de desplazamiento de 56 x 56 píxeles y con diferentes ilustraciones para cada estado.

```
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```

