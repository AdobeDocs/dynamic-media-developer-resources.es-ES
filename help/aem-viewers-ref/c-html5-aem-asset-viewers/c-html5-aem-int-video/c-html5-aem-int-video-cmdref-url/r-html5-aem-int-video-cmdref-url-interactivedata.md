---
title: interactivedata
description: Comando de URL para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# interactivedata{#interactivedata}

Comando de URL para el visualizador de vídeo interactivo.

`interactivedata= *`archivo`*`

Los datos interactivos asocian ciertas regiones horarias del contenido del vídeo con los datos del producto que se muestran posteriormente en muestras interactivas junto al vídeo. También está asociado en el panel call-to-action que se muestra al final de la reproducción del vídeo. También proporciona un título para el vídeo interactivo que se muestra en el panel call-to-action.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> archivo</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica la dirección URL o la ruta al contenido de datos interactivo WebVTT. El archivo WebVTT debe servirlo el servicio de imágenes. </p> </td> 
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
