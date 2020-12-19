---
description: Indica si el visor empieza a cargar contenido de vídeo antes de que se inicio la reproducción.
seo-description: Indica si el visor empieza a cargar contenido de vídeo antes de que se inicio la reproducción.
seo-title: VideoPlayer.preload
solution: Experience Manager
title: VideoPlayer.preload
topic: Dynamic media
uuid: 2aaae96d-d42d-4984-aec9-86e06b3c711c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# VideoPlayer.preload{#videoplayer-preload}

Indica si el visor empieza a cargar contenido de vídeo antes de que se inicio la reproducción.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Si se establece en <span class="codeph"> 1 </span>, el vídeo empieza a descargarse inmediatamente después de que se haya configurado el recurso; de lo contrario, cargue los inicios previamente solo después de que el usuario final o una llamada de API inicien la reproducción. </p> <p>Si se establece en <span class="codeph"> 0 </span>, es posible que determinadas funciones no funcionen hasta que se inicio la reproducción; específicamente, la operación de búsqueda no actualizará el fotograma de vídeo. Si la imagen de póster está desactivada, el visor se muestra como un área vacía en lugar del primer fotograma de vídeo. </p> <p>Tenga en cuenta que la desactivación de la carga previa de vídeo puede omitirse en determinadas versiones de los exploradores Internet Explorer 11 y Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
