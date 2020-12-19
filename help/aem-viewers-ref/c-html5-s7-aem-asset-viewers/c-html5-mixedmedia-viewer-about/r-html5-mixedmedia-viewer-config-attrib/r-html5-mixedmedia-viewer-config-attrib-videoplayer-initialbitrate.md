---
description: nulo
seo-description: nulo
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: 11426516-8336-4186-84b4-15ce5ec7e764
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`basado en IP`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p>Establece la velocidad de bits de vídeo en kbits por segundos o kbps que se utiliza para la reproducción inicial de vídeo en equipos de escritorio. </p> <p>Si este valor de velocidad de bits no existe en el conjunto de vídeos adaptable, el reproductor de vídeo inicio el vídeo que tiene la siguiente velocidad de bits más baja. </p> <p>Si se establece en <span class="codeph"> 0 </span>, el reproductor de vídeo inicio desde la velocidad de bits más baja posible. Aplicable solo para sistemas que no tienen compatibilidad nativa con vídeo HTML5 HLS (que son exploradores Firefox, Chrome e Internet Explorer 11 en Windows 10) y cuando el modo de reproducción está establecido en <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
