---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`duration`*][, *`direction`*][, *`número_giro`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Activa o desactiva la animación automática de giro. Para lograr la mejor experiencia de giro automático, se recomienda cargar previamente todos los fotogramas estableciendo <span class="codeph"> maxloadradius</span> en <span class="codeph"> -1</span>. Sin embargo, tenga en cuenta que esta configuración aumenta el tiempo de carga y el uso del ancho de banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p> La cantidad de segundos por cada giro completo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dirección</span></span> </p> </td> 
   <td colname="col2"> <p> La dirección de giro que es <span class="codeph"> 0</span> para girar hacia el este y <span class="codeph"> 1</span> para girar hacia el oeste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Número de rotaciones completas hasta que se detiene el giro automático. El número es un número de coma flotante. Se establece en <span class="codeph"> -1</span> para un giro automático infinito. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
