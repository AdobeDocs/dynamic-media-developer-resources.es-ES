---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 59d71d3b-706f-4f77-8e75-e24c5654f6e3
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`fundido`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Habilita el <span class="codeph"> iconeffect</span> para que se muestre en la parte superior de la imagen cuando esta se encuentra en estado de restablecimiento y se recomienda una acción disponible para interactuar con la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> contar</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el número máximo de veces que se define la variable <span class="codeph"> iconeffect</span> y vuelve a aparecer. Un valor de <span class="codeph"> -1</span> indica que el icono siempre vuelve a aparecer indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fundido</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración de la animación de mostrar u ocultar, en segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Establece el número de segundos que la variable <span class="codeph"> iconeffect</span> permanece totalmente visible antes de que se oculte automáticamente. Es decir, el tiempo después de completar la animación de fundido pero antes de que comience la animación de fundido-out. Una configuración de <span class="codeph"> 0</span> deshabilita el comportamiento de ocultación automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
