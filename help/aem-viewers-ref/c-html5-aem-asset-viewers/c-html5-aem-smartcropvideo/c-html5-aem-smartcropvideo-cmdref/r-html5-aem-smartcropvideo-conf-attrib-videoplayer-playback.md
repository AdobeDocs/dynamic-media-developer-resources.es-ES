---
title: SmartCropVideoPlayer.playback
description: Atributo de configuración para el visor de recorte inteligente de vídeos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6df94fe7-30ea-42f1-a39e-50219259a098
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Atributo de configuración para el visor de recorte inteligente de vídeos.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> automático|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Establece el tipo de reproducción que utiliza el visor. Cuando se establece <span class="codeph"> auto</span>, en la mayoría de los navegadores de escritorio y en todos los dispositivos iOS, el visor usa flujo de vídeo HTML5 en formato HLS. Vuelve a la reproducción progresiva de HTML5 en ciertos sistemas como el antiguo Internet Explorer y Android™. </p> <p>Si se especifica <span class="codeph"> progressive</span>, el visor solo depende de la reproducción de HTML5 admitida de forma nativa por los navegadores y reproduce vídeo progresivamente en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos automático y progresivo, consulte la Guía del usuario de Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

Se ignora cuando el visor funciona con vídeo externo. Ver [Compatibilidad con vídeo externo]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
