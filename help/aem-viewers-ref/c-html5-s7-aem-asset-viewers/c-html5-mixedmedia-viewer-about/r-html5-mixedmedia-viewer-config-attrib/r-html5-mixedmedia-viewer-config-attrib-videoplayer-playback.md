---
description: Atributo de configuración para el visualizador de vídeo de medios mixtos.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Developer,Business Practitioner
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuración para el visualizador de vídeo de medios mixtos.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Define el tipo de reproducción que utiliza el visor. Cuando se establece <span class="codeph"> auto</span> , en la mayoría de los navegadores de escritorio y en todos los dispositivos iOS, el visor utiliza vídeo de flujo HTML5 en formato HLS. Vuelve a la reproducción progresiva de HTML5 en determinados sistemas, como Internet Explorer y Android. </p> <p>Si se especifica <span class="codeph"> progresiva</span>, el visor solo se basa en la reproducción HTML5 como lo admiten los navegadores de forma nativa y reproduce vídeo progresivamente en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos automático y progresivo, consulte la Guía del usuario del SDK de visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
