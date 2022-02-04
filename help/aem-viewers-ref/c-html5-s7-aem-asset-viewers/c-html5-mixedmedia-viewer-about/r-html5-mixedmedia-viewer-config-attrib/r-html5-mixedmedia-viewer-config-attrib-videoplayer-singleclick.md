---
title: VideoPlayer.singleclick
description: VideoPlayer.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2ec6d871-05d9-4d85-b031-e64386f5d2e9
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_53A26E1617CB411B9586203CB9AA1AB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de un toque o clic para alternar la reproducción/pausa. Establecer en <span class="codeph"> ninguno</span> deshabilita el toque o clic único para reproducir/pausar. Si está configurado como <span class="codeph"> playPause</span>, al hacer clic en el vídeo, se alternan entre la reproducción y la pausa del vídeo. En algunos dispositivos, puede utilizar controles nativos. En tal caso, <span class="codeph"> singleclick</span> está desactivado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`playPause`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=none`
