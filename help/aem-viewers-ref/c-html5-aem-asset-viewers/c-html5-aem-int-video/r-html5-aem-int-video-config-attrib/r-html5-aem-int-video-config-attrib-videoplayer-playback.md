---
title: VideoPlayer.playback
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
TQID: 'https://experienceleague.adobe.com/VnLfO1MI9EIpeoP4fpwMufyy-J2g615LOosZ4hLZlt8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuración para el visualizador de vídeo interactivo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> automático|progresivo</span> </p> </td> 
   <td colname="col2"> <p> Establece el tipo de reproducción que utiliza el visor. </p> <p>Cuando se establece <span class="codeph"> auto</span>, en la mayoría de los navegadores de escritorio y en todos los dispositivos iOS, el visor usa flujo de vídeo HTML5 en formato HLS. Y vuelve a la reproducción progresiva de HTML5 en ciertos sistemas como el antiguo Internet Explorer y Android™. </p> <p>Cuando se establece <span class="codeph"> progressive</span>, el visor solo depende de la reproducción de HTML5 admitida de forma nativa por los navegadores y reproduce vídeo progresivamente en todos los sistemas. </p> <p>Para obtener más información sobre la selección de reproducción en los modos nativo <span class="codeph"> auto</span> y <span class="codeph"> progressive</span>, consulte la Guía del usuario de SDK de visores de HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`auto`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
