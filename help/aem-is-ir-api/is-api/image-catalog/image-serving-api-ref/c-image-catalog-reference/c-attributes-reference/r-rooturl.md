---
description: URL raíz para direcciones URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imágenes relativas.
solution: Experience Manager
title: RootUrl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72560180-53e5-4293-9dd3-c0cd196551dc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# RootUrl{#rooturl}

URL raíz para direcciones URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imágenes relativas.

`attribute::RootUrl` se utiliza en lugar de  `attribute::RootPath` cuando {llaves} o (paréntesis) encierran un  `src=` valor o  `mask=` valor.

## Propiedades {#section-fe02269b4b724319a5d1f2cfcae31cba}

Valor de cadena de texto. Ruta raíz de URL absoluta, incluido el identificador de protocolo inicial. Se admiten los siguientes protocolos: HTTP, HTTPS y FTP.

## Predeterminado {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Se hereda de `default::RootUrl` si no se define. Si está definida pero está vacía, las direcciones URL relativas no son compatibles con este catálogo de imágenes.

## Véase también {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [rule set::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
