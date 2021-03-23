---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
uuid: 98a84ba1-4b89-424a-ac2e-4a59af33cec0
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom en línea
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`anchura de anchura`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Configura cómo el componente recupera nuevas imágenes para las vistas principal y flotante durante el cambio de tamaño. </p> <p>Si se establece en <span class="codeph"> 0 </span>, el componente no carga nuevas imágenes durante el cambio de tamaño y la resolución de la imagen en la vista flotante no cambia. </p> <p>El valor <span class="codeph"> 1 </span> permite especificar uno o varios puntos de interrupción de anchura para la imagen cargada en la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> punto de interrupción,  <span class="varname"> anchura  </span>;  <span class="varname"> width  </span> </span> </p> </td> 
   <td colname="col2"> <p>Puntos de interrupción de ancho para la imagen que se carga en la vista principal. </p> <p>El componente siempre utiliza el mejor tamaño de ajuste para la carga inicial. Después de cambiar el tamaño, se garantiza que la imagen de la vista principal se descargue siempre con la anchura igual al punto de interrupción más grande más cercano y se reduzca la escala en el cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
