---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Developer,Business Practitioner
exl-id: e93de3b5-b42d-4db8-90b9-9e2aa53af775
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`precarga`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica el comportamiento de precarga del componente. </p> <p>Cuando se establece en <span class="codeph"> -1</span>, las miniaturas se cargan simultáneamente cuando el componente se inicializa o el recurso cambia. </p> <p>Cuando se establece en <span class="codeph"> 0</span> solo se cargan las miniaturas visibles. </p> <p>El valor <span class="codeph"><span class="varname"> precarga</span></span> define cuántas filas/columnas invisibles alrededor del área visible están precargadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-a3abd04c03e14c238a07349ce50d8310}

Opcional.

## Predeterminado {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## Ejemplo {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
