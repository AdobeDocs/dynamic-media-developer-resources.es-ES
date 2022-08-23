---
title: IccProfileSrcCmyk
description: Perfil de color de entrada predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material CMYK que no incrustan un perfil de color.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Perfil de color de entrada predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material CMYK que no incrustan un perfil de color.

## Propiedades {#section-0cee77438d914c319ec876edb3490821}

Cadena de texto. Si se especifica, debe ser un `icc::Name` del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o de una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil CMYK.

## Predeterminado {#section-11f6239e0dd14827abf4a95c1b30161c}

Heredado de `default::IccProfileSrcCmyk` si no está definida o si está vacío. If `attribute::IccProfileSrcCmyk` no se resuelve en un perfil válido, `attribute::IccProfileCmyk` se utiliza en su lugar.

## Véase también {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [atributo::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
