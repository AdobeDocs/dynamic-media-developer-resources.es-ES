---
description: Las muestras constan de una fila de imágenes en miniatura con botones de desplazamiento opcionales en los lados izquierdo y derecho. Los botones de desplazamiento solo están visibles en el escritorio si todas las miniaturas no se ajustan al ancho del contenedor. En dispositivos móviles, o si las miniaturas pueden ajustarse al ancho del contenedor, no se muestran los botones de desplazamiento.
seo-description: Las muestras constan de una fila de imágenes en miniatura con botones de desplazamiento opcionales en los lados izquierdo y derecho. Los botones de desplazamiento solo están visibles en el escritorio si todas las miniaturas no se ajustan al ancho del contenedor. En dispositivos móviles, o si las miniaturas pueden ajustarse al ancho del contenedor, no se muestran los botones de desplazamiento.
seo-title: Muestras
solution: Experience Manager
title: Muestras
uuid: d44e775d-5253-4990-98a4-84ff50db09b9
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 3%

---


# Muestras{#swatches}

Las muestras constan de una fila de imágenes en miniatura con botones de desplazamiento opcionales en los lados izquierdo y derecho. Los botones de desplazamiento solo están visibles en el escritorio si todas las miniaturas no se ajustan al ancho del contenedor. En dispositivos móviles, o si las miniaturas pueden ajustarse al ancho del contenedor, no se muestran los botones de desplazamiento.

`.s7zoomviewer .s7swatches`

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto del contenedor de muestras se controla con el siguiente selector de clase CSS:

```
.s7zoomviewer .s7zoomresetbutton
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura de las muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de las muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Las muestras verticales se desplazan en relación con el contenedor del visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar muestras a 460 x 100 píxeles.

```
.s7zoomviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

El espaciado entre las miniaturas de muestra se controla con el siguiente selector de clase CSS:

`.s7zoomviewer .s7swatches .s7thumbcell`

<table id="table_565B354FEA814804A0BE3978E1242110"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> El tamaño del margen horizontal y vertical alrededor de cada miniatura. El espaciado de la miniatura real es igual a la suma del margen izquierdo y derecho que está establecido para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ejemplo**

Configurar el espaciado en diez píxeles tanto vertical como horizontalmente.

```
.s7zoomviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

El aspecto de la miniatura individual se controla con el siguiente selector de clase CSS:

`.s7zoomviewer .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Anchura de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
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
>La miniatura admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a diferentes estados de miniaturas. En concreto, `state="selected"` corresponde a la miniatura de la imagen que se muestra actualmente en la vista principal, `state="default"` corresponde al resto de miniaturas y `state="over"` se utiliza al pasar el ratón.

Ejemplo: para configurar miniaturas de 56 x 56 píxeles, tenga un borde predeterminado de gris claro y un borde seleccionado de gris oscuro.

```
.s7zoomviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7zoomviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7zoomviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

El aspecto de los botones de desplazamiento izquierdo y derecho se controla con los siguientes selectores de clase CSS:

`.s7zoomviewer .s7swatches .s7scrollleftbutton`

`.s7zoomviewer .s7swatches .s7scrollrightbutton`

No es posible colocar botones de desplazamiento utilizando las propiedades CSS arriba, izquierda, abajo y derecha. En su lugar, la lógica del visor los coloca automáticamente.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Anchura del botón de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a diferentes estados de botones: `up`, `down`, `over` y `disabled`.

La información sobre herramientas de botones se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Ejemplo: para configurar botones de desplazamiento de 56 x 56 píxeles y que tengan distintas ilustraciones para cada estado.

```
.s7zoomviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```

