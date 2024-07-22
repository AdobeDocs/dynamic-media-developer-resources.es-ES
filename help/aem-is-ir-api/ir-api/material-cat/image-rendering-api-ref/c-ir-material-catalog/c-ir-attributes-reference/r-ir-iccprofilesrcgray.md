---
title: IccProfileSrcGray
description: Perfil de color de entrada predeterminado en escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material en escala de grises que no incrustan un perfil de color.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# IccProfileSrcGray{#iccprofilesrcgray}

Perfil de color de entrada predeterminado en escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material en escala de grises que no incrustan un perfil de color.

## Propiedades {#section-97923d8561b845309442d57d017d91a4}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes, del catálogo predeterminado o una ruta de acceso de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil en escala de grises.

## Predeterminado {#section-02c52805ee13483dba7878aeab51f889}

Se hereda de `default::IccProfileSrcGray` si no se ha definido o está vacío. Si `attribute::IccProfileSrcGray` no se resuelve en un perfil válido, se utiliza `attribute::IccProfileGray` en su lugar.

## Véase también {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [atributo::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
