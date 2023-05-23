---
title: Video360Player.preload
description: Indica si el visualizador comienza a cargar contenido de vídeo antes de que comience la reproducción.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# Video360Player.preload{#video-player-preload}

Indica si el visualizador comienza a cargar contenido de vídeo antes de que comience la reproducción.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Si se establece en <span class="codeph"> 1 </span>, el vídeo comienza a descargarse justo después de configurar el recurso. De lo contrario, la carga previa solo se inicia después de que el usuario final o una llamada a la API inicien la reproducción. </p> <p>Si se establece en <span class="codeph"> 0 </span>Sin embargo, es posible que algunas funciones no funcionen hasta que comience la reproducción. En concreto, la operación de búsqueda no actualiza el fotograma de vídeo. Si la imagen de póster está desactivada, el visor se muestra como un área vacía en lugar del primer fotograma de vídeo. </p> <p>La desactivación de la precarga de vídeo se puede ignorar en ciertas versiones de Internet Explorer 11 y los navegadores Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
