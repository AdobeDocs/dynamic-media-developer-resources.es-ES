---
title: VideoPlayer.iconeffect
description: Atributo de configuración para el visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Atributo de configuración para el visor de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`atenuación`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Permite que IconEffect se muestre encima del vídeo cuando este se pone en pausa. En algunos dispositivos se utilizan controles nativos. En tal caso, la variable <span class="codeph"> iconefecto</span> se omite el modificador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica el número máximo de veces que IconEffect aparece y vuelve a aparecer. Un valor de <span class="codeph"> -1</span> indica que el icono vuelve a aparecer indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> atenuación</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica la duración en segundos de la animación de mostrar u ocultar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
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
