---
title: resMode
description: Modo de remuestreo. Selecciona el algoritmo de remuestreo o interpolación que se utilizará para escalar la imagen procesada al tamaño especificado con wid=, hei= o scl=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 14%

---

# resMode{#resmode}

Modo de remuestreo. Selecciona el algoritmo de remuestreo o interpolación que se utilizará para escalar la imagen procesada al tamaño especificado con `wid=`, `hei=`, o `scl=`.

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
   <td colname="col2"> <p>selecciona una función de ventana Lanczos modificada como un algoritmo de interpolación. Puede producir resultados ligeramente más nítidos que los bicúbicos a un coste de CPU más alto. </p> <p> <span class="codeph"> afilado </span> se ha reemplazado por <span class="codeph"> sharp2 </span>, que tiene una menor probabilidad de causar artefactos de solapamiento, también conocido como Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Selecciona el <span class="keyword"> Adobe Photoshop </span> remuestreador predeterminado para reducir el tamaño de imagen, denominado "enfoque bicúbico" en <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-ea7029f37e094d9cb85646b85fbac0ce}

Puede producirse en cualquier lugar dentro de la solicitud. Se ignora si no se aplica ningún escalado de imagen final.

## Predeterminado {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Véase también {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
