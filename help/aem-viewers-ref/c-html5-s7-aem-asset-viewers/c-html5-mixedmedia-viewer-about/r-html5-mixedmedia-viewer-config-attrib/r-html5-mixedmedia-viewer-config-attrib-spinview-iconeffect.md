---
title: SpinView.iconeffect
description: SpinView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 473207d2-7e26-4ea3-940e-5a21f29a2b91
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *`count`*][, *`fundido`*][, *`autoHide`*]`

<table id="table_DF2137DF9C7441B381D2B03CEE4B880A"> 
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

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
