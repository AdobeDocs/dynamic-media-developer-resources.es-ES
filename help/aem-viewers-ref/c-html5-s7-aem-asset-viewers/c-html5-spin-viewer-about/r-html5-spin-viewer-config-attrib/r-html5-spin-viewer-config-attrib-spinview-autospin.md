---
description: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
uuid: 9d24ed39-e4b9-442b-bc64-c77707ff69d8
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 6%

---


# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`durationdirectionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Activa o desactiva la animación de giro automática. Para lograr la mejor experiencia de giro automático, se recomienda cargar previamente todos los fotogramas estableciendo <span class="codeph"> maxloadradius</span> en <span class="codeph"> -1</span>. Sin embargo, tenga en cuenta que esto resulta en un mayor tiempo de carga y un mayor uso del ancho de banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p> Número de segundos por un giro completo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dirección</span></span> </p> </td> 
   <td colname="col2"> <p> La dirección de giro que es <span class="codeph"> 0</span> para girar hacia el este y <span class="codeph"> 1</span> para girar hacia el oeste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Número de rotaciones completas realizadas antes de que se detenga el giro automático. El número es un número de coma flotante. Establézcalo en <span class="codeph"> -1</span> para un giro automático infinito. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
