---
description: Atributo de configuración para el visor de vídeo interactivo.
seo-description: Atributo de configuración para el visor de vídeo interactivo.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 2576f433-b9c2-4da1-9a51-f66b71d5df99
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuración para el visor de vídeo interactivo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Define el tipo de reproducción que utiliza el visor. </p> <p>Cuando se establece <span class="codeph"> auto</span>, en la mayoría de los exploradores de escritorio y en todos los dispositivos iOS el visor utiliza vídeo de flujo HTML5 en formato HLS y vuelve a la reproducción progresiva de HTML5 en determinados sistemas como Internet Explorer y Android. </p> <p>Cuando <span class="codeph"> progresivo</span> está establecido, el visor solo se basa en la reproducción HTML5 como admitida de forma nativa por los navegadores y reproduce vídeo de forma progresiva en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos <span class="codeph"> auto</span> y <span class="codeph"> progresivo</span> nativos, consulte la Guía del usuario del SDK de visores HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`auto`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
