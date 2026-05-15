---
title: resMode
description: Modo de remuestreo. Selecciona el algoritmo de remuestreo o interpolación que se utilizará para escalar la imagen procesada al tamaño especificado con wid=, hei= o scl=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
TQID: 'https://experienceleague.adobe.com/VLg7JU1aiA7tRGG6vmoHciv-hDIZftbYtU4hAE5N0DY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 6%

---

# resMode{#resmode}

Modo de remuestreo. Selecciona el algoritmo de remuestreo o interpolación que se utilizará para escalar la imagen procesada al tamaño especificado con `wid=`, `hei=` o `scl=`.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Selecciona la interpolación bilineal estándar. Método de remuestreo más rápido; pueden verse algunos defectos de solapamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Selecciona la interpolación bicúbica. Requiere más CPU que la interpolación bilineal, pero genera imágenes más nítidas con defectos de solapamiento menos evidentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Selecciona una función de ventana de Lanczos modificada como algoritmo de interpolación. Puede producir resultados ligeramente más nítidos que los bicúbicos a un coste de CPU más alto. </p> <p> <span class="codeph"> sharp </span> ha sido reemplazado por <span class="codeph"> sharp2 </span>, lo que tiene una menor probabilidad de causar artefactos de solapamiento, también conocidos como Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Selecciona el remuestreador predeterminado de <span class="keyword"> Adobe Photoshop </span> para reducir el tamaño de la imagen, que se denomina "enfoque bicúbico" en <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-ea7029f37e094d9cb85646b85fbac0ce}

Puede producirse en cualquier lugar dentro de la solicitud. Se ignora si no se aplica ningún escalado de imagen final.

## Predeterminado {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Véase también {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
