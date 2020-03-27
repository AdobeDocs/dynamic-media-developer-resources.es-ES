---
description: Tamaño de calcomanía. Anchura, altura y grosor de un objeto de material de calado.
seo-description: Tamaño de calcomanía. Anchura, altura y grosor de un objeto de material de calado.
seo-title: Tamaño
solution: Experience Manager
title: Tamaño
topic: Scene7 Image Serving - Image Rendering API
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Tamaño{#size}

Tamaño de calcomanía. Anchura, altura y grosor de un objeto de material de calado.

## Propiedades {#section-967bf1112eec4032a91ed0c8a7b10a07}

Tres números reales separados por comas. No debe ser negativo. Establezca los valores no utilizados en 0. Se pueden omitir ceros finales.

Especifique tanto la anchura como la altura si la imagen debe estirarse para ajustarse al tamaño especificado (la proporción de aspecto puede cambiar). Defina la anchura o la altura para escalar la imagen proporcionalmente. Defina la anchura y la altura en 0 para `catalog::Resolution`determinar el tamaño del objeto.

Proporcione un valor de grosor para agregar una sombra paralela al objeto de calcomanía. Opcional para materiales de calado, ignorados por todos los demás materiales.

## Predeterminado {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Esto indica que el tamaño de calcomanía se determina en función de la función de catálogo::Resolution y que el objeto no tiene un grosor (por lo tanto, no se representará ninguna sombra paralela).

## Ejemplos {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>La calcomanía se fuerza a 12x3 pulgadas de tamaño y no tiene espesor (esto es, no hay sombra paralela). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>La calcomanía tiene una anchura de 5 pulgadas, la altura viene determinada por la proporción de aspecto de la imagen y se representa una sombra paralela basada en un grosor de 1 pulgada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>La anchura y la altura de la calcomanía están determinadas por el catálogo::Resolution y que tiene un grosor de media pulgada. </p></td> 
 </tr> 
</table>

## Véase también {#section-31a164e781d14e92bd9d379d3c329e92}

[catálogo::Resolución](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
