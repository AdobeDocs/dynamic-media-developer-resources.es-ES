---
title: Swatches.direction
description: Swatches.direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 906541bc-46dd-4a7c-8ee9-eb45ec3bd340
TQID: 'https://experienceleague.adobe.com/3SW53AEy1Gg8y3r9h9-TpuXaXgSh1MA5T0rxn1ziEU0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 4%

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
