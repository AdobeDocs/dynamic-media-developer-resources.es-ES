---
description: Atributo de configuración para el visualizador de vídeo360.
solution: Experience Manager
title: Video360Player.initialbitrate
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Developer,Business Practitioner
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 8%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Atributo de configuración para el visualizador de vídeo360.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`basado en IP`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> basado en IP</span> </p> </td> 
   <td colname="col2"> <p> Establece la velocidad de bits del vídeo (en kbits por segundo o kbps) que se utiliza para la reproducción inicial de vídeo en un escritorio. </p> <p>Si este valor de velocidad de bits no existe en el conjunto de vídeos adaptables, el reproductor de vídeo comienza con el vídeo que tiene la siguiente velocidad de bits más baja. </p> <p>Si se establece en <span class="codeph"> 0</span>, el reproductor de vídeo se inicia a partir de la velocidad de bits más baja posible. </p> <p>Solo se aplica a sistemas que no admiten de forma nativa el vídeo HTML5 HLS (como los navegadores Firefox, Chrome e Internet Explorer 11 en Windows 10) y cuando el modo de reproducción está configurado en automático. </p> </td> 
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
