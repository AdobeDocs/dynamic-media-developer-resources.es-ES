---
title: VideoPlayer.playback
description: Atributo de configuración para el visualizador de vídeos de medios mixtos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuración para el visualizador de vídeos de medios mixtos.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Establece el tipo de reproducción que utiliza el visor. Cuándo <span class="codeph"> auto</span> está configurado; en la mayoría de los navegadores de escritorio y en todos los dispositivos iOS, el visor utiliza flujo de vídeo HTML5 en formato HLS. Vuelve a la reproducción progresiva de HTML 5 en ciertos sistemas como el antiguo Internet Explorer y Android™. </p> <p>If <span class="codeph"> progresista</span> se especifica, el visor solo utiliza la reproducción de HTML 5 admitida de forma nativa por los navegadores y reproduce vídeo de forma progresiva en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos automático y progresivo, consulte la Guía del usuario de Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
