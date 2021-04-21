---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---


# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`]

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

## Propiedades {#section-831c23dea82449bfa50fd155bea365b7}

Opcional.

## Predeterminado {#section-464be2db89f34516ad93f32f7783d2b0}

[!DNL `1,0.5`]

## Ejemplo {#section-e67c8807762e471bb03d6a8fb20e19d4}

[!DNL `enabledragging=0`]
