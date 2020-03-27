---
description: perfil de color de salida predeterminado RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta RGB cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color RGB especificados con varios comandos de procesamiento de imágenes, como bgc= y color=.
seo-description: perfil de color de salida predeterminado RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta RGB cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color RGB especificados con varios comandos de procesamiento de imágenes, como bgc= y color=.
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fe63607-c328-468a-aa55-0c4d16cf9f0f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileRgb{#iccprofilergb}

perfil de color de salida predeterminado RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta RGB cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color RGB especificados con varios comandos de procesamiento de imágenes, como bgc= y color=.

## Propiedades {#section-b4a1bd92e99047479a5036413525a6d9}

Cadena de texto. Si se especifica, debe ser un valor válido `icc::Name` del mapa de perfiles ICC de este catálogo de material o del catálogo predeterminado, o bien una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil RGB.

## Predeterminado {#section-5809772f8e96438ab7626d323c66a4ba}

Se hereda de `default::IccProfileRgb` si no está definida o si está vacía.

## Véase también {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [atributo::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
