---
description: Atributo de configuración para el visor de vídeo interactivo.
seo-description: Atributo de configuración para el visor de vídeo interactivo.
seo-title: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic media
uuid: 6b21179c-a227-4194-8640-0fcf73ee80e9
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

Atributo de configuración para el visor de vídeo interactivo.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> La imagen que se mostrará en el primer fotograma antes de que se reproduzcan los inicios de vídeo, se resolverá con <span class="codeph"> serverurl</span>. Si se especifica en la dirección URL, codificar HTTP lo siguiente: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> como <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> como <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> como <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Si se omite el <span class="codeph"><span class="varname"> valor image_id</span></span> , el componente intentará utilizar la imagen de póster predeterminada para ese recurso. </p> <p>Cuando el vídeo se especifica como una ruta, el ID de catálogo de imágenes de póster predeterminado se deriva de la ruta del vídeo como el par <span class="codeph"> catalog_id/image_id</span> , donde <span class="codeph"> catalog_id</span> corresponde al primer token de la ruta y <span class="codeph"> image_id</span> es el nombre del vídeo con la extensión eliminada. Si la imagen con ese ID no existe, no se muestra la imagen del póster. </p> <p>Para evitar que se muestre la imagen de póster predeterminada, especifique <span class="codeph"> ninguno</span> como valor de imagen de póster. Si solo se especifica <span class="codeph"><span class="varname"> isCommands</span></span> , los comandos se aplican a la imagen de póster predeterminada antes de que se muestre la imagen. </p> </td> 
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

