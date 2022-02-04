---
title: VideoPlayer.preload
description: Indica si el visor empieza a cargar contenido de vídeo antes de que se inicie la reproducción.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 90fb988a-255c-46fe-b05a-39c95ae8b95d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---

# VideoPlayer.preload{#videoplayer-preload}

Indica si el visor empieza a cargar contenido de vídeo antes de que se inicie la reproducción.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Si está configurado como <span class="codeph"> 1 </span> el vídeo empieza a descargarse justo después de que se haya configurado el recurso; de lo contrario, la precarga solo se inicia después de que el usuario final o una llamada a la API inicien la reproducción. </p> <p>Si está configurado como <span class="codeph"> 0 </span> es posible que determinadas funciones no funcionen hasta que se inicie la reproducción; específicamente, la operación de búsqueda no actualiza el fotograma de vídeo. Si la imagen de póster está desactivada, el visor se muestra como un área vacía en lugar del primer fotograma de vídeo. </p> <p>La desactivación de la precarga de vídeo puede ignorarse en determinadas versiones de los navegadores Internet Explorer 11 y Edge 11. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
