---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
TQID: 'https://experienceleague.adobe.com/nkYQwtTb1AUBLBbnN2HwMZLIjyolj5l-6CxEy-yEo3k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`ancho`*[; *`ancho`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Configura cómo el componente recupera nuevas imágenes para la vista principal y flotante durante el cambio de tamaño. </p> <p>Cuando se establece en <span class="codeph"> 0 </span>, el componente no carga nuevas imágenes durante el cambio de tamaño; la resolución de la imagen en la vista flotante no cambia. </p> <p>Si se establece en <span class="codeph"> 1 </span>, puede especificar uno o más puntos de interrupción de anchura para la imagen cargada en la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> punto de interrupción, <span class="varname"> ancho </span>[; <span class="varname"> ancho </span>] </span> </p> </td> 
   <td colname="col2"> <p> Puntos de interrupción de anchura para la imagen cargada en la vista principal. El componente siempre utiliza el mejor tamaño de ajuste para la carga inicial. Después del cambio de tamaño, se garantiza que la imagen de la vista principal siempre se descargue con la anchura igual al punto de interrupción más grande más cercano y se reduzca la escala en el cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
