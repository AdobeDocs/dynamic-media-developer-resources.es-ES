---
description: nulo
seo-description: nulo
seo-title: CarouselView.enableHD
solution: Experience Manager
title: CarouselView.enableHD
topic: Dynamic media
uuid: 17df4a68-a251-427c-a3c4-1e0679e3f8f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> siempre|nunca|límite</span> </p> </td> 
   <td colname="col2"> <p> Habilite, limite o deshabilite la optimización para dispositivos en los que <span class="codeph"> devicePixelRatio</span> es bueno a <span class="codeph"> 1</span>, es decir, dispositivos con pantalla de alta densidad como iPhone4 y dispositivos similares. </p> <p>Si está activo, el componente limita el tamaño de la solicitud de imagen IS como si el dispositivo solo tuviera una proporción de píxeles de <span class="codeph"> 1</span> y, de ese modo, se reduzca el ancho de banda. </p> <p>Consulte el ejemplo siguiente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Si se utiliza la configuración de <span class="codeph"> límite</span> , el componente solo habilita la densidad de píxeles altos hasta el límite especificado. </p> <p>Consulte el ejemplo siguiente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
