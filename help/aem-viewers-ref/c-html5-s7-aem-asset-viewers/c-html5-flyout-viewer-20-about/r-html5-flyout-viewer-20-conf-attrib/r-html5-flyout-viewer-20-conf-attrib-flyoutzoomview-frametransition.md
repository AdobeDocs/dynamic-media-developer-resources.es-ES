---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 0b0a88a0-d736-4ab8-a25f-15d1689b0a48
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`duración`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|fundido</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo del efecto aplicado a la vista principal cuando cambia el recurso. <span class="codeph"> none</span> significa que no hay transición; el cambio de la vista principal se produce de forma inmediata. La transición de fundido <span class="codeph"></span> activa una transición de fundido cruzado en la que la imagen antigua desaparece y la nueva aparece </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p> Número de segundos necesarios para completar la animación. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

Ninguno.

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`frametransition=fade,1`
