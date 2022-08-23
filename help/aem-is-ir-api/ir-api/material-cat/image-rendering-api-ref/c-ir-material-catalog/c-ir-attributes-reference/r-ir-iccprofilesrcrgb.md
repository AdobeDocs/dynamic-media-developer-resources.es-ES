---
title: IccProfileSrcRgb
description: perfil de color de entrada predeterminado del RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material de RGB y viñetas que no incrustan un perfil de color. También para valores de color de RGB especificados con varios comandos de renderización de imágenes, como bgc= y color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 2%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

perfil de color de entrada predeterminado del RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material de RGB y viñetas que no incrustan un perfil de color. También para los valores de color del RGB especificados con varios comandos de renderización de imágenes, como `bgc=` y `color=`.

## Propiedades {#section-c22966bba03e43c08e9d3fb91bfdd465}

Cadena de texto. Si se especifica, debe ser un `icc::Name` del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o de una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil de RGB.

## Predeterminado {#section-0171cd6680284bfa9844b9cc3644ca61}

Heredado de `default::IccProfileSrcRgb` si no está definida o si está vacío. If `attribute::IccProfileSrcRgb` no se resuelve en un perfil válido, `attribute::IccProfileRgb` se utiliza en su lugar.

## Véase también {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [atributo::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
