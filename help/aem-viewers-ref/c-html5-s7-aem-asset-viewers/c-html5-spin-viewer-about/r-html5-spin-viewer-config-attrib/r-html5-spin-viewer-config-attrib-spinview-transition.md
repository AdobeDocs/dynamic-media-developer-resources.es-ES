---
title: SpinView.transition
description: SpinView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 85dbd5cd-b212-4c77-8f5a-ffbdaca27fdb
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`time`*[, *`flexibilización`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tiempo</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos que tarda la animación para una acción de un solo paso de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> flexibilización</span></span> </p> </td> 
   <td colname="col2"> <p> Crea una ilusión de aceleración o deceleración que hace que la transición parezca más natural. Puede definir la flexibilización en una de las siguientes opciones: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (automático) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (lineal) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (cuadrático) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cúbico) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (en cuarentena) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintic) </li> 
     </ul> </p> <p>El modo automático siempre utiliza la transición lineal cuando el zoom elástico está desactivado (predeterminado). De lo contrario, se ajusta a una de las demás funciones de flexibilización en función del tiempo de transición. Es decir, cuanto más corto sea el tiempo de transición, más alta será la función de aceleración utilizada para acelerar el efecto de aceleración o desaceleración. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`0.5,0`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`transition=2,2`
