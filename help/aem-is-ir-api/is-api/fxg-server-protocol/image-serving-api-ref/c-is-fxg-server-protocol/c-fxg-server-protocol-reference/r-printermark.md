---
description: Mostrar marcas de impresora. Especifica cómo mostrar las marcas de impresora.
solution: Experience Manager
title: printMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 31%

---

# printMark{#printermark}

Mostrar marcas de impresora. Especifica cómo mostrar las marcas de impresora.

` printerMark= *`recortar `*, *`marcadores `*, *`marcas registrar `*, *`marcas color `*, *`barspage `*, *``*, *`informationestilo línea de `*, *`peso incrustar capa`*`

Las diferentes marcas pueden desactivarse o activarse. También se puede controlar el estilo de las marcas de impresora.

Los siguientes son los valores válidos:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>bleed marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>registration marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>color bars= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>estilo= </p></td> 
  <td class="stentry"> <p>Predeterminado </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>El valor predeterminado es predeterminado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>line weight= </p></td> 
  <td class="stentry"> <p>Cualquier valor del rango 0,125 - 2,0, ambos valores incluyen. </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0.25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 1. </p></td> 
 </tr> 
</table>

## Ejemplo {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
