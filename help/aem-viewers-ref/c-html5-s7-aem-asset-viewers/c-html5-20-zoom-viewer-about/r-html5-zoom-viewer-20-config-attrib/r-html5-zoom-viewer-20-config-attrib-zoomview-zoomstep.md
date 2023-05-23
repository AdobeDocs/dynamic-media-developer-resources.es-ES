---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bcd153f3-7a87-4e8f-825b-fc4a136de1dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`escalón`*[, *`límite`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> paso</span></span> </p> </td> 
   <td colname="col2"> <p> Configura el número de acciones de ampliar y alejar necesarias para aumentar o disminuir la resolución mediante un factor de dos. El cambio de resolución para cada acción de zoom es de 2^1 por paso. Configure como. <span class="codeph"> 0</span> para ampliar a resolución completa con una única acción de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> límite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la resolución de zoom máxima en relación con la imagen con resolución completa. El valor predeterminado es <span class="codeph"> 1,0</span>, que no permite un zoom superior a la resolución completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1,1`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
