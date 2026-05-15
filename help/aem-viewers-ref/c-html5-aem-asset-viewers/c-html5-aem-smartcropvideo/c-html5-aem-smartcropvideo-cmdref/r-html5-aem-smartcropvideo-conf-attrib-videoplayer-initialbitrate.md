---
title: SmartCropVideoPlayer.initialbitrate
description: Atributo de configuración para el visor de recorte inteligente de vídeos.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 4fc4fefa-b094-4e2e-b8ec-a439f8a1a56c
TQID: 'https://experienceleague.adobe.com/28EPvFEtw-wS3EhTuDHpTWO1wksSmLnrKfwNJVRkFk4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 2%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

Atributo de configuración para el visor de vídeo.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`valor`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valor </span> </p> </td> 
   <td colname="col2"> <p>Establece la velocidad de bits de vídeo, en kilobits por segundo o kbps, que se utiliza para la reproducción inicial de vídeo en equipos de escritorio. </p> <p>Si este valor de velocidad de bits no existe en el conjunto de vídeos adaptable, el reproductor de vídeo inicia el vídeo que tiene la siguiente velocidad de bits más baja. </p> <p>Si se establece en <span class="codeph"> 0 </span>, el reproductor de vídeo comienza desde la velocidad de bits más baja posible. Aplicable únicamente a sistemas que no admiten de forma nativa el vídeo HLS de HTML5 (que son navegadores Firefox, Chrome e Internet Explorer 11 en Windows 10) y cuando el modo de reproducción está establecido en <span class="codeph"> auto </span>. </p> </td> 
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
