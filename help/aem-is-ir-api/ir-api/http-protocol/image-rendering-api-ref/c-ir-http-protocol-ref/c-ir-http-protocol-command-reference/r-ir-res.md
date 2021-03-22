---
description: Resolución del material. Especifica la resolución de la textura repetible o la imagen de calco.
seo-description: Resolución del material. Especifica la resolución de la textura repetible o la imagen de calco.
seo-title: res
solution: Experience Manager
title: res
uuid: ae755a92-ad06-4cf2-b627-0b8b14e385c3
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---


# res{#res}

Resolución del material. Especifica la resolución de la textura repetible o la imagen de calco.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Resolución; unidades de resolución de material (normalmente píxeles por pulgada) (real). </p> </td> 
 </tr> 
</table>

En el caso de un material de calco, `size=` prevalece si se especifican `size=` y `res=`.

## Propiedades {#section-6a458ddc202f46e0b668c9f040a65cef}

Atributo de material. Ignorado por materiales de color sólido. Sólo por el gabinete y los materiales de revestimiento de ventanas sólo si se utiliza una textura.

## Predeterminado {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, si el material se basa en una entrada de catálogo, en caso contrario  `attribute::Resolution`, si  `res= is` no se especifica o se establece en un valor menor o igual que 0.

## Véase también {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Resolución](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b) de material,  [tamaño=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988),  [catálogo::Resolución](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7),  [atributo::Resolución](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
