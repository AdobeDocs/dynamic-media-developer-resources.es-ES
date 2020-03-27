---
description: El icono de reproducción se superpone en el área de la vista principal. Se muestra cuando se pone en pausa el vídeo o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.
seo-description: El icono de reproducción se superpone en el área de la vista principal. Se muestra cuando se pone en pausa el vídeo o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.
seo-title: Efecto Icono
solution: Experience Manager
title: Efecto Icono
topic: Dynamic media
uuid: 81c9c344-5256-4015-8d02-abbf09dca541
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Icon effect{#icon-effect}

El icono de reproducción se superpone en el área de la vista principal. Se muestra cuando se pone en pausa el vídeo o cuando se llega al final del vídeo, y también depende del parámetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

El aspecto del icono de reproducción se controla con el siguiente selector de clase CSS:

```
.s7interactivevideoviewer . s7videoplayer .s7iconeffect
```

**Propiedades CSS del icono de reproducción**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para el icono de reproducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Colocar dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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

El efecto Icono admite el selector de `state` atributos. `state="play"` se utiliza cuando el vídeo se pone en pausa durante la reproducción y `state="replay"` se utiliza cuando el cursor de reproducción se encuentra al final del flujo.

## Ejemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Configure un icono de reproducción de 100 x 100 píxeles.

```
.s7interactivevideoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7interactivevideoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7interactivevideoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

