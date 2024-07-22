---
title: IccProfileRgb
description: Perfil de color de salida predeterminado del RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta del RGB cuando no se especifique ningún espacio de color de salida con icc=. También para determinados valores de color de RGB especificados con varios comandos de procesamiento de imágenes, como bgc= y color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

Perfil de color de salida predeterminado del RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta del RGB cuando no se especifique ningún espacio de color de salida con `icc=`. También para determinados valores de color de RGB especificados con varios comandos de procesamiento de imágenes, como `bgc=` y `color=`.

## Propiedades {#section-b4a1bd92e99047479a5036413525a6d9}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de materiales, del catálogo predeterminado o una ruta de acceso de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil de RGB.

## Predeterminado {#section-5809772f8e96438ab7626d323c66a4ba}

Se hereda de `default::IccProfileRgb` si no se ha definido o está vacío.

## Véase también {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [atributo::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
