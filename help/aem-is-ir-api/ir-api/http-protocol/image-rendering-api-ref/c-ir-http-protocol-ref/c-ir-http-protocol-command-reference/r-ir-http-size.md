---
title: tamaño
description: Tamaño de calco. Especifica el tamaño del material de una calcomanía.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 2%

---

# tamaño{#size}

Tamaño de calco. Especifica el tamaño del material de una calcomanía.

` size= *`ancho,alto`*[ *`,grosor`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> anchura, altura </span> </p> </td> 
  <td class="stentry"> <p>Tamaño del objeto de calco en unidades de coordenadas de escena (normalmente pulgadas) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> grosor </span> </p> </td> 
  <td class="stentry"> <p>Grosor del objeto de calcomanía en unidades de coordenadas de escena (normalmente pulgadas) (real). </p> </td> 
 </tr> 
</table>

Si ni la anchura ni la altura son 0, la imagen se escala a las dimensiones especificadas exactas y no se conserva la proporción de aspecto de la imagen. Al establecer cualquiera de los valores en 0 se conserva la relación de aspecto de la imagen.

If *`thickness`* se especifica, se representa una sombra paralela si el objeto de viñeta define un vector de luz adecuado. Establecer *`thickness`* a 0 para deshabilitar la representación de sombras paralelas.

## Propiedades {#section-818e01e91fed4015951189c818ef28d8}

Atributo de material. Solo se usa por calcomanías; ignorado por todos los demás materiales. `res=` se ignora si width o height son buenas a 0. Los valores no deben ser negativos.

## Predeterminado {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` si el material de la calcomanía se basa en una entrada del catálogo; de lo contrario `size=0,0,0`. El tamaño de la calcomanía se calcula a partir de `res=` if *`wid`* y *`hei`* no se han especificado o se han establecido en 0. No se representa ninguna sombra paralela si *`thickness`* no se ha especificado o establecido en 0.

## Ejemplo {#section-04fdc2b60b9e4071b672bf6a913738ad}

Un SMS para una calcomanía, cuyo tamaño se basa en la resolución, girada 20 grados en el sentido de las agujas del reloj y tiene un grosor de 2,5 pulgadas, para un efecto de sombra paralela adecuado:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Véase también {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordenadas de escena](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
