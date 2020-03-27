---
description: perfil de color de entrada predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material en escala de grises que no incrustan un perfil de color.
seo-description: perfil de color de entrada predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material en escala de grises que no incrustan un perfil de color.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: e05d1185-ffd6-4c04-a2b8-52228beae37d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcGray{#iccprofilesrcgray}

perfil de color de entrada predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material en escala de grises que no incrustan un perfil de color.

## Propiedades {#section-97923d8561b845309442d57d017d91a4}

Cadena de texto. Si se especifica, debe ser un valor válido `icc::Name` del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o bien una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC referenciado debe ser un perfil en escala de grises.

## Predeterminado {#section-02c52805ee13483dba7878aeab51f889}

Se hereda de `default::IccProfileSrcGray` si no está definida o si está vacía. Si `attribute::IccProfileSrcGray` no se resuelve en un perfil válido, `attribute::IccProfileGray` se utilizará en su lugar.

## Véase también {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [atributo::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
