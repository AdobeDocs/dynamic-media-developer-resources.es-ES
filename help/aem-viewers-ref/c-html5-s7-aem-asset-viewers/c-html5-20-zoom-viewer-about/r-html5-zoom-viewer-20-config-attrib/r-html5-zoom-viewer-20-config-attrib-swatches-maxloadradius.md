---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: df9d5be4-d1e1-4b72-a7e7-0f3611278d2a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 7%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`precarga`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> precarga</span></span> </p> </td> 
   <td> <p>Especifica el comportamiento de precarga del componente. Cuando se configura como <span class="codeph"> -1</span> todas las muestras se cargan simultáneamente cuando el componente se inicializa o se cambia el recurso. </p> <p>Cuando se configura como <span class="codeph"> 0</span> solo se cargan muestras visibles. </p> <p><span class="codeph"><span class="varname"> precarga</span></span> define cuántas filas y columnas invisibles alrededor del área visible se precargan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=-1`
