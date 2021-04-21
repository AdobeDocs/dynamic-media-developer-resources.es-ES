---
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Atributo de configuración para el visualizador de vídeo interactivo.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un toque o clic para alternar la reproducción/pausa. Si se establece en <span class="codeph"> ninguno</span> , se deshabilita el toque o clic único para reproducir/pausar. Si se establece en <span class="codeph"> playPause</span>, al hacer clic en el vídeo se alternan entre la reproducción y la pausa del vídeo. En algunos dispositivos puede utilizar controles nativos. En este caso, se desactiva un comportamiento <span class="codeph"> singleclick</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`playPause`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
