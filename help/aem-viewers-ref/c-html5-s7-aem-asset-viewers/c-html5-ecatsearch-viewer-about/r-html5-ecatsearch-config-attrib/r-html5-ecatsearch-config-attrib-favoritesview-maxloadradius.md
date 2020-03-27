---
description: nulo
seo-description: nulo
seo-title: FavoritesView.maxloadradius
solution: Experience Manager
title: FavoritesView.maxloadradius
topic: Dynamic media
uuid: 0479c371-487a-4e05-b009-9036ea464abf
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el comportamiento de precarga del componente. </p> <p>Cuando se establece en <span class="codeph"> -1</span>, todas las miniaturas se cargan simultáneamente cuando se inicializa el componente o se cambia el recurso. </p> <p>Cuando se establece en <span class="codeph"> 0</span>, solo se cargan las miniaturas visibles. </p> <p> Cuando se configura en <span class="codeph"><span class="varname"> precarga</span></span>, puede especificar cuántas filas invisibles alrededor del área visible se precargan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `1`]

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `maxloadradius=0`]
