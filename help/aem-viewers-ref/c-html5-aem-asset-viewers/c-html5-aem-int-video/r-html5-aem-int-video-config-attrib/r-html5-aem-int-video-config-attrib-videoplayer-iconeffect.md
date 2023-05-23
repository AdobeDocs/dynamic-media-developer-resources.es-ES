---
title: VideoPlayer.iconeffect
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Atributo de configuración para el visualizador de vídeo interactivo.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *`count`*][, *`atenuación`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Activa el IconEffect que se mostrará encima del vídeo cuando este se encuentra en pausa. En algunos dispositivos se utilizan controles nativos. En tales casos, la <span class="codeph"> iconefecto</span> se omite el modificador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> contar</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el número máximo de veces que IconEffect aparece y vuelve a aparecer. Un valor de <span class="codeph"> -1</span> indica que el icono vuelve a aparecer indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> atenuación</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la duración en segundos de la animación de mostrar u ocultar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Establece el número de segundos que IconEffect permanece totalmente visible antes de ocultarse automáticamente. Es decir, el tiempo después de que se complete la transición en la animación y antes de que comience la animación de desaparición. Configure como. <span class="codeph"> 0</span> para desactivar el comportamiento de ocultar automáticamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
