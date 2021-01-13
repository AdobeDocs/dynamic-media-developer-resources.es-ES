---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic media
uuid: 94de31cd-2b4e-4247-b181-26666767f065
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 7%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`basado en IP`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> basado en IP</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica (en kbits por segundos o kbps) la velocidad de bits de vídeo deseada para reproducirse desde un conjunto de vídeos adaptable en caso de que el sistema actual no admita la reproducción de vídeo adaptable. </p> <p>El componente recoge el flujo de vídeo con la velocidad de bits más cercana posible (pero sin superar) al valor especificado. Si todos los flujos de vídeo del conjunto de vídeos adaptable tienen una calidad superior al valor especificado, la lógica elige la velocidad de bits con la calidad más baja. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
