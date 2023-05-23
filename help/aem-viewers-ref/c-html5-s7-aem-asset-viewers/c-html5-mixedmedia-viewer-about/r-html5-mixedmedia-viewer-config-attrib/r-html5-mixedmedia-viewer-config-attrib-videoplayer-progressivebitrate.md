---
title: VideoPlayer.progressivebitrate
description: VideoPlayer.progressivebitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: b156d3f4-c4d3-45fe-b3d3-b7ed38f6eb4d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 6%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`basado en IP`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> basado en IP</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la velocidad de bits de vídeo deseada para la reproducción de un conjunto de vídeos adaptables (en kilobits por segundo o kbps) en caso de que el sistema operativo no admita la reproducción de vídeo adaptable. </p> <p>El componente detectará el flujo de vídeo con la velocidad más cercana posible al valor especificado (pero sin sobrepasarla). Si todos los flujos de vídeo del conjunto de vídeos adaptables tienen una calidad mayor que el valor especificado, la lógica elige la velocidad de bits con la calidad más baja. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
