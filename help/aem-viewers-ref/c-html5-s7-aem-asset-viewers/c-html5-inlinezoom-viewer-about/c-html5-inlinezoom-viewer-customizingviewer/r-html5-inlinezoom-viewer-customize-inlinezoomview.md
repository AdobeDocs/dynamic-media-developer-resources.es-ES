---
description: La vista principal consiste en la imagen estática, la imagen ampliada que se muestra en la vista flotante sobre la imagen estática y el mensaje de sugerencia que se muestra sobre la imagen estática.
seo-description: La vista principal consiste en la imagen estática, la imagen ampliada que se muestra en la vista flotante sobre la imagen estática y el mensaje de sugerencia que se muestra sobre la imagen estática.
seo-title: vista de zoom flotante
solution: Experience Manager
title: vista de zoom flotante
topic: Dynamic media
uuid: a918c775-a36a-44e8-9ca4-90cb8f5c3a5e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Flyout zoom view{#flyout-zoom-view}

La vista principal consiste en la imagen estática, la imagen ampliada que se muestra en la vista flotante sobre la imagen estática y el mensaje de sugerencia que se muestra sobre la imagen estática.

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

Es posible configurar el estilo de fuente, el aspecto del tamaño y el desplazamiento vertical mediante CSS. Sin embargo, la alineación horizontal se gestiona mediante la lógica del visor. No se admite la anulación de CSS mediante el uso `left` o `right` las propiedades.

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
   <td colname="col2"> <p>Desvío desde la parte inferior de la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color de texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nombre de fuente. </p> </td> 
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
   <td colname="col2"> <p>Opacidad de fondo del texto del mensaje. </p> <p>Para Internet Explorer 8, utilice <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

El mensaje de sugerencia se puede localizar. Consulte [Localización de los elementos](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) de la interfaz de usuario para obtener más información.

.

Ejemplo: para configurar un mensaje de punta semitransparente con una fuente Arial blanca de 12 píxeles, 50 píxeles se desplazan de la parte inferior de la vista principal, el relleno y un borde redondeado:

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

