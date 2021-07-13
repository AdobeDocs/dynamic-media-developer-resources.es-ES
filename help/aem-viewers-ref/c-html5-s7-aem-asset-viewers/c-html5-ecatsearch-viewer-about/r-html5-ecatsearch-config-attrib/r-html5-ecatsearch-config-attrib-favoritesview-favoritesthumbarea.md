---
description: FavoritesView.favoritesThumbView
solution: Experience Manager
title: FavoritesView.favoritesThumbView
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Developer,User
exl-id: 3a0a7482-315f-4192-aa6d-e9cc1415194f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 9%

---

# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

[!DNL ` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`área`*`]

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

[!DNL `0.1`]

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `favoritesThumbArea=0.5`]
