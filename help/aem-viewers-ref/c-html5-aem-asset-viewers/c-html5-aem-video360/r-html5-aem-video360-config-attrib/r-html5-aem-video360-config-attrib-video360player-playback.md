---
description: Atributo de configuración para el visualizador de vídeo360.
solution: Experience Manager
title: Video360Player.playback
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---


# Video360Player.playback{#video-player-playback}

Atributo de configuración para el visualizador de vídeo360.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Define el tipo de reproducción que utiliza el visor. </p> <p>Cuando se establece <span class="codeph"> auto</span>, en la mayoría de los navegadores de escritorio y en todos los dispositivos iOS el visor utiliza vídeo de flujo HTML5 en formato HLS y vuelve a la reproducción HTML5 progresiva en determinados sistemas, como Internet Explorer y Android antiguos. </p> <p>Cuando se establece <span class="codeph"> progresivo</span>, el visor solo se basa en la reproducción HTML5 como lo admiten los navegadores de forma nativa y reproduce vídeo de forma progresiva en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos nativo <span class="codeph"> auto</span> y <span class="codeph"> progresivo</span>, consulte la Guía del usuario del SDK de visores HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional. Se omite cuando el visor trabaja con vídeo externo.

Consulte [Compatibilidad con vídeo externo](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) para obtener más información.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`auto`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
