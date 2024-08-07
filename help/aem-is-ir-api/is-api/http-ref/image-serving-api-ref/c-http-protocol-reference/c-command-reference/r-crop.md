---
title: recorte
description: Recortar imagen. Especifica una región de recorte rectangular, expresada en píxeles o normalizada en relación con la imagen de origen de resolución completa o la imagen de máscara.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# recorte{#crop}

Recortar imagen. Especifica una región de recorte rectangular, expresada en píxeles o normalizada en relación con la imagen de origen de resolución completa o la imagen de máscara.

`crop= *`coord`*, *`size`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento de píxeles desde la esquina superior izquierda de la imagen de origen hasta la parte superior izquierda del recorte recto (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento normalizado desde la parte superior izquierda de la imagen de origen hasta la parte superior izquierda del recorte recto (real, real). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> tamaño</span></span> </p></td> 
  <td class="stentry"> <p>Tamaño del recorte recto en píxeles (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>El tamaño normalizado del recorte es relativo al tamaño de la imagen de origen (real, real). </p></td> 
 </tr> 
</table>

También se puede utilizar para extender la imagen más allá de sus límites especificando valores negativos de x, y o anchura, valores de altura superiores a la anchura y altura de la imagen. En este caso, el área extendida es completamente transparente (a menos que se especifique `bgColor=`).

## Propiedades {#section-632e0405bb9940679b5f8b1c10e0902e}

Atributo de imagen/máscara de Source. Se aplica a la imagen de origen de la capa 0 si `layer=comp`. Ignorado por capas que no están asociadas a una imagen o máscara de origen.

## Predeterminado {#section-41f62d386c664f77952bc22e7286bb88}

Imagen completa ( `cropN=0,0,1,1`).

## Ejemplos {#section-2c99b481c0a04321979a3b522aa295d1}

**Recorte un 10% a la izquierda y un 10% a la derecha:**

`…&cropN=0.1,0,0.8,1&…`

**Recortar un 20% del borde inferior de una imagen:**

`…&cropN=0,0,1,0.8&…`

## Véase también {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[rutaDeAccesoDeRecorte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anclaje=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extensión=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
