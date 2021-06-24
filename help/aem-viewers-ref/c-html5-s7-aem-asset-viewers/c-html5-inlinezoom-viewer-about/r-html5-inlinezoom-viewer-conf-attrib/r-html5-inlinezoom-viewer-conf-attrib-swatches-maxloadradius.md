---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom en línea
role: Developer,Business Practitioner
exl-id: 574cb37c-009a-43c7-ae55-8b26c0c096c5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`precarga`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el comportamiento de precarga del componente. Cuando se establece en <span class="codeph"> -1</span>, todas las muestras se cargarán simultáneamente cuando se inicialice el componente o se cambie el recurso. Cuando se establece en <span class="codeph"> 0</span>, solo se cargan muestras visibles. </p> <p><span class="codeph"> <span class="varname"> </span></span> precarga define cuántas filas y columnas invisibles alrededor del área visible se precargarán. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`maxloadradius=-1`
