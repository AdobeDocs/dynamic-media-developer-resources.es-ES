---
description: nulo
seo-description: nulo
seo-title: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
topic: Dynamic media
uuid: 948b154a-250c-41a8-967b-d199ddb6e5e1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p> Configura el número de acciones de acercamiento y alejamiento necesarias para aumentar o reducir la resolución en un factor de dos. El cambio de resolución de cada acción de zoom es de 2^1 por paso. Establezca en <span class="codeph"> 0</span> para aplicar zoom a resolución completa con una sola acción de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> límite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la resolución máxima de zoom, en relación con la imagen de resolución completa. El valor predeterminado es <span class="codeph"> 1,0</span>, lo que no permite ampliar el zoom más allá de la resolución completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Predeterminado {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## Ejemplo {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
