---
description: Perfil de color de entrada predeterminado RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material RGB y viñetas que no incrustan un perfil de color y para los valores de color RGB especificados con varios comandos de renderización de imágenes, como bgc= y color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

Perfil de color de entrada predeterminado RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material RGB y viñetas que no incrustan un perfil de color y para los valores de color RGB especificados con varios comandos de renderización de imágenes, como bgc= y color=.

## Propiedades {#section-c22966bba03e43c08e9d3fb91bfdd465}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil RGB.

## Predeterminado {#section-0171cd6680284bfa9844b9cc3644ca61}

Se hereda de `default::IccProfileSrcRgb` si no está definido o si está vacío. Si `attribute::IccProfileSrcRgb` no se resuelve en un perfil válido, se utiliza `attribute::IccProfileRgb` en su lugar.

## Véase también {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [atributo::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
