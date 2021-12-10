---
title: FavoritesView.favoritesThumbView
description: FavoritesView.favoritesThumbView
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 5c57fcc8-be67-408a-9c4c-4e15d5fe6410
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 10%

---

# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`área`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> área</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el área de recorte para la miniatura de Favoritos. Se expresa como un valor relativo del tamaño total del marco, con un rango de <span class="codeph"> 0</span> a <span class="codeph"> 1,0</span>. </p> <p>Un valor de <span class="codeph"> 1</span> significa que la imagen de marco completa se utiliza para la miniatura. </p> <p>Un valor de <span class="codeph"> 0,1</span> significa que solo se utiliza el 10 % del tamaño del marco. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`0.1`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`favoritesThumbArea=0.5`
