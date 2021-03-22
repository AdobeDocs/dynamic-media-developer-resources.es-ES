---
description: FavoritesView.fmt
solution: Experience Manager
title: FavoritesView.fmt
uuid: 4d9d161e-e39b-4607-9fb1-9dbfb06d7704
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 5%

---


# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica el formato de imagen que utiliza el componente para cargar imágenes desde el servidor de imágenes. El formato es cualquier valor compatible con Image Server y el explorador del cliente. </p> <p>Si el formato de imagen termina con <span class="codeph"> -alpha</span>, el componente procesa las imágenes como contenido transparente. Para los demás valores de formato de imagen, el componente trata las imágenes como opacas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
