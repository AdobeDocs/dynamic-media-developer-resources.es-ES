---
description: Atributo de configuración para el visor de Video360.
seo-description: Atributo de configuración para el visor de Video360.
seo-title: Video360Player.initialbitrate
solution: Experience Manager
title: Video360Player.initialbitrate
topic: Dynamic media
uuid: a23fa941-6dd2-41c0-aca9-06f0cdb027b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.initialbitrate{#video-player-initialbitrate}

Atributo de configuración para el visor de Video360.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`basado en IP`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> basado en IP</span> </p> </td> 
   <td colname="col2"> <p> Establece la velocidad de bits del vídeo (en kbits por segundo o kbps) que se utiliza para la reproducción inicial del vídeo en un escritorio. </p> <p>Si este valor de velocidad de bits no existe en el conjunto de vídeos adaptable, el reproductor de vídeo inicio con el vídeo que tiene la siguiente velocidad de bits más baja. </p> <p>Si se establece en <span class="codeph"> 0</span> , el reproductor de vídeo inicio desde la velocidad de bits más baja posible. </p> <p>Solo se aplica a sistemas que no admiten de forma nativa vídeos HTML5 HLS (como los navegadores Firefox, Chrome e Internet Explorer 11 en Windows 10) y cuando el modo de reproducción está establecido en automático. </p> </td> 
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

