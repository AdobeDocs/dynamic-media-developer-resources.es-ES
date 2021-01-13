---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
topic: Dynamic media
uuid: f84da456-ac02-4037-b1fd-7440823eb1ef
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *``*[, *`aceleración de tiempo`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tiempo</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos que dura la animación de una sola acción de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> flexibilización</span></span> </p> </td> 
   <td colname="col2"> <p> Crea una ilusión de aceleración o deceleración que hace que la transición parezca más natural. Puede definir la aceleración en una de las siguientes opciones: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (automático) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (lineal) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (cuadrático) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cúbico) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (en cuarto) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintic) </li> 
     </ul> </p> <p>El modo automático siempre utiliza transición lineal cuando el zoom elástico está desactivado (predeterminado). De lo contrario, se ajusta a una de las demás funciones de aceleración en función del tiempo de transición. Es decir, cuanto más corto sea el tiempo de transición, más alta será la función de aceleración que se utilizará para acelerar el efecto de aceleración o desaceleración. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-ebfd9162c8504666bf0e4485bf3b1383}

Opcional.

## Predeterminado {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## Ejemplo {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
