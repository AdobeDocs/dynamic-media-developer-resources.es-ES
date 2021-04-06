---
description: Atributo de configuración para el visualizador de vídeo360.
solution: Experience Manager
title: Video360Player.posterimage
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Desarrollador, profesional empresarial
exl-id: fffd0976-0aeb-4e61-981f-b84e9076f35f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 11%

---

# Video360Player.posterimage{#video-player-posterimage}

Atributo de configuración para el visualizador de vídeo360.

` [Video360Player.|<containerId>_video360Player.]posterimage=none|[? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Modificadores del servicio de imágenes que controlan el aspecto de la imagen del póster. Si se especifica en la dirección URL, HTTP codifica lo siguiente: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> como  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> como  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> como  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p> Este modificador funciona para el contenido de vídeo alojado en Dynamic Media Classic o AEM Dynamic Media. </p> <p>Para evitar que se muestre la imagen de póster predeterminada, especifique <span class="codeph"> none</span> como valor de imagen de póster. </p> </td> 
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
