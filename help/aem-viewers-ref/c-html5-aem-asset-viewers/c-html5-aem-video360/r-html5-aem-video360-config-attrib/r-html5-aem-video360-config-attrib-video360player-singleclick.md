---
title: Video360Player.singleclick
description: Atributo de configuración para el visualizador de vídeo360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 11%

---

# Video360Player.singleclick{#video-player-singleclick}

Atributo de configuración para el visualizador de vídeo360.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un toque o clic para alternar la reproducción/pausa. Si se establece en <span class="codeph"> ninguno</span> , se deshabilita el toque o clic único para reproducir/pausar. Si se establece en <span class="codeph"> playPause</span>, al seleccionar el vídeo, se alternan entre la reproducción y la pausa del vídeo. En algunos dispositivos, puede utilizar controles nativos. En este caso, se desactiva un comportamiento <span class="codeph"> singleclick</span>. </p> </td> 
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
