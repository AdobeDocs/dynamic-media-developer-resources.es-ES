---
description: Atributo de configuración para el visor de vídeo.
seo-description: Atributo de configuración para el visor de vídeo.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic media
uuid: df669b2e-31da-4de0-b480-e54402c9545c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Atributo de configuración para el visor de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un solo clic o toque para alternar la reproducción y la pausa. Si se establece en <span class="codeph"> none</span> deshabilita el toque o clic único para reproducir/pausa. Si se establece en <span class="codeph"> playPause</span>, al hacer clic en el vídeo se alternará entre la reproducción y la pausa del vídeo. En algunos dispositivos, puede utilizar controles nativos. En ese caso, se desactiva el comportamiento de <span class="codeph"> singleclick</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```

