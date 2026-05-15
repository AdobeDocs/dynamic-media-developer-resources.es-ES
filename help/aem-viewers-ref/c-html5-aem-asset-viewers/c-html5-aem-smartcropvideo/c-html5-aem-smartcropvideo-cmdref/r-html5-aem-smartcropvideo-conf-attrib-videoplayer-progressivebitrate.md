---
title: SmartCropVideoPlayer.progressivebitrate
description: Atributo de configuración para el visor de recorte inteligente de vídeos.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 25e3e7e9-0979-472c-a589-aaf0e221b885
TQID: 'https://experienceleague.adobe.com/HSShyhUx64vEYIAuInb1sRH5UAdknbAkQWFjYv4yvxo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 3%

---

# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

Atributo de configuración para el visor de recorte inteligente de vídeos.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`valor`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valor</span> </p> </td> 
   <td colname="col2"> <p> Especifica la velocidad de bits de vídeo deseada (en kilobits por segundo o kbps) para la reproducción de un conjunto de vídeos adaptables en caso de que el sistema operativo no admita la reproducción de vídeo adaptable. </p> <p>El componente detectará el flujo de vídeo con la velocidad más cercana posible al valor especificado (pero sin sobrepasarla). Si todos los flujos de vídeo del conjunto de vídeos adaptables tienen una calidad mayor que el valor especificado, la lógica elige la velocidad de bits con la calidad más baja. </p> </td> 
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
