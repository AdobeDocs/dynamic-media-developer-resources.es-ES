---
title: ThumbnailGridView.enabledragging
description: ThumbnailGridView.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
TQID: 'https://experienceleague.adobe.com/zdDZOJxd9p7pOlbP9XPEBl27AILe8fvINca8lbsnImI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 6%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Activa o desactiva la capacidad del usuario de desplazar muestras con un ratón o mediante gestos táctiles </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Funciones dentro del intervalo <span class="codeph"> 0-1 </span>. Es un valor <span class="codeph"> % </span> para el movimiento en una dirección incorrecta de la velocidad real. Si se establece en <span class="codeph"> 1 </span>, se mueve con el mouse. Si se establece en <span class="codeph"> 0 </span>, no le permite moverse en la dirección incorrecta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-831c23dea82449bfa50fd155bea365b7}

Opcional.

## Predeterminado {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## Ejemplo {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`

