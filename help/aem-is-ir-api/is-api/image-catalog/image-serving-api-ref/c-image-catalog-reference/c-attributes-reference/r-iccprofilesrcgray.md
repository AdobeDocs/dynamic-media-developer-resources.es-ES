---
description: Perfil de color de entrada predeterminado en escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen en escala de grises que no incrustan un perfil de color y para determinados valores de color en escala de grises especificados con varios comandos del servicio de imágenes, como color=.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54290f71-36b2-4b37-ac04-4fe85c1f34ab
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcGray{#iccprofilesrcgray}

Perfil de color de entrada predeterminado en escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen en escala de grises que no incrustan un perfil de color y para determinados valores de color en escala de grises especificados con varios comandos del servicio de imágenes, como color=.

## Propiedades {#section-8cbb316df6eb463aaca7b308d3568086}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes, del catálogo predeterminado o una ruta de acceso de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil en escala de grises.

## Predeterminado {#section-bcc7250715884412bd0780f60d1cce7b}

Se hereda de `default::IccProfileSrcGray` si no se ha definido o está vacío. Si `attribute::IccProfileSrcGray` no se resuelve en un perfil válido, se utiliza `attribute::IccProfileGray` en su lugar.

## Véase también {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35), [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
