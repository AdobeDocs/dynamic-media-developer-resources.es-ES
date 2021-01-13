---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
topic: Dynamic media
uuid: 3666b947-4a37-4711-90b0-f9c048b588f8
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
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

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`1`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`maxloadradius=-1`
