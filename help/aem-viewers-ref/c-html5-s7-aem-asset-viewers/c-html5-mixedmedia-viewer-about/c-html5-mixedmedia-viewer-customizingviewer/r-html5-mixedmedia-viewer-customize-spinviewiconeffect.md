---
description: El indicador de giro se superpone en el área de vista de giro. Se muestra cuando la imagen está en estado de restablecimiento y también depende del parámetro iconeffect.
seo-description: El indicador de giro se superpone en el área de vista de giro. Se muestra cuando la imagen está en estado de restablecimiento y también depende del parámetro iconeffect.
seo-title: Efecto del icono de vista de giro
solution: Experience Manager
title: Efecto del icono de vista de giro
topic: Dynamic media
uuid: 33445a3d-51dc-47a4-a8d1-87d25ea001e1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Efecto del icono de vista de giro{#spin-view-icon-effect}

El indicador de giro se superpone en el área de vista de giro. Se muestra cuando la imagen está en estado de restablecimiento y también depende del parámetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7spinview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Ilustración del indicador de giro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho del indicador de giro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del indicador de giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

El indicador de giro admite el selector de `state` atributos definido `spin_1D` en caso de conjunto de giros unidimensional y `spin_2D` en caso de conjunto de giros multidimensional.

Ejemplo: para configurar un indicador de zoom de 100 x 100 píxeles.

```
.s7mixedmediaviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```

