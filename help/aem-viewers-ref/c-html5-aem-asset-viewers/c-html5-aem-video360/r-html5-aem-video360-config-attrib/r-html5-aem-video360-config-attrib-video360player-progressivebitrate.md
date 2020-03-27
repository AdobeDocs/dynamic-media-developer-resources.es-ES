---
description: Atributo de configuración para el visor de Video360.
seo-description: Atributo de configuración para el visor de Video360.
seo-title: Video360Player.progressivebitrate
solution: Experience Manager
title: Video360Player.progressivebitrate
topic: Dynamic media
uuid: 438c18d7-e7ac-4834-8445-def590264448
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Atributo de configuración para el visor de Video360.

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`basado en IP`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> basado en IP</span> </p> </td> 
   <td colname="col2"> <p> Especifica en kbits por segundos (o kbps), la velocidad de bits de vídeo deseada para reproducirse desde un conjunto de vídeos adaptable en caso de que el sistema actual no admita la reproducción de vídeo adaptable. </p> <p>El componente capta el flujo de vídeo con la velocidad de bits más cercana posible (pero sin superar) al valor especificado. Si todos los flujos de vídeo del conjunto de vídeos adaptable tienen una calidad superior al valor especificado, la lógica elige la velocidad de bits con la calidad más baja. </p> </td> 
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

