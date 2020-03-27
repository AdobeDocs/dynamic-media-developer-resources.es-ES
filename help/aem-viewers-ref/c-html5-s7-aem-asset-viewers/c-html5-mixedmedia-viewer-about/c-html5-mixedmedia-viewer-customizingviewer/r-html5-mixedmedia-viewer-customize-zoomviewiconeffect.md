---
description: El indicador de zoom se superpone en el área de vista de zoom. Se muestra cuando la imagen está en estado de restablecimiento y también depende del parámetro iconeffect.
seo-description: El indicador de zoom se superpone en el área de vista de zoom. Se muestra cuando la imagen está en estado de restablecimiento y también depende del parámetro iconeffect.
seo-title: Efecto del icono de vista de zoom
solution: Experience Manager
title: Efecto del icono de vista de zoom
topic: Dynamic media
uuid: 69a44789-9587-4459-9c75-048773c9e368
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Efecto del icono de vista de zoom{#zoom-view-icon-effect}

El indicador de zoom se superpone en el área de vista de zoom. Se muestra cuando la imagen está en estado de restablecimiento y también depende del parámetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área del visor principal**

El aspecto del área de visualización se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect
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
   <td colname="col2"> <p> Ilustración del indicador de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ancho del indicador de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del indicador de zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El efecto Icono admite el selector de `media-type` atributos, que puede utilizar para aplicar diferentes efectos de icono en diferentes dispositivos. En particular, `media-type='standard'` corresponde a sistemas de escritorio en los que la entrada del ratón se utiliza normalmente y `media-type='multitouch'` corresponde a dispositivos con entrada táctil.

Ejemplo: para configurar un indicador de zoom de 100 x 100 píxeles con diferentes ilustraciones para sistemas de escritorio y dispositivos táctiles.

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```

