---
description: Mostrar marcas de impresora. Especifica cómo se muestran las marcas de impresora.
seo-description: Mostrar marcas de impresora. Especifica cómo se muestran las marcas de impresora.
seo-title: printerMark
solution: Experience Manager
title: printerMark
topic: Scene7 Image Serving - Image Rendering API
uuid: 3e5699ce-3ccd-4f85-91dd-c40c252a758d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# printerMark{#printermark}

Mostrar marcas de impresora. Especifica cómo se muestran las marcas de impresora.

` printerMark= *`recortar`*, *`marcas`*, *`de sangrado marcas de registro`*, *`marcas de color`*, *`de barrido`*, *``*, *`información de estillínea de`*, *`grosor incrustar capa`*`

Las distintas marcas pueden desactivarse o activarse. También se puede controlar el estilo de las marcas de impresora.

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
  <td class="stentry"> <p>Predeterminado es Predeterminado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>peso de línea= </p></td> 
  <td class="stentry"> <p>Cualquier valor en el intervalo 0,125 - 2,0, ambos valores inclusive. </p></td> 
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
