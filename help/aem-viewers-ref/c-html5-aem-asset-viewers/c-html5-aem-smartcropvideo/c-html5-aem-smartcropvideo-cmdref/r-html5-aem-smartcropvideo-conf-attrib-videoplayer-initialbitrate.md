---
title: SmartCropVideoPlayer.initialbitrate
description: Atributo de configuración para el visor de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

Atributo de configuración para el visualizador de vídeo.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`basado en IP`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> basado en IP </span> </p> </td> 
   <td colname="col2"> <p>Establece la velocidad de bits de vídeo (en kilobits por segundos o Kbps) que se utiliza para la reproducción inicial de vídeo en equipos de escritorio. </p> <p>Si este valor de velocidad de bits no existe en el conjunto de vídeos adaptables, el reproductor de vídeo inicia el vídeo que tiene la siguiente velocidad de bits más baja. </p> <p>Si está configurado como <span class="codeph"> 0 </span>, el reproductor de vídeo se inicia a partir de la velocidad de bits más baja posible. Aplicable solo para sistemas que no tienen compatibilidad nativa con vídeo HLS de HTML5 (que son navegadores Firefox, Chrome e Internet Explorer 11 en Windows 10) y cuando el modo de reproducción está configurado en <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
