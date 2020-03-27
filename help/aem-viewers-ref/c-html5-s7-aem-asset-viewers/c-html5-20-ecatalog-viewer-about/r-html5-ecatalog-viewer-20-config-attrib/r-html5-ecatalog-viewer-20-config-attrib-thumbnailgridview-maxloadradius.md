---
description: nulo
seo-description: nulo
seo-title: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
topic: Dynamic media
uuid: 13ea3917-346a-47c3-a535-f771910fa1c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica el comportamiento de precarga del componente. </p> <p>Cuando se establece en <span class="codeph"> -1</span> , las miniaturas se cargan simultáneamente cuando se inicializa el componente o cambia el recurso. </p> <p>Cuando se establece en <span class="codeph"> 0</span> , solo se cargan las miniaturas visibles. </p> <p>Establecer <span class="codeph"><span class="varname"> precarga</span></span> define cuántas filas/columnas invisibles alrededor del área visible se cargan previamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-a3abd04c03e14c238a07349ce50d8310}

Opcional.

## Predeterminado {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## Ejemplo {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
