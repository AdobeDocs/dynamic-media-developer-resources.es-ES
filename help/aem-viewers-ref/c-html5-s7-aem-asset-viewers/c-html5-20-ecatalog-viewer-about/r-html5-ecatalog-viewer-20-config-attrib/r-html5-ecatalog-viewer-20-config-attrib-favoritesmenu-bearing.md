---
title: FavoritesMenu.bearing
description: Especifica la dirección de la animación de diapositivas para el contenedor de botones.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

Especifica la dirección de la animación de diapositivas para el contenedor de botones.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Cuando se configura como <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>o <span class="codeph"> right</span>, el panel se despliega en la dirección especificada sin una comprobación de límites adicionales, lo que provoca el recorte del panel por un contenedor exterior. </p> <p>Cuando se configura como <span class="codeph"> ajuste vertical</span>, el componente cambia primero la posición del panel base a la parte inferior del menú Favoritos. Intenta desplegar el panel en una de las siguientes direcciones desde esa ubicación base: abajo, derecha, izquierda. Con cada intento, el componente comprueba si el panel está recortado por un contenedor exterior. Si todos los intentos fallan, el componente intenta cambiar la posición del panel base a la parte superior y repetir los intentos de despliegue desde la dirección superior, derecha e izquierda. </p> <p>Cuando se configura como <span class="codeph"> fit-lateral</span>, el componente utiliza una lógica similar. La base se desplaza primero a la derecha, intentando hacia la derecha, hacia abajo, y hacia arriba y hacia abajo. Luego, desplaza la base hacia la izquierda, tratando de ir hacia la izquierda, hacia abajo y hacia arriba. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
