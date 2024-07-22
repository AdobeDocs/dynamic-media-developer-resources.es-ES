---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3cb91483-de8c-4d5c-9b46-7026c5001f3a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Especifica la alineación interna (anclaje) del contenedor de muestras dentro del área del componente. En Muestras, el tamaño del contenedor de miniaturas interno es tal que solo se muestra un número entero de muestras. Como resultado, hay cierto relleno entre los límites del contenedor interno y el componente externo. Este comando especifica cómo se coloca el contenedor de muestras interno dentro del componente.

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> izquierda|centro|derecha</span> </p> </td> 
   <td> <p> Define la alineación de las muestras horizontales. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> superior|centro|inferior</span> </p> </td> 
   <td> <p> Define la alineación de las muestras verticales. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`center,center`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`align=left,top`
