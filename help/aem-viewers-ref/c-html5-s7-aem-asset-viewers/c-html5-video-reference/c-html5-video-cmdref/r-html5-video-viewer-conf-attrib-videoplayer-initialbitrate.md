---
description: Atributo de configuración para el visor de vídeo.
seo-description: Atributo de configuración para el visor de vídeo.
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: b2dde5f4-0449-4cad-a1f2-e336027f92c6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Atributo de configuración para el visor de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`basado en IP`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> basado en IP </span> </p> </td> 
   <td colname="col2"> <p>Establece la velocidad de bits de vídeo en kbits por segundos o kbps que se utiliza para la reproducción inicial de vídeo en equipos de escritorio. </p> <p>Si este valor de velocidad de bits no existe en el conjunto de vídeos adaptable, el reproductor de vídeo inicio el vídeo que tiene la siguiente velocidad de bits más baja. </p> <p>Si se establece en <span class="codeph"> 0, </span> el reproductor de vídeo inicio desde la velocidad de bits más baja posible. Aplicable solo para sistemas que no son compatibles con el vídeo HTML5 HLS (navegadores Firefox, Chrome e Internet Explorer 11 en Windows 10) y cuando el modo de reproducción está establecido en <span class="codeph"> auto </span>. </p> </td> 
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

