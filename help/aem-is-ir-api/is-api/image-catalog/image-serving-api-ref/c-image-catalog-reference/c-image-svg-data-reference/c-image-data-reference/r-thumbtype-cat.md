---
description: Tipo de miniatura. Describe cómo se va a generar una miniatura para esta imagen.
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# ThumbType{#thumbtype}

Tipo de miniatura. Describe cómo se va a generar una miniatura para esta imagen.

Se admiten los siguientes tipos de miniaturas:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Recorte (1) </p></td> 
  <td class="stentry"> <p>Recortar la imagen según la proporción de aspecto de la miniatura. A menos que la proporción de aspecto del rectángulo de miniaturas y la imagen sea exactamente la misma, se recorta una parte de la imagen para garantizar que todo el rectángulo de miniaturas se rellene con datos de imagen. El rectángulo de recorte se coloca en la imagen usando <span class="codeph"> attribute::ThumbHorizAlign</span> y <span class="codeph"> attribute::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Cabeza (2) </p></td> 
  <td class="stentry"> <p>Ajuste toda la imagen en el rectángulo de miniaturas. La imagen se coloca dentro del rectángulo de miniaturas usando <span class="codeph"> attribute::ThumbHorizAlign</span> y <span class="codeph"> attribute::ThumbVertAlign</span>, y cualquier espacio adicional se rellena con <span class="codeph"> attribute::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Textura (3) </p></td> 
  <td class="stentry"> <p>Recorte la imagen en función de la resolución. La imagen se ha escalado según la proporción del catálogo <span class="codeph">::ThumbRes</span> a <span class="codeph"> catalog::Resolution</span>. Si la imagen resultante es más grande que la miniatura, se recorta para ajustarse; si la imagen a escala es más pequeña que la miniatura, el área restante se rellena con <span class="codeph"> atributo::ThumbBkgColor</span>. <span class="codeph"> attribute::ThumbHorizAlign</span> y <span class="codeph"> attribute::ThumbVertAlign</span> se utilizan para determinar la posición del rectángulo de recorte dentro de una imagen más grande o la posición de una imagen más pequeña dentro de la miniatura. </p></td> 
 </tr> 
</table>

Los clientes solicitan miniaturas de imágenes con `req=tmb` solicitudes.

## Propiedades {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Valor de enumeración. Los valores válidos son 1, 2 o 3, que corresponden a los tipos Recortar, Ajustar y Textura, respectivamente.

## Predeterminado {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` se usa si el campo no está presente, si el valor es 0 o si el campo está vacío.

## Véase también {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) , [attribute::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e), [attribute::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691), [attribute::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f), [catálogo::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69), [catálogo::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Escalado de miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
