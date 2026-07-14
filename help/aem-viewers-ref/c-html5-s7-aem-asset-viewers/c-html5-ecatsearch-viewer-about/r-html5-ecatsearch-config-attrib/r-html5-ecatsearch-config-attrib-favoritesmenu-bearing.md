---
description: Especifica la dirección de la animación de diapositiva para el contenedor de botones.
solution: Experience Manager
title: FavoritosMenú.cojinete
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2466a288-59c2-4a5e-b0bd-ff5b42dcacdb
TQID: 'https://experienceleague.adobe.com/Pe9frhI8cmIorx5zE-cdC-frEP77UOksMwyM9PvUCdo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# FavoritosMenú.cojinete{#favoritesmenu-bearing}

Especifica la dirección de la animación de diapositiva para el contenedor de botones.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> arriba|abajo|izquierda|derecha|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Cuando se establece en <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> o <span class="codeph"> right</span>, el panel se despliega en la dirección especificada sin una comprobación de límites adicional, lo que provoca que un contenedor externo recorte el panel. </p> <p>Cuando se establece en <span class="codeph"> fit-vertical</span>, el componente primero cambia la posición del panel base a la parte inferior del menú Favoritos e intenta desplegar el panel en una de las siguientes direcciones desde dicha ubicación base: bottom, right, left. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue desde la dirección superior, derecha e izquierda. </p> <p>Cuando se establece en <span class="codeph"> fit-lateral</span>, el componente utiliza una lógica similar. La base se desplaza primero hacia la derecha, tratando de girar hacia la derecha, hacia abajo y hacia arriba. Luego, desplaza la base hacia la izquierda, tratando de izquierda, abajo y arriba en las direcciones de despliegue. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
