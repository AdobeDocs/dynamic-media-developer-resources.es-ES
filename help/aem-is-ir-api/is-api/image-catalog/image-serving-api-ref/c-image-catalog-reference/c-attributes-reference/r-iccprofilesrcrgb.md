---
description: PERFIL de color de entrada RGB predeterminado. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen RGB que no incrustan un perfil de color y para determinados valores de color RGB especificados con varios comandos de servicio de imágenes, como color=.
seo-description: PERFIL de color de entrada RGB predeterminado. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen RGB que no incrustan un perfil de color y para determinados valores de color RGB especificados con varios comandos de servicio de imágenes, como color=.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

PERFIL de color de entrada RGB predeterminado. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen RGB que no incrustan un perfil de color y para determinados valores de color RGB especificados con varios comandos de servicio de imágenes, como color=.

## Propiedades {#section-3cd753196959462e9e674dab0b033d08}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil RGB.

## Predeterminado {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Se hereda de `default::IccProfileSrcRgb` si no está definida o si está vacía. Si `attribute::IccProfileSrcRgb` no se resuelve en un perfil válido, se utiliza `attribute::IccProfileRgb` en su lugar.

## Véase también {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [atributo::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df),  [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
