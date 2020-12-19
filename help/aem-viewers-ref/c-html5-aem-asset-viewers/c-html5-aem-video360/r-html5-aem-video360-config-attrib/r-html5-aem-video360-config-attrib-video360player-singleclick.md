---
description: Atributo de configuración para el visor de Video360.
seo-description: Atributo de configuración para el visor de Video360.
seo-title: Video360Player.singleclick
solution: Experience Manager
title: Video360Player.singleclick
topic: Dynamic media
uuid: 2972405c-5c89-45d0-a542-19c7463901b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 12%

---


# Video360Player.singleclick{#video-player-singleclick}

Atributo de configuración para el visor de Video360.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un solo clic o toque para alternar la reproducción y la pausa. Si se establece en <span class="codeph"> none</span> deshabilita el toque o clic único para reproducir/pausa. Si se establece en <span class="codeph"> playPause</span>, al hacer clic en el vídeo se alternará entre la reproducción y la pausa del vídeo. En algunos dispositivos puede utilizar controles nativos. En este caso, se desactiva el comportamiento <span class="codeph"> singleclick</span>. </p> </td> 
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

