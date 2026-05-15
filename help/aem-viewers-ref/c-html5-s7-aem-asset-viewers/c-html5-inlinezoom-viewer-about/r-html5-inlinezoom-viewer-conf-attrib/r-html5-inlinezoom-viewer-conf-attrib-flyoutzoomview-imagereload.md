---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
TQID: 'https://experienceleague.adobe.com/utzPqD5UMx7TnJK8FvqflzoSjOWGVaGXhKlviY1U9xQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`ancho`*[; *`ancho`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Configura cómo el componente recupera nuevas imágenes para la vista principal y flotante durante el cambio de tamaño. </p> <p>Definido como <span class="codeph"> 0 </span>, el componente no carga nuevas imágenes durante el cambio de tamaño y la resolución de la imagen en la vista flotante no cambia. </p> <p>Set to <span class="codeph"> 1 </span> permite especificar uno o más puntos de interrupción de anchura para la imagen cargada en la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> punto de interrupción, <span class="varname"> ancho </span>; <span class="varname"> ancho </span> </span> </p> </td> 
   <td colname="col2"> <p>Puntos de interrupción de anchura para la imagen cargada en la vista principal. </p> <p>El componente siempre utiliza el mejor tamaño de ajuste para la carga inicial. Después del cambio de tamaño, se garantiza que la imagen de la vista principal siempre se descargue con la anchura igual al punto de interrupción más grande más cercano y se reduzca la escala en el cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
