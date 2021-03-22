---
description: El icono de reproducción se superpone en el área de vista de vídeo. Se muestra cuando el vídeo está en pausa o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.
seo-description: El icono de reproducción se superpone en el área de vista de vídeo. Se muestra cuando el vídeo está en pausa o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.
seo-title: Efecto Icono del reproductor de vídeo
solution: Experience Manager
title: Efecto Icono del reproductor de vídeo
uuid: 5d59c4b2-a7a1-49e1-84c7-0e127a571c4f
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%

---


# Efecto del icono del reproductor de vídeo{#video-player-icon-effect}

El icono de reproducción se superpone en el área de vista de vídeo. Se muestra cuando el vídeo está en pausa o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del icono de reproducción se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**Propiedades CSS del icono de reproducción**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p> La imagen mostrada para el icono de reproducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho del icono de reproducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del icono de reproducción. </p> </td> 
  </tr> 
 </tbody> 
</table>

El efecto Icono admite el selector de atributos `state`. `state="play"` se utiliza cuando el vídeo está en pausa en mitad de la reproducción y  `state="replay"` se utiliza cuando el cabezal de reproducción está al final de la emisión.

## Ejemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Configure un icono de reproducción de 100 x 100 píxeles.

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

