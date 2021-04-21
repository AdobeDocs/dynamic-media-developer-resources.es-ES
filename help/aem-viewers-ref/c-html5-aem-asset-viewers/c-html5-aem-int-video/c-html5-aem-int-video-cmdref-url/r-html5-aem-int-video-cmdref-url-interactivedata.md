---
description: URL para el visualizador de vídeo interactivo.
solution: Experience Manager
title: interactivedata
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 5%

---

# interactivedata{#interactivedata}

URL para el visualizador de vídeo interactivo.

`interactivedata= *`archivo`*`

Los datos interactivos asocian ciertas regiones horarias del contenido del vídeo con los datos del producto que luego se muestran en muestras interactivas junto al vídeo. También está asociado al panel de llamada a la acción que se muestra al finalizar la reproducción de vídeo. También proporciona un título para el vídeo interactivo que se muestra en el panel de llamada a la acción.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una dirección URL o ruta al contenido de datos interactivo de WebVTT. El archivo WebVTT debe ser servido por Image Serving. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

Ninguno.

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
