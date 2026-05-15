---
title: VideoPlayer.preload
description: Indica si el visualizador comienza a cargar contenido de vídeo antes de que comience la reproducción.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
TQID: 'https://experienceleague.adobe.com/rFRl01K5HvqAfCruY5lf9p-x-K2sujtT4xppeVw-7xA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# VideoPlayer.preload{#videoplayer-preload}

Indica si el visualizador comienza a cargar contenido de vídeo antes de que comience la reproducción.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Si se establece en <span class="codeph"> 1 </span>, el vídeo comienza a descargarse justo después de configurar el recurso; de lo contrario, la carga previa solo se inicia después de que el usuario final o una llamada de API inicien la reproducción. </p> <p>Si se establece en <span class="codeph"> 0 </span>, es posible que algunas características no funcionen hasta que comience la reproducción; en concreto, la operación de búsqueda no actualiza el fotograma de vídeo. Si la imagen de póster está desactivada, el visor se muestra como un área vacía en lugar del primer fotograma de vídeo. </p> <p>La desactivación de la precarga de vídeo puede ignorarse en determinadas versiones de Internet Explorer 11 y de los navegadores Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
