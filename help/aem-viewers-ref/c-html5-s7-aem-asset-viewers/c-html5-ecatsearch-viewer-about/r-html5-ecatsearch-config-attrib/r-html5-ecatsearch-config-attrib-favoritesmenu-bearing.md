---
description: Especifica la dirección de la animación de diapositiva para el contenedor de botones.
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2466a288-59c2-4a5e-b0bd-ff5b42dcacdb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

Especifica la dirección de la animación de diapositiva para el contenedor de botones.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Cuando se establece en <span class="codeph"> arriba</span>, <span class="codeph"> abajo</span>, <span class="codeph"> left</span>, o <span class="codeph"> derecha</span>, el panel se despliega en la dirección especificada sin una comprobación de límites adicional, lo que da como resultado un recorte del panel por un contenedor externo. </p> <p>Cuando se establece en <span class="codeph"> fit-vertical</span>, el componente primero cambia la posición del panel base a la parte inferior del menú Favoritos e intenta desplegar el panel en una de las siguientes direcciones desde dicha ubicación base: bottom, right, left. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue desde la dirección superior, derecha e izquierda. </p> <p>Cuando se establece en <span class="codeph"> fit-lateral</span>, el componente utiliza una lógica similar. La base se desplaza primero hacia la derecha, tratando de girar hacia la derecha, hacia abajo y hacia arriba. Luego, desplaza la base hacia la izquierda, tratando de izquierda, abajo y arriba en las direcciones de despliegue. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
