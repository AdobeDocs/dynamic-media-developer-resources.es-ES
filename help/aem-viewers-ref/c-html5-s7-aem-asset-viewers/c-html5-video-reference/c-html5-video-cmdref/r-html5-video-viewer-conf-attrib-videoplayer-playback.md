---
description: Atributo de configuración para el visualizador de vídeo.
seo-description: Atributo de configuración para el visualizador de vídeo.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
uuid: 5ab7a322-9de0-4a26-95be-b9b2ff8e5a84
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuración para el visualizador de vídeo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Define el tipo de reproducción que utiliza el visor. Cuando se establece <span class="codeph"> auto</span> , en la mayoría de los navegadores de escritorio y en todos los dispositivos iOS, el visor utiliza vídeo de flujo HTML5 en formato HLS. Vuelve a la reproducción progresiva de HTML5 en determinados sistemas, como Internet Explorer y Android. </p> <p>Si se especifica <span class="codeph"> progresiva</span>, el visor solo se basa en la reproducción HTML5 como lo admiten los navegadores de forma nativa y reproduce vídeo progresivamente en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos automático y progresivo, consulte la Guía del usuario del SDK de visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

Se omite cuando el visor trabaja con vídeo externo. Consulte [Compatibilidad con vídeo externo](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

