---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
uuid: 3e7cdb44-4366-4e84-a6c7-c1cf1f5e6344
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 6%

---


# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Habilite, limite o deshabilite la optimización para dispositivos en los que <span class="codeph"> devicePixelRatio</span> sea bueno que <span class="codeph"> 1</span>, es decir, dispositivos con una pantalla de alta densidad como iPhone4 y dispositivos similares. Si está activo, el componente limita el tamaño de la solicitud de imagen IS como si el dispositivo solo tuviera una relación de píxeles de <span class="codeph"> 1</span> y, por lo tanto, reduce el ancho de banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Si se utiliza la configuración <span class="codeph"> limit</span> , el componente permite una alta densidad de píxeles únicamente hasta el límite especificado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
