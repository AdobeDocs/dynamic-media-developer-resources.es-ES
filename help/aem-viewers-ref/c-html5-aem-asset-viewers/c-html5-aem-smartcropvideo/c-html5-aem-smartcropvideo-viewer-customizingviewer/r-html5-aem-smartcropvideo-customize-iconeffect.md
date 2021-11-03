---
description: El icono de reproducción se superpone en el área de vista principal. Se muestra cuando el vídeo está en pausa o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.
solution: Experience Manager
title: Icono, efecto
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: f4bf343a-4a78-470b-abe5-94e2d608f45d
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 1%

---

# Icono, efecto{#icon-effect}

El icono de reproducción se superpone en el área de vista principal. Se muestra cuando el vídeo está en pausa o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del icono de reproducción se controla con el siguiente selector de clase CSS:

```
.s7smartcropvideoviewer . s7smartcropvideoplayer .s7iconeffect
```

**Propiedades CSS del icono de reproducción**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p> La imagen mostrada para el icono de reproducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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

El efecto Icono admite la variable `state` selector de atributos. `state="play"` se utiliza cuando el vídeo está en pausa en mitad de la reproducción, y `state="replay"` se utiliza cuando el cabezal de reproducción está al final del flujo.

## Ejemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Configure un icono de reproducción de 100 x 100 píxeles.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
