---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 122c6406-6fd7-4e45-bff2-11022a3f2cf7
TQID: 'https://experienceleague.adobe.com/RAxn-9VY1W6XWau-hMwdiiIks9Fzdrtex0C54aHs-tE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`duration`*[, *`count`*][, *`fade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duración</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica el número de segundos que el texto de sugerencia se muestra antes de ocultarse. Cuando se establece en <span class="codeph"> -1</span>, el mensaje siempre se muestra, aunque el usuario active el menú flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> recuento</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica el número de veces que se muestra el texto al ver nuevas imágenes del conjunto. Un valor de <span class="codeph"> -1</span> significa que el texto siempre se muestra al ver cualquier imagen del conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fundido</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración de una animación de transición que se produce cuando el texto aparece o desaparece. Un valor de <span class="codeph"> 0</span> significa que no hay transición de fundido. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
