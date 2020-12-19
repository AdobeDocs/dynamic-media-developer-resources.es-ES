---
description: Espacio de color predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta en escala de grises cuando no se especifique ningún espacio de color de salida con icc=.
seo-description: Espacio de color predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta en escala de grises cuando no se especifique ningún espacio de color de salida con icc=.
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Scene7 Image Serving - Image Rendering API
uuid: 064be242-d964-4fb8-99ea-78bb5599e70f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# IccProfileGray{#iccprofilegray}

Espacio de color predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta en escala de grises cuando no se especifique ningún espacio de color de salida con icc=.

## Propiedades {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de material o del catálogo predeterminado, o bien una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC referenciado debe ser un perfil en escala de grises.

## Predeterminado {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Se hereda de `default::IccProfileGray` si no está definida o si está vacía.

## Véase también {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [atributo::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
