---
description: Perfil de color de entrada predeterminado de RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen RGB que no incrustan un perfil de color y para determinados valores de color RGB especificados con varios comandos del servicio de imágenes, como color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
TQID: 'https://experienceleague.adobe.com/CPYMKHgIu7mllwz1C-EM190nZxHzJ3547TWIEevP1rc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

Perfil de color de entrada predeterminado de RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de origen RGB que no incrustan un perfil de color y para determinados valores de color RGB especificados con varios comandos del servicio de imágenes, como color=.

## Propiedades {#section-3cd753196959462e9e674dab0b033d08}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes, del catálogo predeterminado o una ruta de acceso de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil de RGB.

## Predeterminado {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Se hereda de `default::IccProfileSrcRgb` si no se ha definido o está vacío. Si `attribute::IccProfileSrcRgb` no se resuelve en un perfil válido, se utiliza `attribute::IccProfileRgb` en su lugar.

## Véase también {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
