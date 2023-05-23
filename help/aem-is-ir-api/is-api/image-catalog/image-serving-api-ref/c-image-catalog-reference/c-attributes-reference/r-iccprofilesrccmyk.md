---
title: IccProfileSrcCmyk
description: Perfil de color de entrada predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen CMYK que no incrustan un perfil de color y para determinados valores de color CMYK especificados con varios comandos del servicio de imágenes, como color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Perfil de color de entrada predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen CMYK que no incrustan un perfil de color y para determinados valores de color CMYK especificados con varios comandos del servicio de imágenes, como color=.

## Propiedades {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Cadena de texto. Si se especifica, debe ser un válido `icc::Name` valor del mapa de perfil ICC de este catálogo de imágenes, del catálogo predeterminado o una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC referenciado debe ser un perfil CMYK.

## Predeterminado {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Heredado de `default::IccProfileSrcCmyk` si no se define o si está vacío. If `attribute::IccProfileSrcCmyk` no se resuelve en un perfil válido, `attribute::IccProfileCmyk` se utiliza en su lugar.

## Véase también {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
