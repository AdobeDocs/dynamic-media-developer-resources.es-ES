---
description: Atributo de configuración para el visor de vídeo de recorte inteligente.
solution: Experience Manager
title: SmartCropVideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Atributo de configuración para el visor de vídeo de recorte inteligente.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Define el tipo de reproducción que utiliza el visor. When <span class="codeph"> auto</span> está configurado, en la mayoría de los navegadores de escritorio y en todos los dispositivos iOS, el visor utiliza la transmisión de vídeo HTML5 en formato HLS. Vuelve a la reproducción progresiva de HTML5 en determinados sistemas, como Internet Explorer y Android antiguos. </p> <p>If <span class="codeph"> progresivo</span> , el visor solo se basa en la reproducción de HTML5 como admitida de forma nativa por los navegadores y reproduce el vídeo progresivamente en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos automático y progresivo, consulte la Guía del usuario del SDK de visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

Se omite cuando el visor trabaja con vídeo externo. Consulte [Compatibilidad con vídeo externo]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
