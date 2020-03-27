---
description: perfil de color de salida predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta en escala de grises cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color en escala de grises especificados con varios comandos de servicio de imágenes, como color=.
seo-description: perfil de color de salida predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta en escala de grises cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color en escala de grises especificados con varios comandos de servicio de imágenes, como color=.
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Scene7 Image Serving - Image Rendering API
uuid: a7d40114-f91f-4637-bb49-5b06b9ce846d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileGray{#iccprofilegray}

perfil de color de salida predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta en escala de grises cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color en escala de grises especificados con varios comandos de servicio de imágenes, como color=.

## Propiedades {#section-03f090ee2acf4537b83f78840d23ecab}

Cadena de texto. Si se especifica, debe ser un valor válido `icc::Name` del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o bien una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC referenciado debe ser un perfil en escala de grises.

## Predeterminado {#section-95ba3ab15edc4259b657c6ebf8783d61}

Se hereda de `default::IccProfileGray` si no está definida o si está vacía.

## Véase también {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
