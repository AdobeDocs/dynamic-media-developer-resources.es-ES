---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> Habilita o deshabilita la capacidad de un usuario para desplazarse por las muestras con un ratón o mediante gestos táctiles </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> Funciones dentro del rango <span class="codeph"> 0-1 </span>. Es un valor <span class="codeph"> % </span> para el movimiento en la dirección incorrecta de la velocidad real. Si se establece en <span class="codeph"> 1 </span>, se mueve con el ratón. Si se establece en <span class="codeph"> 0 </span>, no le permite moverse en la dirección incorrecta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enabledragging=0`
