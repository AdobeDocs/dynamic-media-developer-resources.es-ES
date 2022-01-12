---
title: Vista de zoom flotante
description: La vista principal consiste en la imagen estática y la imagen ampliada mostrada en la vista flotante sobre la imagen estática. También consiste en el mensaje de sugerencia que se muestra sobre la imagen estática.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 3%

---

# Vista de zoom flotante{#flyout-zoom-view}

La vista principal consiste en la imagen estática y la imagen ampliada mostrada en la vista flotante sobre la imagen estática. También consiste en el mensaje de sugerencia que se muestra sobre la imagen estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS de la vista principal**

El aspecto de la vista principal se controla con el siguiente selector de clase CSS:

```
.s7flyoutviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo de la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para que la vista principal sea transparente:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Propiedades CSS del mensaje de sugerencia**

El aspecto del mensaje de sugerencia se controla con el siguiente selector de clase CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

Es posible configurar el estilo, el tamaño, la apariencia y el desplazamiento vertical de la fuente mediante CSS. Sin embargo, la alineación horizontal la gestiona la lógica del visor. Sobrescribir mediante CSS usando `left` o `right` no se admiten propiedades de .

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p>Desplazamiento desde la parte inferior de la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color de texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nombre de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p>Relleno alrededor del texto del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Color de relleno de fondo del texto del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Radio del borde de fondo del texto del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidad </span> </p> </td> 
   <td colname="col2"> <p>La opacidad del fondo del texto del mensaje. </p> <p>Para Internet Explorer 8, utilice <span class="codeph"> filtro:alfa(opacity-...) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

El mensaje de sugerencia se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) para obtener más información.

.

Ejemplo: para configurar un mensaje de punta semitransparente con una fuente Arial® de 12 píxeles y blanco, 50 píxeles de desplazamiento desde la parte inferior de la vista principal, el relleno y un borde redondeado:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
