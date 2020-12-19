---
description: PERFIL de color de entrada RGB predeterminado. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material RGB y las viñetas que no incrustan un perfil de color y para los valores de color RGB especificados con varios comandos de procesamiento de imágenes, como bgc= y color=.
seo-description: PERFIL de color de entrada RGB predeterminado. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material RGB y las viñetas que no incrustan un perfil de color y para los valores de color RGB especificados con varios comandos de procesamiento de imágenes, como bgc= y color=.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 9657e296-0d2a-4b05-9be7-5a54d3277f90
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

PERFIL de color de entrada RGB predeterminado. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material RGB y las viñetas que no incrustan un perfil de color y para los valores de color RGB especificados con varios comandos de procesamiento de imágenes, como bgc= y color=.

## Propiedades {#section-c22966bba03e43c08e9d3fb91bfdd465}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil RGB.

## Predeterminado {#section-0171cd6680284bfa9844b9cc3644ca61}

Se hereda de `default::IccProfileSrcRgb` si no está definida o si está vacía. Si `attribute::IccProfileSrcRgb` no se resuelve en un perfil válido, se utiliza `attribute::IccProfileRgb` en su lugar.

## Véase también {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [atributo::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
