---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`duration`*[, *`espaciado`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|diapositiva </span> </p> </td> 
   <td colname="col2"> <p>Especifica el tipo del efecto aplicado al cambiar el marco. El atributo <span class="codeph"> ninguno </span> significa que no hay transición; el cambio de fotograma se produce instantáneamente. El atributo <span class="codeph"> fundido </span> significa transición de fundido cruzado entre marcos antiguos y nuevos. El atributo <span class="codeph"> diapositiva </span> activa la transición en la que el marco antiguo se desliza fuera de la vista y el nuevo marco se desliza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración (en segundo lugar) de <span class="codeph"> fundido </span> o <span class="codeph"> diapositiva </span> efecto de transición. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espaciado </span> </span> </p> </td> 
   <td colname="col2"> <p>El espaciado entre fotogramas adyacentes en <span class="codeph"> diapositiva </span> transición, tiene el rango de <span class="codeph"> 0 </span> hasta <span class="codeph"> 1 </span> y es relativo al ancho del componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

Ninguno.

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
