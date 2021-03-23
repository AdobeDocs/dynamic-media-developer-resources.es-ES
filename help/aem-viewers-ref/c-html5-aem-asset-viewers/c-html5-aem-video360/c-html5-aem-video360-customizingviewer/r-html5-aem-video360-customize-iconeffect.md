---
description: El icono de reproducción se superpone en el área de vista principal. Se muestra cuando el vídeo está en pausa o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.
seo-description: El icono de reproducción se superpone en el área de vista principal. Se muestra cuando el vídeo está en pausa o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.
seo-title: Icono, efecto
solution: Experience Manager
title: Icono, efecto
uuid: a1e7d877-097c-4f43-8a6d-9627dc4924b1
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---


# Icono, efecto{#icon-effect}

El icono de reproducción se superpone en el área de vista principal. Se muestra cuando el vídeo está en pausa o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del icono de reproducción se controla con el siguiente selector de clase CSS:

```
.s7video360viewer . s7video360player .s7iconeffect
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
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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

**Ejemplo** : configure un icono de reproducción de 100 x 100 píxeles.

```
.s7video360viewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

