---
description: Tipo de miniatura. Describe cómo se va a generar una miniatura para esta imagen.
seo-description: Tipo de miniatura. Describe cómo se va a generar una miniatura para esta imagen.
seo-title: ThumbType
solution: Experience Manager
title: ThumbType
topic: Scene7 Image Serving - Image Rendering API
uuid: b737b5a4-ad6d-4a9c-b48f-81cf170dd210
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# ThumbType{#thumbtype}

Tipo de miniatura. Describe cómo se va a generar una miniatura para esta imagen.

Se admiten los siguientes tipos de miniaturas:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Recortar (1) </p></td> 
  <td class="stentry"> <p>Recorte la imagen con la proporción de aspecto de la miniatura. A menos que la proporción de aspecto del rectángulo de miniaturas y la imagen sea exactamente la misma, una parte de la imagen se recorta para garantizar que todo el rectángulo de miniaturas se rellene con datos de imagen. El rectángulo de recorte se coloca en la imagen utilizando el atributo <span class="codeph">::ThumbHorizAlign</span> y el atributo <span class="codeph">::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Ajustar (2) </p></td> 
  <td class="stentry"> <p>Ajuste toda la imagen en el rectángulo de miniaturas. La imagen se coloca dentro del rectángulo de miniaturas utilizando el atributo <span class="codeph">::ThumbHorizAlign</span> y el atributo <span class="codeph">::ThumbVertAlign</span>, y cualquier espacio adicional se rellena con el atributo <span class="codeph">::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Textura (3) </p></td> 
  <td class="stentry"> <p>Recorte la imagen según la resolución. La imagen se escala por la proporción de <span class="codeph"> catálogo::ThumbRes</span> a <span class="codeph"> catálogo::Resolution</span>. Si la imagen resultante es más grande que la miniatura, se recorta para ajustarse, si la imagen escalada es más pequeña que la miniatura, el área restante se rellena con el atributo <span class="codeph">::ThumbBkgColor</span>. <span class="codeph"> atributo::</span> ThumbHorizAlignand  <span class="codeph"> attribute::</span> ThumbVertAlignare se utilizan para determinar la posición del rectángulo de recorte dentro de una imagen o posición más grande de una imagen más pequeña dentro de la miniatura. </p></td> 
 </tr> 
</table>

Los clientes solicitan miniaturas de imágenes con solicitudes `req=tmb`.

## Propiedades {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Valor de enumeración. Los valores válidos son 1, 2 o 3, que corresponden a los tipos de recorte, ajuste y textura, respectivamente.

## Predeterminado {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` se utiliza si el campo no está presente, si el valor es 0 o si el campo está vacío.

## Véase también {#section-fc1a79d3e6274b4381a17da159649a07}

[atributo::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ,  [atributo::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e),  [atributo::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691),  [atributo::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f),  [Catálogo::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69),  [ ](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)  [ ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)  [atributo::Resolution, escala de miniatura, catálogo de miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
