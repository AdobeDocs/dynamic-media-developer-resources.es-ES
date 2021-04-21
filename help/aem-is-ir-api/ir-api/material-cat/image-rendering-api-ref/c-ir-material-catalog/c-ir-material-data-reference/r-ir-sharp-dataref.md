---
description: Enfoque. El atributo de perfeccionamiento determina cuándo se enfoca el material durante el procesamiento.
solution: Experience Manager
title: Nitidez
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 10%

---


# Enfocado{#sharp}

Enfoque. El atributo de perfeccionamiento determina cuándo se enfoca el material durante el procesamiento.

El tipo y la cantidad de nitidez se controlan mediante la viñeta a través de una plantilla de material predeterminada o con `catalog::RenderSettings`.

## Propiedades {#section-aac81b1a611b4bca90b8544eae7896df}

Enum.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Sin perfeccionamiento. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Perfilado normal (después de la transformación). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Afilado alternativo (antes de la transformación). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Más nitidez (tanto antes como después de la transformación). </p></td> 
 </tr> 
</table>

Ignorado por materiales de color sólido, opcional para todos los demás materiales.

## Predeterminado {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` se utiliza si el campo no está presente, si está vacío o si el valor no es una de las opciones admitidas.

## Véase también {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[atributo::Enfoque](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) ,  [catálogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd),  [afilado=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
