---
description: Modo de remuestreo. Selecciona el algoritmo de remuestreo o interpolación que se utilizará para escalar la imagen representada al tamaño especificado con wid=, hei= o scl=.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 13%

---

# resMode{#resmode}

Modo de remuestreo. Selecciona el algoritmo de remuestreo o interpolación que se utilizará para escalar la imagen representada al tamaño especificado con wid=, hei= o scl=.

` `resMode=bilin|bicub|Sharp2|biSharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Selecciona la interpolación bilineal estándar. Método de remuestreo más rápido; pueden verse algunos defectos de solapamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Selecciona la interpolación bicúbica. Mayor densidad de CPU que la interpolación bilineal, pero producirá imágenes más nítidas con menos artefactos de solapamiento visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> agudo2  </span> </p> </td> 
   <td colname="col2"> <p>selecciona una función de ventana Lanczos modificada como un algoritmo de interpolación. Puede producir resultados ligeramente más nítidos que la bicúbica a un mayor costo de CPU. </p> <p> <span class="codeph"> el punto  </span> ha sido sustituido por el  <span class="codeph"> punto 2  </span>, que tiene menos probabilidades de causar artefactos de aliasing, también conocido como Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bici  </span> </p> </td> 
   <td colname="col2"> <p>Selecciona el <span class="keyword"> reampliador predeterminado </span> de Adobe Photoshop para reducir el tamaño de la imagen, que se denomina "nitidez bicúbica" en <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-ea7029f37e094d9cb85646b85fbac0ce}

Puede ocurrir en cualquier lugar dentro de la solicitud. Se omite si no se aplica ningún escalado de imagen final.

## Predeterminado {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Véase también {#section-16c557a2250e4f04b3e6cbef18add9ce}

[atributo::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
