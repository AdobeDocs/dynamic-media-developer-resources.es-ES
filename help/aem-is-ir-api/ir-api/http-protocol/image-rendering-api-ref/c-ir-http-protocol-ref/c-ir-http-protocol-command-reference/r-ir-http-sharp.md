---
description: Enfocar textura. Especifica el enfoque que se aplicará al procesar este material.
seo-description: Enfocar textura. Especifica el enfoque que se aplicará al procesar este material.
seo-title: enfocado
solution: Experience Manager
title: enfocado
topic: Scene7 Image Serving - Image Rendering API
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 5%

---


# sharp{#sharp}

Enfocar textura. Especifica el enfoque que se aplicará al procesar este material.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Sin enfoque. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Enfoque normal (tarde). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 enfoque alternativo (inicial). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Más enfoque (temprano y tarde). </p> </td> 
 </tr> 
</table>

`sharp=1` aplica enfoque una vez procesado el material;  `sharp=2` aplica enfoque después de aplicar la escala inicial de la textura, pero antes de que se transforme en escena;  `sharp=3` aplica enfoque antes y después de la transformación.

El algoritmo de enfoque y la cantidad de enfoque y otros parámetros USM (máscara de enfoque) se controlan mediante la plantilla de material predeterminada proporcionada por la viñeta o con `rs=`.

## Propiedades {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Atributo Material. Ignorado por materiales de color sólido.

## Predeterminado {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, si el material está basado en una entrada de catálogo, en caso contrario  `attribute::Sharp`.

## Véase también {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catálogo::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e),  [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
