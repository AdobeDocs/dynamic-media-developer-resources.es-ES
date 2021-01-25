---
description: PERFIL de color de salida predeterminado RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta RGB cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color RGB especificados con varios comandos de servicio de imágenes, como color=.
seo-description: PERFIL de color de salida predeterminado RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta RGB cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color RGB especificados con varios comandos de servicio de imágenes, como color=.
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 40606151-d5fa-4ae5-b6f0-e811bfea4691
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# IccProfileRgb{#iccprofilergb}

PERFIL de color de salida predeterminado RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta RGB cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color RGB especificados con varios comandos de servicio de imágenes, como color=.

## Propiedades {#section-3dd55c954d4d4ad4bb715ed7cee31025}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil RGB.

## Predeterminado {#section-dfe08dd7b851453ca816623a4179955b}

Se hereda de `default::IccProfileRgb` si no está definida o si está vacía.

## Véase también {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [atributo::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2),  [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
