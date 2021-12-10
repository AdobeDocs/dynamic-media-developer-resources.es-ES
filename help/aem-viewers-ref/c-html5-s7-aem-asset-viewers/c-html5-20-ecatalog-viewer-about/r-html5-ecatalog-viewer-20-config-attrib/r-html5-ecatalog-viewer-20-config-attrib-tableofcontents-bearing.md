---
title: TableOfContents.bearing
description: TableOfContents.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 2%

---

# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> Controla la dirección del aspecto del panel desplegable. </p> <p>Cuando se configura como <span class="codeph"> ajuste vertical</span>, el componente cambia primero la posición del panel base a la parte inferior de su botón e intenta desplegar el panel a la derecha o a la izquierda desde la ubicación base. Con cada intento, el componente comprueba si el panel está recortado por un contenedor exterior. Si todos los intentos fallan, el componente intenta cambiar la posición del panel base a la parte superior y repetir los intentos de despliegue en la dirección derecha e izquierda. </p> <p>Cuando se configura como <span class="codeph"> fit-lateral</span>, el componente utiliza una lógica similar, pero cambia la base a la derecha primero, intentando bajar y subir las direcciones de despliegue. Luego, desplaza la base hacia la izquierda, tratando de bajar y subir las direcciones de despliegue. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Establece el retraso en segundos para el temporizador de ocultación automática desplegable que oculta el panel cuando un usuario está inactivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-55436ddd78b04f538dbb9a7a8463feae}

Opcional.

## Predeterminado {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## Ejemplo {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
