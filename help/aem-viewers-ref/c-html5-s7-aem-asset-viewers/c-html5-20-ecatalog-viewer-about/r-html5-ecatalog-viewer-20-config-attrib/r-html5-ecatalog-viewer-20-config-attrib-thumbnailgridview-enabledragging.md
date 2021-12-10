---
title: ThumbnailGridView.enabledragging
description: ThumbnailGridView.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 6%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> Habilita o deshabilita la capacidad de un usuario para desplazarse por las muestras con un ratón o mediante gestos táctiles </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Funciones dentro de <span class="codeph"> 0-1 </span> intervalo. Es un <span class="codeph"> % </span> para el movimiento en la dirección incorrecta de la velocidad real. Si está configurado en <span class="codeph"> 1 </span>, se mueve con el ratón. Si está configurado en <span class="codeph"> 0 </span>, no permite moverse en la dirección equivocada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-831c23dea82449bfa50fd155bea365b7}

Opcional.

## Predeterminado {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## Ejemplo {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
