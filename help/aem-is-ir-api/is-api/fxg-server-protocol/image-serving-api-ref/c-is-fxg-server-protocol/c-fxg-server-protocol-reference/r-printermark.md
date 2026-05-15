---
description: Mostrar marcas de impresora. Especifica cómo mostrar las marcas de impresora.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
TQID: 'https://experienceleague.adobe.com/tit-a3stXGj0fZoMgi15lPIk-MtZSvUDOqlcayfNlwk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 24%

---

# printerMark{#printermark}

Mostrar marcas de impresora. Especifica cómo mostrar las marcas de impresora.

` printerMark= *`marcas de recorte`*, *`marcas de sangrado`*, *`marcas de registro`*, *`barras de color`*, *`información de página`*, *`estilo`*, *`grosor de línea`*, *`incrustación de capa`*`

Las diferentes marcas se pueden activar o desactivar. El estilo de las marcas de impresora también se puede controlar.

Los siguientes son los valores válidos:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>marcas de recorte= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>marcas de sangrado= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>marcas de registro= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>barras de color= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>información de página= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Predeterminado </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>El valor predeterminado es Predeterminado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>grosor de línea= </p></td> 
  <td class="stentry"> <p>Cualquier valor en el rango 0,125 - 2,0, ambos valores incluidos. </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>incrustar capa= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>El valor predeterminado es 1. </p></td> 
 </tr> 
</table>

## Ejemplo {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
