---
description: nulo
seo-description: nulo
seo-title: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic media
uuid: 42bbef39-36b6-4f1d-a228-0aaf107600a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica el número de segundos que se muestra el texto de sugerencia antes de que se oculte. Cuando se establece en <span class="codeph"> -1</span>, el mensaje siempre se muestra, incluso si el usuario activa el menú flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica el número de veces que se muestra el texto al ver imágenes nuevas en el conjunto. Un valor de <span class="codeph"> -1</span> significa que el texto siempre se muestra al ver cualquier imagen del conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fundido</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración de una animación de fundido que se produce cuando el texto aparece o desaparece. Un valor de <span class="codeph"> 0</span> significa que no hay transición de fundido. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
