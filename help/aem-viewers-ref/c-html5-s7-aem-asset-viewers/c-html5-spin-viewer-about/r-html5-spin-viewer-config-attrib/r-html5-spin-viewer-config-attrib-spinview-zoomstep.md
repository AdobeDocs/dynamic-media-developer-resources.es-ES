---
title: SpinView.zoomstep
description: SpinView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 919477d0-87d9-4cf7-a7c8-0fbb68c6ff96
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *`paso`*[, *`límite`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> paso</span></span> </p> </td> 
   <td colname="col2"> <p> Configura el número de acciones de ampliar y alejar necesarias para aumentar o disminuir la resolución mediante un factor de dos. El cambio de resolución para cada acción de zoom es de 2^1 por paso. Definir en <span class="codeph"> 0</span> para ampliar a la resolución completa con una única acción de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> límite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la resolución de zoom máxima en relación con la imagen con resolución completa. El valor predeterminado es <span class="codeph"> 1.0</span>, que no permite un zoom superior a la resolución completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
