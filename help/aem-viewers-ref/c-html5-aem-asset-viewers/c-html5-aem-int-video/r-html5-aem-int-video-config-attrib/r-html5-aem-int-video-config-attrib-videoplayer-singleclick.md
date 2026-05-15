---
title: VideoPlayer.singleclick
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
TQID: 'https://experienceleague.adobe.com/Vg05yIAO5E-vWvJdcuQTR0hHQjO9ZNJ2-jJXckvUxxs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 72
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Atributo de configuración para el visualizador de vídeo interactivo.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación del clic/toque en la activación o desactivación de reproducción/pausa. Si se establece en <span class="codeph"> none</span>, se deshabilita el clic/toque en la reproducción/pausa. Si se establece en <span class="codeph"> playPause</span>, al seleccionar el vídeo se alternará entre reproducir y pausar. En algunos dispositivos, puede utilizar controles nativos. En este caso, se deshabilita un comportamiento <span class="codeph"> singleclick</span>. </p> </td> 
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
