---
description: Tamaño de calcomanía. Especifica el tamaño de un material de calado.
seo-description: Tamaño de calcomanía. Especifica el tamaño de un material de calado.
seo-title: tamaño
solution: Experience Manager
title: tamaño
topic: Scene7 Image Serving - Image Rendering API
uuid: b82f3429-3d84-4707-8126-d390239df9a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 3%

---


# tamaño{#size}

Tamaño de calcomanía. Especifica el tamaño de un material de calado.

` size= *`anchura,altura`*[ *`,grosor`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> anchura, altura  </span> </p> </td> 
  <td class="stentry"> <p>Tamaño del objeto de calcomanía en unidades de coordenadas de escena (normalmente pulgadas) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> thickness  </span> </p> </td> 
  <td class="stentry"> <p>Grosor del objeto de calcomanía en unidades de coordenadas de escena (normalmente pulgadas) (real). </p> </td> 
 </tr> 
</table>

Si ni la anchura ni la altura son 0, la imagen se redimensiona con las dimensiones especificadas exactas y no se conserva la proporción de aspecto de la imagen. Si se establece cualquiera de los valores en 0, se conserva la proporción de aspecto de la imagen.

Si se especifica *`thickness`*, se procesa una sombra paralela si el objeto de viñeta define un vector de luz adecuado. Establezca *`thickness`* en 0 para deshabilitar el procesamiento de sombra paralela.

## Propiedades {#section-818e01e91fed4015951189c818ef28d8}

Atributo Material. Solo se utilizan en calcomanías; ignorados por todos los demás materiales. `res=` se omite si width o height es bueno que 0. Los valores no deben ser negativos.

## Predeterminado {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` si el material de calado se basa en una entrada de catálogo; en caso contrario  `size=0,0,0`. El tamaño de calcomanía se calcula a partir de `res=` si *`wid`* y *`hei`* no se especifican o se establecen en 0. No se procesa ninguna sombra paralela si no se especifica *`thickness`* o se establece en 0.

## Ejemplo {#section-04fdc2b60b9e4071b672bf6a913738ad}

Un MSS para una calcomanía, cuyo tamaño se basa en la resolución, girada en 20 grados en el sentido de las agujas del reloj y con un grosor de 2,5 pulgadas, para obtener un efecto de sombra paralela adecuado:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Véase también {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordenadas](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1) de escena,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04),  [atributo::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
