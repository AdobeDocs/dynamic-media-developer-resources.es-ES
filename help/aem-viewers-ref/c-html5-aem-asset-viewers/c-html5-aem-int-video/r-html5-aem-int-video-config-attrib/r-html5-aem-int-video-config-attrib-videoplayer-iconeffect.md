---
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Developer,User
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 4%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Atributo de configuración para el visualizador de vídeo interactivo.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Habilita el IconEffect para que se muestre sobre el video cuando el video está en estado pausado. En algunos dispositivos se utilizan controles nativos. En estos casos, se ignora el modificador <span class="codeph"> iconeffect</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> contar</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el número máximo de veces que el IconEffect aparece y vuelve a aparecer. Un valor de <span class="codeph"> -1</span> indica que el icono vuelve a aparecer indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fundido</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la duración en segundos de la animación de mostrar u ocultar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Establece el número de segundos que IconEffect permanece totalmente visible antes de que se oculte automáticamente. Es decir, el tiempo después de la atenuación en la animación se completa y antes de que comience la animación de atenuación. Establézcalo en <span class="codeph"> 0</span> para deshabilitar el comportamiento de ocultación automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
