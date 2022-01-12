---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b02f033d-be84-4cd0-b4bb-3ae9e424680c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 8%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`precarga`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> precarga</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el comportamiento de precarga del componente. Cuando se configura como <span class="codeph"> -1</span> todas las muestras se cargan simultáneamente cuando el componente se inicializa o se cambia el recurso. Cuando se configura como <span class="codeph"> 0</span> solo se cargan muestras visibles. </p> <p><span class="codeph"> <span class="varname"> precarga</span></span> define cuántas filas y columnas invisibles alrededor del área visible se precargan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`1`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`maxloadradius=-1`
