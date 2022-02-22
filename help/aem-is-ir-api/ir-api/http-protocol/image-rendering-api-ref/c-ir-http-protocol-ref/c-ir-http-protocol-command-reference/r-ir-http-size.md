---
title: tamaño
description: Tamaño de la calcomanía. Especifica el tamaño de un material de calco.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---

# tamaño{#size}

Tamaño de la calcomanía. Especifica el tamaño de un material de calco.

` size= *`anchura,altura`*[ *`,grosor`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> anchura, altura </span> </p> </td> 
  <td class="stentry"> <p>Tamaño del objeto calc en unidades de coordenadas de escena (normalmente pulgadas) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> grosor </span> </p> </td> 
  <td class="stentry"> <p>Grosor del objeto calc en unidades de coordenadas de escena (normalmente pulgadas) (real). </p> </td> 
 </tr> 
</table>

Si la anchura o la altura no son 0, la imagen se amplía a las dimensiones exactas especificadas y no se conserva la relación de aspecto de la imagen. Si se define cualquiera de los valores como 0, se conserva la relación de aspecto de la imagen.

If *`thickness`* se especifica, se representa una sombra paralela si el objeto de viñeta define un vector de luz adecuado. Establezca *`thickness`* a 0 para desactivar el procesamiento de sombras paralelas.

## Propiedades {#section-818e01e91fed4015951189c818ef28d8}

Atributo de material. Solo se usa en calcomanías; ignorado por todos los demás materiales. `res=` se ignora si la anchura o la altura son buenas a 0. Los valores no deben ser negativos.

## Predeterminado {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` si el material de calco se basa en una entrada de catálogo; otherwise `size=0,0,0`. El tamaño del calco se calcula a partir de `res=` if *`wid`* y *`hei`* no se especifican o se establecen en 0. No se representa ninguna sombra paralela si *`thickness`* no se ha especificado o establecido en 0.

## Ejemplo {#section-04fdc2b60b9e4071b672bf6a913738ad}

Un MSS para un calco, cuyo tamaño se basa en la resolución, girado en 20 grados en el sentido de las agujas del reloj y con un espesor de 2,5 pulgadas, para un efecto de sombra de caída adecuado:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Véase también {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordenadas de escenas](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [atributo:Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
