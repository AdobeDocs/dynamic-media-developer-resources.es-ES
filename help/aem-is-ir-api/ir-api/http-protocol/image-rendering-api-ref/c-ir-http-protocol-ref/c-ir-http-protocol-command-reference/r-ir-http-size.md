---
description: Tamaño de la calcomanía. Especifica el tamaño de un material de calco.
seo-description: Tamaño de la calcomanía. Especifica el tamaño de un material de calco.
seo-title: tamaño
solution: Experience Manager
title: tamaño
uuid: b82f3429-3d84-4707-8126-d390239df9a2
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 3%

---


# tamaño{#size}

Tamaño de la calcomanía. Especifica el tamaño de un material de calco.

` size= *`anchura,altura`*[ *`,grosor`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> anchura, altura  </span> </p> </td> 
  <td class="stentry"> <p>Tamaño del objeto calc en unidades de coordenadas de escena (normalmente pulgadas) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> grosor  </span> </p> </td> 
  <td class="stentry"> <p>Grosor del objeto calc en unidades de coordenadas de escena (normalmente pulgadas) (real). </p> </td> 
 </tr> 
</table>

Si ni la anchura ni la altura son 0, la imagen se escala a las dimensiones exactas especificadas y no se conserva la relación de aspecto de la imagen. Si se define cualquiera de los valores como 0, se conserva la relación de aspecto de la imagen.

Si se especifica *`thickness`*, se representa una sombra paralela si el objeto de viñeta define un vector de luz adecuado. Establezca *`thickness`* en 0 para deshabilitar el procesamiento de sombras desplegables.

## Propiedades {#section-818e01e91fed4015951189c818ef28d8}

Atributo de material. Solo se usa en calcomanías; ignorado por todos los demás materiales. `res=` se ignora si la anchura o la altura son buenas a 0. Los valores no deben ser negativos.

## Predeterminado {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` si el material de calco se basa en una entrada de catálogo; de lo contrario  `size=0,0,0`. El tamaño de calcomanía se calcula a partir de `res=` si *`wid`* y *`hei`* no se especifican o se establecen en 0. No se procesa ninguna sombra de colocación si no se especifica *`thickness`* o se establece en 0.

## Ejemplo {#section-04fdc2b60b9e4071b672bf6a913738ad}

Un MSS para un calco, cuyo tamaño se basa en la resolución, girado en 20 grados en el sentido de las agujas del reloj y con un espesor de 2,5 pulgadas, para un efecto de sombra de caída adecuado:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Véase también {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordenadas](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1) de escena,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04),  [atributo::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
