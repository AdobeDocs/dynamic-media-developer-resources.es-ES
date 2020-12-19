---
description: Anclaje de imagen (zona interactiva). Especifica el punto de anclaje de textura (punto interactivo) de la textura repetible o del material de calado.
seo-description: Anclaje de imagen (zona interactiva). Especifica el punto de anclaje de textura (punto interactivo) de la textura repetible o del material de calado.
seo-title: delimitador
solution: Experience Manager
title: delimitador
topic: Scene7 Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# delimitador{#anchor}

Anclaje de imagen (zona interactiva). Especifica el punto de anclaje de textura (punto interactivo) de la textura repetible o del material de calado.

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Desplazamiento de píxeles desde la esquina superior izquierda de la imagen de origen (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Desplazamiento normalizado desde el centro de la imagen de origen (real, real). </p></td> 
 </tr> 
</table>

Se aplica una textura repetible a un objeto de viñeta, de modo que el punto de anclaje de textura ( `anchor=`) se encuentra en el punto de origen de textura del objeto.

Se aplica una imagen de calcomanía a un objeto de viñeta, de modo que el punto de ancla de calcomanía se encuentra en el punto de origen de calcomanía del objeto. La posición de calcomanía se puede ajustar con el comando `pos=`.

`anchorN=0,0` coloca el anclaje de imagen en el centro de la imagen de origen. `anchorN=-0.5,-0.5` o  `anchor=0,0` está en la esquina superior izquierda y  `anchorN=0.5,0.5` se encuentra en la esquina inferior derecha de la imagen de origen.

## Propiedades {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Atributo** Material. Se omite si `align=2` o si el material no es una textura repetible, un papel tapiz o una calcomanía.

## Predeterminado {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, si el material está basado en una entrada de catálogo. De lo contrario, `anchor=0,0` (la esquina superior izquierda de la imagen) para texturas y fondos de pantalla repetibles y `anchorN=0,0` (el centro de la imagen) para calcomanías.

## Véase también {#section-b18bf0b035644ca5aedebbc64373718e}

[catálogo::Anclaje](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [alinear=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
