---
description: Atributo de configuración para el visualizador de vídeo360.
seo-description: Atributo de configuración para el visualizador de vídeo360.
seo-title: Video360Player.singleclick
solution: Experience Manager
title: Video360Player.singleclick
uuid: 2972405c-5c89-45d0-a542-19c7463901b4
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 11%

---


# Video360Player.singleclick{#video-player-singleclick}

Atributo de configuración para el visualizador de vídeo360.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

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

