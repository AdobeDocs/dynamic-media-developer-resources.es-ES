---
title: IccProfileGray
description: Perfil de color de salida predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta en escala de grises cuando no se especifique ningún espacio de color de salida con icc= y para ciertos valores de color en escala de grises especificados con varios comandos de Image Serving, como color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

Perfil de color de salida predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta en escala de grises cuando no se especifique ningún espacio de color de salida con icc= y para ciertos valores de color en escala de grises especificados con varios comandos de Image Serving, como color=.

## Propiedades {#section-03f090ee2acf4537b83f78840d23ecab}

Cadena de texto. Si se especifica, debe ser un `icc::Name` del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o de una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser de escala de grises.

## Predeterminado {#section-95ba3ab15edc4259b657c6ebf8783d61}

Heredado de `default::IccProfileGray` si no está definida o si está vacío.

## Véase también {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
