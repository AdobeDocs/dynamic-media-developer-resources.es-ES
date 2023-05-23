---
title: SmartCropVideoPlayer.preload
description: Indica si el visualizador comienza a cargar contenido de vídeo antes de que comience la reproducción.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7a83a02e-7b75-4f15-b8c1-aa7b64e6d3bd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

Indica si el visualizador comienza a cargar contenido de vídeo antes de que comience la reproducción.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Si se establece en <span class="codeph"> 1 </span> el vídeo comienza a descargarse justo después de configurar el recurso; de lo contrario, la carga previa solo se inicia después de que el usuario final o una llamada de API inicien la reproducción. </p> <p>Si se establece en <span class="codeph"> 0 </span> es posible que algunas funciones no funcionen hasta que se vuelva a iniciar la reproducción; en concreto, la operación de búsqueda no actualiza el fotograma de vídeo. Si la imagen de póster está desactivada, el visor se muestra como un área vacía en lugar del primer fotograma de vídeo. </p> <p>La desactivación de la precarga de vídeo se puede ignorar en ciertas versiones de Internet Explorer 11 y los navegadores Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
