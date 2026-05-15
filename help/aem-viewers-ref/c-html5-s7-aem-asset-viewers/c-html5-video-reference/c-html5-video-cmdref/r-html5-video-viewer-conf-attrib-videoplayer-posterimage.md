---
title: VideoPlayer.posterimage
description: Atributo de configuración para el visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
TQID: 'https://experienceleague.adobe.com/W683yWq5ODlrEemGRm-dUsxYIAsAVF8LdsoEOlu3IRw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

Atributo de configuración para el visor de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Imagen que se mostrará en el primer fotograma antes de que comience la reproducción del vídeo, resuelta en <span class="codeph"> serverurl</span>. Si se especifica en la dirección URL, codifique en HTTP lo siguiente: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> como <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> y </span> como <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> como <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Si se omite el valor <span class="codeph"><span class="varname"> image_id</span></span>, el componente intenta usar la imagen de póster predeterminada para ese recurso en su lugar. </p> <p>Cuando el vídeo se especifica como ruta, el ID de catálogo de las imágenes de póster predeterminadas se deriva de la ruta de vídeo como el par <span class="codeph"> catalog_id/image_id</span>, donde <span class="codeph"> catalog_id</span> corresponde al primer token de la ruta. Y <span class="codeph"> image_id</span> es el nombre del vídeo con la extensión eliminada. Si la imagen con ese ID no existe, la imagen del póster no se muestra. </p> <p>Para evitar que se muestre la imagen de póster predeterminada, especifique <span class="codeph"> none</span> como valor de la imagen de póster. Si sólo se especifican los comandos <span class="codeph"><span class="varname"> isCommands</span></span>, los comandos se aplicarán a la imagen de póster predeterminada antes de que se muestre la imagen. </p> </td> 
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
