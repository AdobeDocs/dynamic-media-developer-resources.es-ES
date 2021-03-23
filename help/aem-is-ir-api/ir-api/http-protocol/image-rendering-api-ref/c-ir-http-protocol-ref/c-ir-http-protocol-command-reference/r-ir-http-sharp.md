---
description: Enfoque la textura. Especifica la nitidez que se aplicará al procesar este material.
seo-description: Enfoque la textura. Especifica la nitidez que se aplicará al procesar este material.
seo-title: enfocado
solution: Experience Manager
title: enfocado
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 5%

---


# Sharp{#sharp}

Enfoque la textura. Especifica la nitidez que se aplicará al procesar este material.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Sin perfeccionamiento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Perfeccionamiento normal (final). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 nitidez alternativa (al principio). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Más nitidez (temprana y tardía). </p> </td> 
 </tr> 
</table>

`sharp=1` aplica nitidez una vez procesado el material;  `sharp=2` aplica nitidez después de la escala inicial de la textura, pero antes de que se transforme en escena;  `sharp=3` aplica nitidez tanto antes como después de la transformación.

El algoritmo de perfeccionamiento y la cantidad de perfeccionamiento y otros parámetros USM (máscara de enfoque) se controlan mediante la plantilla de material predeterminada que proporciona la viñeta o con `rs=`.

## Propiedades {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Atributo de material. Ignorado por materiales de color sólido.

## Predeterminado {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, si el material está basado en una entrada de catálogo, en caso contrario  `attribute::Sharp`.

## Véase también {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catálogo::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e),  [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
