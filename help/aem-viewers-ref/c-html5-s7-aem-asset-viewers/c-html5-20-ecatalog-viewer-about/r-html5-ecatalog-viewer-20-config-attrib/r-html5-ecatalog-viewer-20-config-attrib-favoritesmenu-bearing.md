---
description: Especifica la dirección de la animación de diapositivas para el contenedor de botones.
seo-description: Especifica la dirección de la animación de diapositivas para el contenedor de botones.
seo-title: FavoritosMenú.porte
solution: Experience Manager
title: FavoritosMenú.porte
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavoritosMenú.porte{#favoritesmenu-bearing}

Especifica la dirección de la animación de diapositivas para el contenedor de botones.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Cuando se establece en <span class="codeph"> arriba</span>, <span class="codeph"> abajo</span>, <span class="codeph"> izquierda</span>o <span class="codeph"> derecha</span>, el panel se despliega en la dirección especificada sin una comprobación adicional de los límites, lo que da como resultado un recorte del panel por un contenedor exterior. </p> <p>Cuando se define en <span class="codeph"> vertical</span>, el componente cambia primero la posición del panel base a la parte inferior del menú Favoritos e intenta desplegar el panel en una de las siguientes direcciones desde dicha ubicación base: abajo, derecha, izquierda. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue desde una dirección superior, derecha e izquierda. </p> <p>Cuando se define como <span class="codeph"> ajustable lateral</span>, el componente utiliza una lógica similar. La base se desplaza primero a la derecha, y prueba las direcciones hacia la derecha, hacia abajo y hacia arriba. Luego, desplaza la base hacia la izquierda, tratando de ir hacia la izquierda, hacia abajo y hacia arriba. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
