---
description: Perfil de color de entrada predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen en escala de grises que no incrustan un perfil de color y para ciertos valores de color en escala de grises especificados con varios comandos de servicio de imágenes, como color=.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Perfil de color de entrada predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen en escala de grises que no incrustan un perfil de color y para ciertos valores de color en escala de grises especificados con varios comandos de servicio de imágenes, como color=.

## Propiedades {#section-8cbb316df6eb463aaca7b308d3568086}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser de escala de grises.

## Predeterminado {#section-bcc7250715884412bd0780f60d1cce7b}

Se hereda de `default::IccProfileSrcGray` si no está definido o si está vacío. Si `attribute::IccProfileSrcGray` no se resuelve en un perfil válido, se utiliza `attribute::IccProfileGray` en su lugar.

## Véase también {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [atributo::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35),  [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
