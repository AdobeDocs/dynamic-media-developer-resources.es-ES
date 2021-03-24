---
description: Atributo de configuración para el visualizador de vídeo.
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 5%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Atributo de configuración para el visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`basado en IP`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> basado en IP</span> </p> </td> 
   <td colname="col2"> <p> Especifica (en kbits por segundos o kbps) la velocidad de bits de vídeo deseada para reproducirse desde un conjunto de vídeo adaptable en caso de que el sistema actual no admita la reproducción de vídeo adaptable. </p> <p>El componente recoge el flujo de vídeo con la velocidad de bits más cercana posible (pero sin exceder) al valor especificado. Si todos los flujos de vídeo del conjunto de vídeos adaptables tienen una calidad superior a la especificada, la lógica elige la velocidad de bits con la calidad más baja. </p> </td> 
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

