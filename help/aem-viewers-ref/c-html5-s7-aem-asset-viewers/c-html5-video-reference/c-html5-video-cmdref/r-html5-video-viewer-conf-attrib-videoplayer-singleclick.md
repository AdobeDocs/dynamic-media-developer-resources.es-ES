---
title: VideoPlayer.singleclick
description: Atributo de configuración para el visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
TQID: 'https://experienceleague.adobe.com/RH1L9ADikh3LiDMwfqDdrGOZ7L08nRyFgIly2yCKZf4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Atributo de configuración para el visor de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ninguno|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación del clic/toque en la activación o desactivación de reproducción/pausa. Si se establece en <span class="codeph"> none</span>, se deshabilita el clic/toque en la reproducción/pausa. Si se establece en <span class="codeph"> playPause</span>, hacer clic en el vídeo cambia entre reproducir y pausar. En algunos dispositivos, puede utilizar controles nativos. En tal caso, el comportamiento <span class="codeph"> singleclick</span> está deshabilitado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
