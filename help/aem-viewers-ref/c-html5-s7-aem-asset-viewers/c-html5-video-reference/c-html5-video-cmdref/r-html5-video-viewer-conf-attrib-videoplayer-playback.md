---
title: VideoPlayer.playback
description: Atributo de configuración para el visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuración para el visor de vídeo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Establece el tipo de reproducción que utiliza el visor. Cuándo <span class="codeph"> auto</span> está configurado; en la mayoría de los navegadores de escritorio y en todos los dispositivos iOS, el visor utiliza flujo de vídeo HTML5 en formato HLS. Vuelve a la reproducción progresiva de HTML 5 en ciertos sistemas como el antiguo Internet Explorer y Android™. </p> <p>If <span class="codeph"> progresista</span> se especifica, el visor solo utiliza la reproducción de HTML 5 admitida de forma nativa por los navegadores y reproduce vídeo de forma progresiva en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos automático y progresivo, consulte la Guía del usuario de Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

Se ignora cuando el visor funciona con vídeo externo. Consulte [Compatibilidad con vídeo externo](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
