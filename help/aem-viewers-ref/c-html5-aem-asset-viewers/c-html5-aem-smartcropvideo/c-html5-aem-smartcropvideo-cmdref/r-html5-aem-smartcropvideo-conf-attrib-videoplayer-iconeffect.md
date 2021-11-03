---
title: SmartCropVideoPlayer.iconeffect
description: Atributo de configuración para el visor de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

Atributo de configuración para el visor de vídeo de recorte inteligente.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`fundido`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Habilita IconEffect para que se muestre sobre el vídeo cuando este está en pausa. En algunos dispositivos se utilizan controles nativos. En tal caso, la variable <span class="codeph"> iconeffect</span> se ignora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica el número máximo de veces que el IconEffect aparece y vuelve a aparecer. Un valor de <span class="codeph"> -1</span> indica que el icono vuelve a aparecer indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fundido</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica la duración en segundos de la animación de mostrar u ocultar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Establece el número de segundos que el IconEffect permanece visible antes de que se oculte automáticamente. Es decir, el tiempo después de finalizar la animación de fundido y antes de que comience la animación de fundido-out. Una configuración de <span class="codeph"> 0</span> deshabilita el comportamiento de ocultación automática. </p> </td> 
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
