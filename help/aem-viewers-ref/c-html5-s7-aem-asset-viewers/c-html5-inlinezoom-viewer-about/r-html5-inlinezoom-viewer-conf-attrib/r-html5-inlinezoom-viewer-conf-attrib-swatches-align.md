---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: d9db34f3-66df-45c2-9727-bdcdf09773db
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

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`center,center`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`align=left,top`
