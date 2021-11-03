---
description: Atributo de configuración para el visor de vídeo de recorte inteligente.
solution: Experience Manager
title: SmartCropVideoPlayer.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

Atributo de configuración para el visor de vídeo de recorte inteligente.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un toque o clic para alternar la reproducción/pausa. Establecer en <span class="codeph"> ninguno</span> deshabilita el toque o clic único para reproducir/pausar. Si está configurado como <span class="codeph"> playPause</span>, al hacer clic en el vídeo, se alternan entre la reproducción y la pausa del vídeo. En algunos dispositivos, puede utilizar controles nativos. En tal caso, <span class="codeph"> singleclick</span> está desactivado. </p> </td> 
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
