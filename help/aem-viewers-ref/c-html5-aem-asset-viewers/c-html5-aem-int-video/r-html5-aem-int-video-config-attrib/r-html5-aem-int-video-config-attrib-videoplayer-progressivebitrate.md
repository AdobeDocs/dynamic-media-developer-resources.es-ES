---
title: VideoPlayer.progressivebitrate
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 6%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Atributo de configuración para el visualizador de vídeo interactivo.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`basado en IP`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> basado en IP</span> </p> </td> 
   <td colname="col2"> <p> Especifica en kilobits por segundos (kbps), la velocidad de bits de vídeo que se desea reproducir desde un conjunto de vídeos adaptables en caso de que el sistema actual no admita la reproducción de vídeo adaptable. </p> <p>El componente recoge el flujo de vídeo con la velocidad de bits más cercana posible (pero sin superar) al valor especificado. Si todos los flujos de vídeo del conjunto de vídeos adaptables tienen una calidad superior a la especificada, la lógica elige la velocidad de bits con la calidad más baja. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
