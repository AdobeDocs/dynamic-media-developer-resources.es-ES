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
ht-degree: 5%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_53A26E1617CB411B9586203CB9AA1AB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ninguno|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación del clic/toque en la activación o desactivación de reproducción/pausa. Si se establece en <span class="codeph"> none</span>, se deshabilita el clic/toque en la reproducción/pausa. Si se establece en <span class="codeph"> playPause</span>, hacer clic en el vídeo cambia entre reproducir y pausar. En algunos dispositivos, puede utilizar controles nativos. En tal caso, el comportamiento <span class="codeph"> singleclick</span> está deshabilitado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`playPause`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=none`
