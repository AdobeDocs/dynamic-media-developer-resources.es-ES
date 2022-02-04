---
title: VideoPlayer.posterimage
description: VideoPlayer.posterimage
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> La imagen que se muestra en el primer fotograma antes de que el vídeo empiece a reproducirse, se resuelve con <span class="codeph"> serverurl</span>. Si se especifica en la dirección URL, HTTP codifica lo siguiente: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> como <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> como <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> como <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Si la variable <span class="codeph"><span class="varname"> image_id</span></span> se omite, el componente intenta usar la imagen de póster predeterminada para ese recurso. </p> <p>Cuando el vídeo se especifica como una ruta, el ID de catálogo predeterminado de las imágenes de póster se deriva de la ruta de vídeo como <span class="codeph"> catalog_id/image_id</span> par donde <span class="codeph"> catalog_id</span> corresponde al primer token de la ruta. Y, <span class="codeph"> image_id</span> es el nombre del vídeo con la extensión eliminada. Si la imagen con ese ID no existe, no se muestra la imagen de póster. </p> <p>Para evitar la visualización de la imagen de póster predeterminada, especifique <span class="codeph"> ninguno</span> como valor de imagen de póster. Si solo la variable <span class="codeph"><span class="varname"> isCommands</span></span> , los comandos se aplican a la imagen de póster predeterminada antes de que se muestre la imagen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Ninguno.

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
