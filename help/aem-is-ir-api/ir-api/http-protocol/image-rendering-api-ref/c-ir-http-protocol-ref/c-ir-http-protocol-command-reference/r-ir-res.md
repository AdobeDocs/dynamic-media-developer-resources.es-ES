---
title: res
description: Resolución de material. Especifica la resolución de la textura repetible o la imagen de calcomanía.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f207355d-5819-47fc-bda5-27a411449569
TQID: 'https://experienceleague.adobe.com/F-ow5-VFHuZFZ7F-v3csRKFxospULbiR2bDpqbvUaYc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 105
ht-degree: 2%

---

# res{#res}

Resolución de material. Especifica la resolución de la textura repetible o la imagen de calcomanía.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Resolución; unidades de resolución de material (normalmente píxeles por pulgada) (real). </p> </td> 
 </tr> 
</table>

Si hay un material de calcomanía, `size=` prevalece si se especifican `size=` y `res=`.

## Propiedades {#section-6a458ddc202f46e0b668c9f040a65cef}

Atributo de material. Ignorado por materiales de color sólido. Solo por los materiales de revestimiento de gabinete y ventana solo si también se utiliza una textura.

## Predeterminado {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, si el material se basa en una entrada de catálogo; en caso contrario, `attribute::Resolution`, si `res= is` no se ha especificado o establecido en un valor menor o igual que 0.

## Véase también {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Resolución de material](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b), [tamaño=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988), [catálogo::Resolución](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7), [atributo::Resolución](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
