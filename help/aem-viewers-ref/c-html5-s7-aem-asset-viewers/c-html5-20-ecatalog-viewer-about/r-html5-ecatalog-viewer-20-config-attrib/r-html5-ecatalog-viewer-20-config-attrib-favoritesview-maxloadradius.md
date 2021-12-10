---
title: FavoritesView.maxloadradius
description: FavoritesView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 6bbf75f1-96e7-496d-9f5c-6f449f76bfdd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 7%

---

# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

` [FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`precarga`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> precarga</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el comportamiento de precarga del componente. </p> <p>Cuando se configura como <span class="codeph"> -1</span>, todas las miniaturas se cargan simultáneamente cuando el componente se inicializa o se cambia el recurso. </p> <p>Cuando se configura como <span class="codeph"> 0</span>, solo se cargan las miniaturas visibles. </p> <p> Cuando se configura como <span class="codeph"><span class="varname"> precarga</span></span>, puede especificar cuántas filas invisibles alrededor del área visible se precargan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`1`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`maxloadradius=0`
