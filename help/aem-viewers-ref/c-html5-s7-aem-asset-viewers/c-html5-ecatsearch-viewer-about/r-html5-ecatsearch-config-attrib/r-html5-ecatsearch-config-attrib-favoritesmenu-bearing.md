---
description: Especifica la dirección de la animación de diapositivas para el contenedor de botones.
seo-description: Especifica la dirección de la animación de diapositivas para el contenedor de botones.
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic media
uuid: c3f415ad-f976-464a-9067-a5d526908352
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

Especifica la dirección de la animación de diapositivas para el contenedor de botones.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Cuando se establece en <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> o <span class="codeph"> right</span>, el panel se despliega en la dirección especificada sin una verificación adicional de los límites, lo que resulta en un recorte del panel por un contenedor externo. </p> <p>Cuando se establece en <span class="codeph"> fit-vertical</span>, el componente primero cambia la posición del panel base a la parte inferior del menú Favoritos e intenta desplegar el panel en una de las siguientes direcciones desde dicha ubicación base: abajo, derecha, izquierda. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue desde una dirección superior, derecha e izquierda. </p> <p>Cuando se establece en <span class="codeph"> fit-lateral</span>, el componente utiliza una lógica similar. La base se desplaza primero a la derecha, y prueba las direcciones hacia la derecha, hacia abajo y hacia arriba. Luego, desplaza la base hacia la izquierda, tratando de ir hacia la izquierda, hacia abajo y hacia arriba. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
