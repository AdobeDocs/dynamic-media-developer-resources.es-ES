---
description: FavoritesView.favoritesThumbView
solution: Experience Manager
title: FavoritesView.favoritesThumbView
uuid: 5c362eb3-dece-4546-8a79-fd79c2852a78
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 9%

---


# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`área`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> área</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el área de recorte para la miniatura de Favoritos. Se expresa como un valor relativo del tamaño total del fotograma, con un rango de <span class="codeph"> 0</span> a <span class="codeph"> 1,0</span>. </p> <p>Un valor de <span class="codeph"> 1</span> significa que la imagen de marco completa se utiliza para la miniatura. </p> <p>Un valor de <span class="codeph"> 0.1</span> significa que solo se utiliza el 10% del tamaño del fotograma. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`0.1`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`favoritesThumbArea=0.5`
