---
title: ZoomView.transition
description: ZoomView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f1b4faa3-14d1-4eef-acc2-214c7be4a5ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`tiempo`*[, *`aliviando`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> vez</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos que tarda la animación para una única acción de paso de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> aliviando</span></span> </p> </td> 
   <td colname="col2"> <p> Crea una ilusión de aceleración o desaceleración que hace que la transición parezca más natural. Puede establecer la aceleración en una de las siguientes opciones: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (automático) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (lineal) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (cuadrático) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cúbico) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (cuártico) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quíntico) </li> 
     </ul> </p> <p>El modo automático siempre utiliza una transición lineal cuando el zoom elástico está desactivado (predeterminado). De lo contrario, se ajusta a una de las otras funciones de aceleración en función del tiempo de transición. Es decir, cuanto más corto sea el tiempo de transición, mayor será la función de aceleración utilizada para acelerar el efecto de aceleración o desaceleración. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`0.5,0`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`transition=2,2`
