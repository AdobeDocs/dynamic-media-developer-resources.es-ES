---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 300bbee8-29f1-444d-bf98-42aeb9c5017b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Especifica la alineación interna (anclaje) del contenedor de muestras dentro del área del componente. En Muestras, el tamaño del contenedor de miniaturas interno es tal que solo se muestra un número entero de muestras. Como resultado, hay cierto relleno entre los límites del contenedor interno y el componente externo. Este comando especifica cómo se coloca el contenedor de muestras interno dentro del componente.

<table id="table_33CC037517964DA89EE0C005BB6B32BB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> izquierda|centro|derecha</span> </p> </td> 
   <td colname="col2"> <p> Define la alineación de las muestras horizontales. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> superior|centro|inferior</span> </p> </td> 
   <td colname="col2"> <p> Define la alineación de las muestras verticales. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`center,center`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`align=left,top`
