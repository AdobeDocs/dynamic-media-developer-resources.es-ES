---
title: SmartCropVideoPlayer.posterimage
description: Atributo de configuración para el visor de recorte inteligente de vídeos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ff4f8e2c-b9c3-4fba-b3f0-fa1eaddcd8c0
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

Atributo de configuración para el visor de recorte inteligente de vídeos.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Imagen que se mostrará en el primer fotograma antes de que comience la reproducción del vídeo, resuelta con <span class="codeph"> serverurl</span>. Si se especifica en la dirección URL, codifique en HTTP lo siguiente: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Si la variable <span class="codeph"><span class="varname"> image_id</span></span> Si el valor se omite, el componente intenta utilizar la imagen de póster predeterminada para ese recurso. </p> <p>Cuando el vídeo se especifica como una ruta, el ID de catálogo de las imágenes de póster predeterminado se deriva de la ruta de vídeo como <span class="codeph"> catalog_id/image_id</span> par. El <span class="codeph"> catalog_id</span> corresponde al primer token de la ruta y <span class="codeph"> image_id</span> es el nombre del vídeo sin la extensión. Si la imagen con ese ID no existe, la imagen del póster no se muestra. </p> <p>Para evitar que se muestre la imagen de póster predeterminada, especifique <span class="codeph"> ninguno</span> como valor de la imagen del póster. Si solo el <span class="codeph"><span class="varname"> isCommands</span></span> Si se especifican, los comandos se aplican a la imagen de póster predeterminada antes de que se muestre la imagen. </p> </td> 
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
