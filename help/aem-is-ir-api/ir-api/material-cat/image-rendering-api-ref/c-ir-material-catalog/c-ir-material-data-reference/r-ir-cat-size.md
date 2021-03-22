---
description: Tamaño de la calcomanía. Anchura, altura y grosor de un objeto de material de calco.
seo-description: Tamaño de la calcomanía. Anchura, altura y grosor de un objeto de material de calco.
seo-title: Tamaño
solution: Experience Manager
title: Tamaño
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 5%

---


# Tamaño{#size}

Tamaño de la calcomanía. Anchura, altura y grosor de un objeto de material de calco.

## Propiedades {#section-967bf1112eec4032a91ed0c8a7b10a07}

Tres números reales separados por comas. No debe ser negativo. Defina los valores no utilizados en 0. Se pueden omitir ceros finales.

Especifique tanto la anchura como la altura solo si la imagen debe estirarse para ajustarse al tamaño especificado (la relación de aspecto puede cambiar). Defina la anchura o la altura para escalar la imagen proporcionalmente. Defina tanto la anchura como la altura en 0 para utilizar `catalog::Resolution`para determinar el tamaño del objeto.

Proporcione un valor de grosor para agregar una sombra paralela al objeto calc. Opcional para materiales de calco, ignorados por todos los demás materiales.

## Predeterminado {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Esto indica que el tamaño de calcomanía se determina en función del catálogo::Resolution y que el objeto no tiene espesor (por lo tanto, no se representará ninguna sombra de colocación).

## Ejemplos {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>El calco es forzado a 12x3 pulgadas en tamaño y no tiene espesor (esto es, no tiene sombra de gota). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>El calco tiene una anchura de 5 pulgadas, la altura viene determinada por la relación de aspecto de la imagen y se representa una sombra paralela basada en un grosor de 1 pulgada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,5 </p></td> 
  <td class="stentry"> <p>La anchura y la altura de calcomanías están determinadas por el catálogo::Resolution y que tiene un grosor de medio pulgada. </p></td> 
 </tr> 
</table>

## Véase también {#section-31a164e781d14e92bd9d379d3c329e92}

[catálogo::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
