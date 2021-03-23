---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
uuid: 3666b947-4a37-4711-90b0-f9c048b588f8
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flotante
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '62'
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

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`1`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`maxloadradius=-1`
