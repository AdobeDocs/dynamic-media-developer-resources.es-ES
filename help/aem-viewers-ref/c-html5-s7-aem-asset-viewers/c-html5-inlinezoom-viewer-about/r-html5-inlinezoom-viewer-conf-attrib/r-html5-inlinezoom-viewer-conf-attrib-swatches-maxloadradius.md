---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
topic: Dynamic Media
uuid: 15d555bc-f9f7-4d0e-809e-7a51358e5c03
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 7%

---


# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el comportamiento de precarga del componente. Cuando se establece en <span class="codeph"> -1</span>, todas las muestras se cargan simultáneamente cuando se inicializa el componente o se cambia el recurso. Cuando se establece en <span class="codeph"> 0</span> sólo se cargan muestras visibles. </p> <p><span class="codeph"> <span class="varname"> </span></span> preload define cuántas filas/columnas invisibles alrededor del área visible se precargarán. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`maxloadradius=-1`
