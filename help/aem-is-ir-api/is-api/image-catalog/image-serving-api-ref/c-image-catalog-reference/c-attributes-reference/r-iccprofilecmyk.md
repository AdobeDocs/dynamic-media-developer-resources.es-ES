---
description: Perfil de color de salida predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta CMYK cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color CMYK especificados con varios comandos del servicio de imágenes, como color=.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

Perfil de color de salida predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta CMYK cuando no se especifique ningún espacio de color de salida con icc= y para determinados valores de color CMYK especificados con varios comandos del servicio de imágenes, como color=.

## Propiedades {#section-d8b6102cc1c744d482f99808ccfcaa24}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes, del catálogo predeterminado o una ruta de acceso de archivo relativa a `attribute::RootPath`. El perfil ICC referenciado debe ser un perfil CMYK.

## Predeterminado {#section-62442df09a724950bfbdd0640b3e6678}

Se hereda de `default::IccProfileCmyk` si no se ha definido o está vacío.

## Véase también {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728), [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
