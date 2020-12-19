---
description: Recortar imagen. Especifica una región de recorte rectangular, expresada en píxeles o normalizada en relación con la imagen de origen o la imagen de máscara de resolución completa.
seo-description: Recortar imagen. Especifica una región de recorte rectangular, expresada en píxeles o normalizada en relación con la imagen de origen o la imagen de máscara de resolución completa.
seo-title: recorte
solution: Experience Manager
title: recorte
topic: Scene7 Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 3%

---


# recorte{#crop}

Recortar imagen. Especifica una región de recorte rectangular, expresada en píxeles o normalizada en relación con la imagen de origen o la imagen de máscara de resolución completa.

`crop= *``*, *`coordsize`*`

`cropN= *``*, *`codeNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento de píxeles desde la esquina superior izquierda de la imagen de origen hasta la parte superior izquierda del rectángulo de recorte (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> codeN</span></span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento normalizado desde la parte superior izquierda de la imagen de origen hasta la parte superior izquierda del rectángulo de recorte (real, real). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p></td> 
  <td class="stentry"> <p>Tamaño del rectángulo de recorte en píxeles (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Tamaño normalizado del rectángulo de recorte en relación con el tamaño de la imagen de origen (real, real). </p></td> 
 </tr> 
</table>

También se puede utilizar para extender la imagen más allá de sus límites especificando valores negativos de altura (x, y) y/o de anchura (width) mayores que el ancho y el alto de la imagen. En este caso, el área extendida es completamente transparente (a menos que se especifique `bgColor=`).

## Propiedades {#section-632e0405bb9940679b5f8b1c10e0902e}

Atributo de imagen/máscara de origen. Se aplica a la imagen de origen de capa 0 si `layer=comp`. Omitido por capas que no están asociadas con una imagen o máscara de origen.

## Predeterminado {#section-41f62d386c664f77952bc22e7286bb88}

Imagen completa ( `cropN=0,0,1,1`).

## Ejemplos {#section-2c99b481c0a04321979a3b522aa295d1}

**Recorte 10% de la izquierda y 10% de la derecha:**

`…&cropN=0.1,0,0.8,1&…`

**Recorte un 20 % del borde inferior de una imagen:**

`…&cropN=0,0,1,0.8&…`

## Véase también {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [cutPathbgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
