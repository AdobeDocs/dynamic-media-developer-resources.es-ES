---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Developer,User
exl-id: b3cc32ef-dd6c-47a3-9e55-86a43e874a84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 7%

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
