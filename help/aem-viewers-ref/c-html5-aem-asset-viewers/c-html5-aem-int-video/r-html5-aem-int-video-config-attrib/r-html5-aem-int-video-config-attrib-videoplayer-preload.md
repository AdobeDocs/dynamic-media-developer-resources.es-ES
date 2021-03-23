---
description: Indica si el visor empieza a cargar contenido de vídeo antes de que se inicie la reproducción.
seo-description: Indica si el visor empieza a cargar contenido de vídeo antes de que se inicie la reproducción.
seo-title: VideoPlayer.preload
solution: Experience Manager
title: VideoPlayer.preload
uuid: d080465d-7349-4671-aaa4-c49e549d1f64
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 3%

---


# VideoPlayer.preload{#videoplayer-preload}

Indica si el visor empieza a cargar contenido de vídeo antes de que se inicie la reproducción.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Si se establece en <span class="codeph"> 1 </span> el vídeo empieza a descargarse justo después de que se haya configurado el recurso; de lo contrario, la precarga solo se inicia después de que el usuario final o una llamada a la API inicien la reproducción. </p> <p>Si se establece en <span class="codeph"> 0 </span>, es posible que determinadas funciones no funcionen hasta que se inicie la reproducción; específicamente, la operación de búsqueda no actualizará el fotograma de vídeo. Si la imagen de póster está desactivada, el visor se muestra como un área vacía en lugar del primer fotograma de vídeo. </p> <p>Tenga en cuenta que la desactivación de la precarga de vídeo puede ignorarse en determinadas versiones de los navegadores Internet Explorer 11 y Edge 11. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
