---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
uuid: 5badee0b-3bbc-4306-bc60-a606775db2bd
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Habilite, limite o deshabilite la optimización para dispositivos en los que <span class="codeph"> devicePixelRatio</span> sea bueno que <span class="codeph"> 1</span>. Afecta a dispositivos con una pantalla de alta densidad como iPhone4 y dispositivos similares. Si está activo, el componente limita el tamaño de la solicitud de imagen IS como si el dispositivo tuviera una relación de píxeles de <span class="codeph"> 1</span>, reduciendo así el ancho de banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Si se utiliza la configuración de límite, el componente permite una alta densidad de píxeles sólo hasta el límite especificado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
