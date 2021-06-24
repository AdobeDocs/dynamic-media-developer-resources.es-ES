---
description: FlyoutZoomView.frametransition
solution: Experience Manager
title: FlyoutZoomView.frametransition
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flotante
role: Developer,Business Practitioner
exl-id: 0b0a88a0-d736-4ab8-a25f-15d1689b0a48
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 10%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`duración`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto aplicado a la vista principal al cambiar el recurso. El <span class="codeph"> ninguno</span> significa que no hay transición, el cambio de vista principal se produce instantáneamente. El <span class="codeph"> fundido</span> activa la transición de fundido cruzado donde la imagen antigua se desvanece y la nueva imagen se desvanece </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p> Número de segundos que tarda la animación en completarse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

Ninguno.

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`frametransition=fade,1`
