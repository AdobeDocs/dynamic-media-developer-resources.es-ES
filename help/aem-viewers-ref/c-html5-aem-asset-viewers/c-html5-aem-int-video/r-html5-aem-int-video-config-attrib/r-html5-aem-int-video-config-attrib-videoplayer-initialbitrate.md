---
title: VideoPlayer.initialbitrate
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Atributo de configuración para el visualizador de vídeo interactivo.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`valor`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valor</span> </p> </td> 
   <td colname="col2"> <p> Establece la velocidad de bits de vídeo (en kilobits por segundo o kbps) que se utiliza para la reproducción inicial de vídeo en un equipo de escritorio. </p> <p>Si este valor de velocidad de bits no existe en el conjunto de vídeos adaptable, el reproductor de vídeo comienza con el vídeo que tiene la siguiente velocidad de bits más baja. </p> <p>Si se establece en <span class="codeph"> 0</span>, el reproductor de vídeo comenzará desde la velocidad de bits más baja posible. </p> <p>Aplicable únicamente a sistemas que no admiten de forma nativa vídeo HLS de HTML5 (como los navegadores Firefox, Chrome e Internet Explorer 11 en Windows 10) y cuando el modo de reproducción está establecido en automático. </p> </td> 
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
