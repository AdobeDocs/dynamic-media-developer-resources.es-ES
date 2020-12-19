---
description: nulo
seo-description: nulo
seo-title: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic media
uuid: 28663f44-11cb-4522-bd12-d6bec17b4173
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> La imagen que se muestra en el primer fotograma antes de que se reproduzcan los inicios de vídeo, se resuelve con <span class="codeph"> serverurl</span>. Si se especifica en la dirección URL, codificar HTTP lo siguiente: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> como  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> como  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Si se omite el valor <span class="codeph"><span class="varname"> image_id</span></span>, el componente intentará usar la imagen de póster predeterminada para ese recurso. </p> <p>Cuando el vídeo se especifica como una ruta, la identificación predeterminada del catálogo de imágenes de póster se deriva de la ruta de vídeo como el par <span class="codeph"> catalog_id/image_id</span> donde <span class="codeph"> catalog_id</span> corresponde al primer token de la ruta y <span class="codeph"> image_id</span> es el nombre del vídeo con la extensión eliminada. Si la imagen con ese ID no existe, no se muestra la imagen del póster. </p> <p>Para evitar que se muestre la imagen de póster predeterminada, especifique <span class="codeph"> none</span> como valor de imagen de póster. Si solo se especifica <span class="codeph"><span class="varname"> isCommands</span></span>, los comandos se aplican a la imagen de póster predeterminada antes de que se muestre la imagen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Ninguno.

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
