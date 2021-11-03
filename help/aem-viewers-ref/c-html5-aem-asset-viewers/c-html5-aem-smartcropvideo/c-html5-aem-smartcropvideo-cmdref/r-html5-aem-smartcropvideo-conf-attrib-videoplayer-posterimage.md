---
title: SmartCropVideoPlayer.posterimage
description: Atributo de configuración para el visor de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

Atributo de configuración para el visor de vídeo de recorte inteligente.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> La imagen que se muestra en el primer fotograma antes de que el vídeo empiece a reproducirse, se resuelve con <span class="codeph"> serverurl</span>. Si se especifica en la dirección URL, HTTP codifica lo siguiente: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> como <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> como <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> como <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Si la variable <span class="codeph"><span class="varname"> image_id</span></span> se omite, el componente intenta usar la imagen de póster predeterminada para ese recurso. </p> <p>Cuando el vídeo se especifica como una ruta, el id de catálogo predeterminado de las imágenes de póster se deriva de la ruta de vídeo como <span class="codeph"> catalog_id/image_id</span> par. La variable <span class="codeph"> catalog_id</span> corresponde al primer token de la ruta y <span class="codeph"> image_id</span> es el nombre del vídeo con la extensión eliminada. Si la imagen con ese ID no existe, no se muestra la imagen de póster. </p> <p>Para evitar la visualización de la imagen de póster predeterminada, especifique <span class="codeph"> ninguno</span> como valor de imagen de póster. Si solo la variable <span class="codeph"><span class="varname"> isCommands</span></span> , los comandos se aplican a la imagen de póster predeterminada antes de que se muestre la imagen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

Ninguno.

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
