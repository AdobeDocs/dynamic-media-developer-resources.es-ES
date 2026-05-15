---
title: SmartCropVideoPlayer.iconeffect
description: Atributo de configuración para el visor de recorte inteligente de vídeos.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 369e389c-f0e2-405e-b4aa-2f6b9ac8b8ea
TQID: 'https://experienceleague.adobe.com/xgBGHFv7Zssfc7tbONV97-Tsbvl-Jn5y2oUU8X26dBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 4%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

Atributo de configuración para el visor de recorte inteligente de vídeos.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Permite que IconEffect se muestre encima del vídeo cuando este se pone en pausa. En algunos dispositivos se utilizan controles nativos. En tal caso, se omite el modificador <span class="codeph"> iconeffect</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recuento</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica el número máximo de veces que IconEffect aparece y vuelve a aparecer. Un valor de <span class="codeph"> -1</span> indica que el icono reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fundido</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica la duración en segundos de la animación de mostrar u ocultar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ocultar automáticamente</span> </span> </p> </td> 
   <td colname="col2"> <p> Establece el número de segundos que IconEffect permanece visible antes de ocultarse automáticamente. Es decir, el tiempo después de completar la animación de fundido de entrada y antes de que comience la animación de fundido de salida. Una configuración de <span class="codeph"> 0</span> deshabilita el comportamiento de ocultar automáticamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
