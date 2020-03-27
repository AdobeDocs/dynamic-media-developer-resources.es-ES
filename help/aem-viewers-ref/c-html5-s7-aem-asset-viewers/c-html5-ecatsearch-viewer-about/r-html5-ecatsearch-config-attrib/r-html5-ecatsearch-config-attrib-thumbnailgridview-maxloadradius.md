---
description: nulo
seo-description: nulo
seo-title: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
topic: Dynamic media
uuid: e72ae5d6-574e-4f30-827c-021ce5dafcee
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

[!DNL `[ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

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

[!DNL `1`]

## Ejemplo {#section-472614b59e04430490a7f16c932bce89}

[!DNL `maxloadradius=0`]
