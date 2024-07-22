---
title: Muestras
description: Las muestras constan de una fila de imágenes en miniatura con botones de desplazamiento opcionales en los lados izquierdo y derecho.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7040edf2-4356-4493-b886-8c5694f5863a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 1%

---

# Muestras{#swatches}

Las muestras constan de una fila de imágenes en miniatura con botones de desplazamiento opcionales en los lados izquierdo y derecho.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Los botones de desplazamiento solo están visibles en el escritorio si todas las miniaturas no caben en la anchura del contenedor. En dispositivos móviles, o si las miniaturas pueden ajustarse a la anchura del contenedor, no se muestran los botones de desplazamiento.

**Propiedades CSS de las muestras**

El aspecto del contenedor de muestras se controla con el siguiente selector de clase CSS:

```
.s7flyoutviewer .s7swatches
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> El ancho de las muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura de las muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior </span> </p> </td> 
   <td colname="col2"> <p> Las muestras verticales se desplazan en relación con el contenedor del visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar muestras de 460 x 100 píxeles:

```
.s7flyoutviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

**Propiedades CSS del espaciado de muestra de miniatura**

El espaciado entre las miniaturas de muestra se controla con el selector de clases CSS:

```
.s7flyoutviewer .s7swatches .s7thumbcell
```

<table id="table_70FAD50E38EB4647B8FAB832F552BBB8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen </span> </p> </td> 
   <td colname="col2"> <p> El tamaño del margen horizontal y vertical alrededor de cada miniatura. El espaciado de miniaturas real es igual a la suma de los márgenes izquierdo y derecho establecidos para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar el espaciado para que sea de diez píxeles vertical y horizontalmente:

```
.s7flyoutviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

**Propiedades CSS de las muestras de miniaturas**

El aspecto de la miniatura individual se controla con el siguiente selector de clase CSS:

```
.s7flyoutviewer .s7swatches .s7thumb
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> Ancho de las muestras de miniaturas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura de las muestras de miniaturas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde de las muestras de miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura admite el selector de atributos `state`, que se usa para aplicar diferentes aspectos a diferentes estados de miniaturas. En particular, `state="selected"` corresponde a la miniatura de la imagen que se muestra actualmente en la vista principal, `state="default"` corresponde al resto de las miniaturas y `state="over"` se utiliza al pasar el ratón por encima.

Ejemplo: para configurar miniaturas de 56 x 56 píxeles, con un borde predeterminado de gris claro y un borde seleccionado de gris oscuro:

```
.s7flyoutviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7flyoutviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7flyoutviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

**Propiedades CSS de los botones de desplazamiento izquierdo y derecho**

El aspecto de los botones de desplazamiento izquierdo y derecho se controla con los siguientes selectores de clase CSS:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton 
.s7flyoutviewer .s7swatches .s7scrollrightbutton
```

No es posible colocar botones de desplazamiento con las propiedades CSS `top`, `left`, `bottom` y `right`. En su lugar, la lógica del visor los coloca automáticamente.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propiedad CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> Ancho del botón de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura del botón de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p>Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Ver <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que se usa para aplicar distintas máscaras a los estados de los botones `up`, `down`, `over` y `disabled`.

La información sobre herramientas de los botones se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) para obtener más información.

Ejemplo: para configurar botones de desplazamiento de 56 x 56 píxeles con ilustraciones diferentes para cada estado:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
