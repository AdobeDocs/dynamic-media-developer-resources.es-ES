---
title: Video360Player.initialbitrate
description: Atributo de configuración para el visor de Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Atributo de configuración para el visor de Video360.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`valor`*`

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
