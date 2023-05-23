---
title: Swatches.direction
description: Swatches.direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bd01ff03-fea7-42ad-aa99-72273f55bda0
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 5%

---

# Swatches.direction{#swatches-direction}

`[Swatches.|<containerId>_swatches.]direction=auto|left|right`

<table id="table_B4B930A32C0742F4932BF071B9EEA9F4"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td> <p> Especifica la forma en que la vista se rellena con muestras. </p> <p> <span class="codeph"> left </span> establece el orden de relleno de izquierda a derecha; </p> <p> <span class="codeph"> derecha </span> invierte el orden para que la vista se rellene de derecha a izquierda y de arriba a abajo. </p> <p>Cuándo <span class="codeph"> auto </span> está configurado, se aplica el componente <span class="codeph"> derecha </span> modo cuando la configuración regional está establecida en <span class="codeph"> ja </span>; de lo contrario, se utiliza left. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`direction=right`
