---
title: Efecto Icono de reproductor de vídeo
description: El icono Reproducir se superpone en el área de vista de vídeo. Se muestra cuando el vídeo está en pausa o cuando se llega al final del vídeo y también depende del parámetro iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# Efecto Icono de reproductor de vídeo{#video-player-icon-effect}

El icono Reproducir se superpone en el área de vista de vídeo. Se muestra cuando el vídeo está en pausa o cuando se llega al final del vídeo y también depende del parámetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del icono de reproducción se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**Propiedades CSS del icono de reproducción**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> La imagen mostrada para el icono de reproducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> La anchura del icono de reproducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura del icono de reproducción. </p> </td> 
  </tr> 
 </tbody> 
</table>

El efecto de icono admite `state` selector de atributos. El selector `state="play"` se utiliza cuando el vídeo se pone en pausa en mitad de la reproducción y `state="replay"` se utiliza cuando el cabezal de reproducción está al final del flujo.

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
