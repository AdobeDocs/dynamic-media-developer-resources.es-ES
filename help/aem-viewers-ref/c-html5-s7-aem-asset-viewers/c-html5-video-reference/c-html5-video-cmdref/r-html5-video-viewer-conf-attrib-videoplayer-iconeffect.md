---
description: Atributo de configuración para el visualizador de vídeo.
seo-description: Atributo de configuración para el visualizador de vídeo.
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
uuid: 1ba6f24a-77bb-41ef-a831-a7ac817abd73
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Atributo de configuración para el visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Habilita IconEffect para que se muestre sobre el vídeo cuando este está en pausa. En algunos dispositivos se utilizan controles nativos. En este caso, se ignora el modificador <span class="codeph"> iconeffect</span>. </p> </td> 
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
   <td colname="col2"> <p> Establece el número de segundos que el IconEffect permanece visible antes de que se oculte automáticamente. Es decir, el tiempo después de finalizar la animación de fundido y antes de que comience la animación de fundido-out. Un valor de <span class="codeph"> 0</span> deshabilita el comportamiento de ocultación automática. </p> </td> 
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

