---
title: Tamaño
description: Tamaño de calco. Anchura, altura y grosor de un objeto de material de calcomanía.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
TQID: 'https://experienceleague.adobe.com/HLyEmmOch9kiHQ3sqpvHCQiHOBltjQcsZaDu0na1-Ww'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 217
ht-degree: 5%

---

# Tamaño{#size}

Tamaño de calco. Anchura, altura y grosor de un objeto de material de calcomanía.

## Propiedades {#section-967bf1112eec4032a91ed0c8a7b10a07}

Tres números reales separados por comas. No debe ser negativo. Establezca los valores no utilizados en 0. Pueden omitirse los ceros finales.

Especifique la anchura y la altura únicamente si la imagen debe estirarse para ajustarse al tamaño especificado (la proporción de aspecto puede cambiar). Defina la anchura o la altura para escalar la imagen proporcionalmente. Establezca anchura y altura en 0 para usar `catalog::Resolution` y determinar el tamaño del objeto.

Proporcione un valor de grosor para añadir una sombra paralela al objeto de calco. Opcional para los materiales de calcomanía, ignorada por todos los demás materiales.

## Predeterminado {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Esto indica que el tamaño de la calcomanía se debe determinar en función de catalog::Resolution y que el objeto no tiene grosor (por lo tanto, no se representa ninguna sombra paralela).

## Ejemplos {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>La calcomanía es forzada a 12x3 pulgadas de tamaño y no tiene espesor (esto es, sin sombra de gota). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>La calcomanía tiene 5 pulgadas de ancho, la altura está determinada por la proporción de aspecto de la imagen y se procesa una sombra paralela en función de un grosor de 1 pulgada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>La anchura y altura de la calcomanía viene determinada por catalog::Resolution y tiene un grosor de ½ pulgada. </p></td> 
 </tr> 
</table>

## Véase también {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)

