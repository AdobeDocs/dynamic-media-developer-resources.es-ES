---
title: CarouselView.enableHD
description: CarouselView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 5%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Activar, limitar o desactivar la optimización para dispositivos en los que <span class="codeph"> devicePixelRatio</span> es bueno que <span class="codeph"> 1</span>, es decir, dispositivos con visualización de alta densidad como iPhone4 y similares. </p> <p>Si está activo, el componente limita el tamaño de la solicitud de imagen del servicio de imágenes como si el dispositivo solo tuviera una proporción de píxeles de <span class="codeph"> 1</span> y así reducir el ancho de banda. </p> <p>Consulte el ejemplo siguiente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Si se usa la variable <span class="codeph"> límite</span> Con esta configuración, el componente solo permite una alta densidad de píxeles hasta el límite especificado. </p> <p>Consulte el ejemplo siguiente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
