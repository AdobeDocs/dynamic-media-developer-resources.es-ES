---
title: Swatches.direction
description: Swatches.direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 906541bc-46dd-4a7c-8ee9-eb45ec3bd340
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 5%

---

# Swatches.direction{#swatches-direction}

`[Swatches.|<containerId>_swatches.]direction=auto|left|right`

<table id="table_B4B930A32C0742F4932BF071B9EEA9F4"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> auto|izquierda|derecha </span> </p> </td> 
   <td> <p> Especifica la forma en que la vista se rellena con muestras. </p> <p> <span class="codeph"> left </span> establece el orden de relleno de izquierda a derecha; </p> <p> <span class="codeph"> </span> de la derecha invierte el orden para que la vista se rellene de derecha a izquierda y de arriba a abajo. </p> <p>Cuando se establece <span class="codeph"> auto </span>, el componente aplica el modo <span class="codeph"> right </span> cuando locale se establece en <span class="codeph"> ja </span>; de lo contrario, se usa left. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`auto`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`direction=right`
