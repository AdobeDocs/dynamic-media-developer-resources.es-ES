---
description: nulo
seo-description: nulo
seo-title: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
topic: Dynamic media
uuid: 3e7cdb44-4366-4e84-a6c7-c1cf1f5e6344
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> siempre|nunca|límite</span> </p> </td> 
   <td colname="col2"> <p> Habilite, limite o deshabilite la optimización para dispositivos en los que <span class="codeph"> devicePixelRatio</span> es bueno a <span class="codeph"> 1</span>, es decir, dispositivos con una pantalla de alta densidad como iPhone4 y dispositivos similares. Si está activo, el componente limita el tamaño de la solicitud de imagen IS como si el dispositivo solo tuviera una proporción de píxeles de <span class="codeph"> 1</span> y, por tanto, reduzca el ancho de banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Si se utiliza la configuración de <span class="codeph"> límite</span> , el componente solo habilita la densidad de píxeles altos hasta el límite especificado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
