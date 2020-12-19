---
description: Atributo de configuración para el visor de vídeo de medios mixtos.
seo-description: Atributo de configuración para el visor de vídeo de medios mixtos.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuración para el visor de vídeo de medios mixtos.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Define el tipo de reproducción que utiliza el visor. Cuando <span class="codeph"> auto</span> está establecido, en la mayoría de los exploradores de escritorio y en todos los dispositivos iOS, el visor utiliza vídeo de flujo HTML5 en formato HLS. Vuelve a la reproducción progresiva de HTML5 en determinados sistemas como Internet Explorer y Android. </p> <p>Si se especifica <span class="codeph"> progresivo</span>, el visor solo se basa en la reproducción de HTML5 como admitida de forma nativa por los navegadores y reproduce vídeo de forma progresiva en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos automático y progresivo, consulte la Guía del usuario del SDK de visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
