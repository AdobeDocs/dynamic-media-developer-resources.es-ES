---
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Developer,Business Practitioner
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuración para el visualizador de vídeo interactivo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Define el tipo de reproducción que utiliza el visor. </p> <p>Cuando se establece <span class="codeph"> auto</span>, en la mayoría de los navegadores de escritorio y en todos los dispositivos iOS el visor utiliza vídeo de flujo HTML5 en formato HLS y vuelve a la reproducción HTML5 progresiva en determinados sistemas, como Internet Explorer y Android antiguos. </p> <p>Cuando se establece <span class="codeph"> progresivo</span>, el visor solo se basa en la reproducción HTML5 como lo admiten los navegadores de forma nativa y reproduce vídeo de forma progresiva en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos nativo <span class="codeph"> auto</span> y <span class="codeph"> progresivo</span>, consulte la Guía del usuario del SDK de visores HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`auto`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
