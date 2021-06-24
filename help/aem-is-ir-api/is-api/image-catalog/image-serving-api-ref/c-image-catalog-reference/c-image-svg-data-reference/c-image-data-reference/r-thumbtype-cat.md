---
description: Tipo de miniatura. Describe cómo se va a generar una miniatura para esta imagen.
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 1%

---

# ThumbType{#thumbtype}

Tipo de miniatura. Describe cómo se va a generar una miniatura para esta imagen.

Se admiten los siguientes tipos de miniaturas:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Recorte (1) </p></td> 
  <td class="stentry"> <p>Recorte la imagen hasta la proporción de aspecto de la miniatura. A menos que la proporción de aspecto del rectángulo de la miniatura y la imagen sea exactamente la misma, una parte de la imagen se recorta para garantizar que todo el rectángulo de la miniatura se rellene con datos de imagen. El rectángulo de recorte se coloca en la imagen utilizando el atributo <span class="codeph">::ThumbHorizAlign</span> y el atributo <span class="codeph">::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Ajuste (2) </p></td> 
  <td class="stentry"> <p>Ajuste toda la imagen en el rectángulo de miniaturas. La imagen se coloca dentro del rectángulo de la miniatura utilizando el atributo <span class="codeph">::ThumbHorizAlign</span> y el atributo <span class="codeph">::ThumbVertAlign</span>, y cualquier espacio adicional se rellena con el atributo <span class="codeph">::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Textura (3) </p></td> 
  <td class="stentry"> <p>Recorte la imagen según la resolución. La imagen se escala por la proporción de <span class="codeph"> catálogo::ThumbRes</span> a <span class="codeph"> catálogo::Resolution</span>. Si la imagen resultante es más grande que la miniatura, se recorta para que quepa, si la imagen escalada es más pequeña que la miniatura, el área restante se rellena con el atributo <span class="codeph">::ThumbBkgColor</span>. <span class="codeph"> atributo::</span> ThumbHorizAlignand  <span class="codeph"> attribute::</span> ThumbVertAlignare se utilizan para determinar la posición del rectángulo de recorte dentro de una imagen o posición más grande de una imagen más pequeña dentro de la miniatura. </p></td> 
 </tr> 
</table>

Los clientes solicitan miniaturas de imágenes con solicitudes `req=tmb`.

## Propiedades {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Valor Enum. Los valores válidos son 1, 2 o 3, que corresponden a los tipos Recortar, Ajustar y Textura, respectivamente.

## Predeterminado {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` se utiliza si el campo no está presente, si el valor es 0 o si el campo está vacío.

## Véase también {#section-fc1a79d3e6274b4381a17da159649a07}

[atributo::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ,  [atributo::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e),  [atributo::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691),  [atributo::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f),  [catálogo::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69),  [catálogo::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1),  [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [Escalado de miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
