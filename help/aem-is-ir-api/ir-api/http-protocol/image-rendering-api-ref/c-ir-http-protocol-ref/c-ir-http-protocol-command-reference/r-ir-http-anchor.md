---
title: delimitador
description: Anclaje de imagen (punto interactivo). Especifica el punto de anclaje de textura (punto interactivo) del material repetible de textura o calcomanía.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# delimitador{#anchor}

Anclaje de imagen (punto interactivo). Especifica el punto de anclaje de textura (punto interactivo) del material repetible de textura o calcomanía.

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Desplazamiento de píxel desde la esquina superior izquierda de la imagen de origen (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Desplazamiento normalizado desde el centro de la imagen de origen (real, real). </p></td> 
 </tr> 
</table>

Se aplica una textura repetible a un objeto de viñeta, de modo que el punto de ancla de la textura ( `anchor=`) se encuentra en el punto de origen de la textura del objeto.

Se aplica una imagen de calcomanía a un objeto de viñeta, de modo que el punto de anclaje de calcomanía se encuentre en el punto de origen de la calcomanía del objeto. La posición de la calcomanía se puede ajustar aún más utilizando el `pos=` comando.

`anchorN=0,0` Sitúa el anclaje de la imagen en el centro de la imagen de origen. `anchorN=-0.5,-0.5` o `anchor=0,0` se encuentra en la esquina superior izquierda y `anchorN=0.5,0.5` se encuentra en la esquina inferior derecha de la imagen de origen.

## Propiedades {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Atributo de material**. Ignorado si `align=2`, o si el material no es una textura repetible, un papel tapiz, ni una calcomanía.

## Predeterminado {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, si el material se basa en una entrada de catálogo. De lo contrario, `anchor=0,0` (la esquina superior izquierda de la imagen) para texturas y fondos de pantalla repetibles, y `anchorN=0,0` (el centro de la imagen) para calcas.

## Véase también {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
