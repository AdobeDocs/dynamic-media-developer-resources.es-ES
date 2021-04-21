---
description: Perfil de color de salida predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta CMYK cuando no se especifique ningún espacio de color de salida con icc= y para ciertos valores de color CMYK especificados con varios comandos de Image Serving, como color=.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# IccProfileCmyk{#iccprofilecmyk}

Perfil de color de salida predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta CMYK cuando no se especifique ningún espacio de color de salida con icc= y para ciertos valores de color CMYK especificados con varios comandos de Image Serving, como color=.

## Propiedades {#section-d8b6102cc1c744d482f99808ccfcaa24}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil CMYK.

## Predeterminado {#section-62442df09a724950bfbdd0640b3e6678}

Se hereda de `default::IccProfileCmyk` si no está definido o si está vacío.

## Véase también {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [atributo::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728),  [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
