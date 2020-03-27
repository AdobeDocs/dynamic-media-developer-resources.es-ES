---
description: perfil de color de entrada predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen CMYK que no incrustan un perfil de color y para determinados valores de color CMYK especificados con varios comandos de servicio de imágenes, como color=.
seo-description: perfil de color de entrada predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen CMYK que no incrustan un perfil de color y para determinados valores de color CMYK especificados con varios comandos de servicio de imágenes, como color=.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 5f1c2eb6-7f32-4603-9587-d8c1f6a72bb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

perfil de color de entrada predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen CMYK que no incrustan un perfil de color y para determinados valores de color CMYK especificados con varios comandos de servicio de imágenes, como color=.

## Propiedades {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Cadena de texto. Si se especifica, debe ser un valor válido `icc::Name` del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o bien una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil CMYK.

## Predeterminado {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Se hereda de `default::IccProfileSrcCmyk` si no está definida o si está vacía. Si `attribute::IccProfileSrcCmyk` no se resuelve en un perfil válido, `attribute::IccProfileCmyk` se utiliza en su lugar.

## Véase también {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
