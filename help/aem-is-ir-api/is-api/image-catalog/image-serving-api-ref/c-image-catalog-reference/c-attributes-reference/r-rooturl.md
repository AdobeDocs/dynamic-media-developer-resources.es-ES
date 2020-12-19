---
description: Dirección URL raíz para direcciones URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imágenes relativas.
seo-description: Dirección URL raíz para direcciones URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imágenes relativas.
seo-title: RootUrl
solution: Experience Manager
title: RootUrl
topic: Scene7 Image Serving - Image Rendering API
uuid: 173ce99a-f87e-4700-a28a-1a87b8c55b85
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# RootUrl{#rooturl}

Dirección URL raíz para direcciones URL de imágenes relativas. Especifica la dirección URL raíz para las direcciones URL de imágenes relativas.

`attribute::RootUrl` se utiliza en lugar de  `attribute::RootPath` cuando un  `src=` valor o  `mask=` se encierra entre {llaves} o (paréntesis).

## Propiedades {#section-fe02269b4b724319a5d1f2cfcae31cba}

Valor de cadena de texto. Ruta de acceso raíz absoluta de la dirección URL, incluido el identificador de protocolo inicial. Se admiten los siguientes protocolos: HTTP, HTTPS y FTP.

## Predeterminado {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Se hereda de `default::RootUrl` si no se define. Si están definidas pero vacías, las direcciones URL relativas no son compatibles con este catálogo de imágenes.

## Véase también {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [atributo:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [conjunto de reglas::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
