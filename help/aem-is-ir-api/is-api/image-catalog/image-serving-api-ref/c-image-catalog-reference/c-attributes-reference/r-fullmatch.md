---
description: Opción de coincidencia de catálogo.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# FullMatch{#fullmatch}

Opción de coincidencia de catálogo.

Se especifica una entrada de catálogo como `*`rootId`*/ *`imageId`*` emparejar en solicitudes HTTP. Al analizar, se selecciona un catálogo si `*`rootId`*` coincide con el `attribute::RootId` valor del catálogo, y el registro de catálogo se identifica mediante la coincidencia `*`imageId`*` con un `catalog::Id` valor. Si se encuentra un catálogo, pero no hay coincidencia de entrada de catálogo `*`imageId`*`, el servidor puede hacer una de estas dos cosas:

If `attribute::FullMatch` no se ha definido, el servidor utiliza los atributos del catálogo coincidente. En este caso, `*`rootId`*` se ha reemplazado por `attribute::RootPath` (o `default::RootPath`, si no se especifica en este catálogo).

If `attribute::FullMatch` Cuando se establece, el servidor ignora por completo el catálogo, como si no se hubiera encontrado ningún catálogo coincidente, y continúa utilizando los atributos de catálogo predeterminados. En este caso, `*`rootId`*` permanece como parte de la ruta (que va precedida de `default::RootPath`).

## Propiedades {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Indicador. Establezca el valor en 0 para el comportamiento predeterminado o en 1 para habilitar el comportamiento de coincidencia completa.

## Predeterminado {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Heredado de `default::FullMatch` si no se define o si está vacío.

## Véase también {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
