---
description: Recortar imagen. Especifica una zona de recorte rectangular, expresada en píxeles o normalizada en relación con la imagen de origen o la imagen de máscara de resolución completa.
solution: Experience Manager
title: recorte
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 3%

---

# recorte{#crop}

Recortar imagen. Especifica una zona de recorte rectangular, expresada en píxeles o normalizada en relación con la imagen de origen o la imagen de máscara de resolución completa.

`crop= *``*, *`coordsize`*`

`cropN= *``*, *`codeNameN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento de píxeles desde la esquina superior izquierda de la imagen de origen hasta la esquina superior izquierda del recorte (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> codeN</span></span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento normalizado desde la parte superior izquierda de la imagen de origen hasta la parte superior izquierda del recorte recto (real, real). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p></td> 
  <td class="stentry"> <p>Tamaño del anillo de recorte en píxeles (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Tamaño normalizado del anillo de recorte en relación con el tamaño de la imagen de origen (real, real). </p></td> 
 </tr> 
</table>

También se puede utilizar para ampliar la imagen más allá de sus límites especificando valores negativos de x, y y y/o de ancho, valores de altura más grandes que el ancho y la altura de la imagen. En este caso, el área extendida es totalmente transparente (a menos que se especifique `bgColor=`).

## Propiedades {#section-632e0405bb9940679b5f8b1c10e0902e}

Atributo imagen/máscara de origen. Se aplica a la imagen de origen de capa 0 si `layer=comp`. Ignoradas por capas que no están asociadas a una imagen o máscara de origen.

## Predeterminado {#section-41f62d386c664f77952bc22e7286bb88}

Toda la imagen ( `cropN=0,0,1,1`).

## Ejemplos {#section-2c99b481c0a04321979a3b522aa295d1}

**Recorte un 10% de la izquierda y un 10% de la derecha:**

`…&cropN=0.1,0,0.8,1&…`

**Recortar un 20% del borde inferior de una imagen:**

`…&cropN=0,0,1,0.8&…`

## Véase también {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [cropPathColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
