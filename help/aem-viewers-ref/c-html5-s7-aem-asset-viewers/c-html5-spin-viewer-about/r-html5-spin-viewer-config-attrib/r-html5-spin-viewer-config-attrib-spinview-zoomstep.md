---
description: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
uuid: f8369636-08e9-4f00-8562-86a2a907b4fa
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 6%

---


# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> paso</span></span> </p> </td> 
   <td colname="col2"> <p> Configura el número de acciones de acercamiento y alejamiento necesarias para aumentar o reducir la resolución en un factor de dos. El cambio de resolución para cada acción de zoom es de 2^1 por paso. Establézcalo en <span class="codeph"> 0</span> para hacer zoom a resolución completa con una sola acción de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> límite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la resolución máxima de zoom, en relación con la imagen de resolución completa. El valor predeterminado es <span class="codeph"> 1.0</span>, lo que no permite ampliar el zoom más allá de la resolución completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
