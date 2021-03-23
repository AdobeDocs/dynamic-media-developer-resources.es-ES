---
description: Opción de coincidencia de catálogo.
seo-description: Opción de coincidencia de catálogo.
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%

---


# FullMatch{#fullmatch}

Opción de coincidencia de catálogo.

Una entrada de catálogo se especifica como un par `*`rootId`*/ *`imageId`*` en las solicitudes HTTP. Al analizar, se selecciona un catálogo si `*`rootId`*` coincide con el valor `attribute::RootId` del catálogo y el registro del catálogo se identifica coincidiendo con `*`imageId`*` con un valor `catalog::Id`. Si se encuentra un catálogo, pero no hay ninguna entrada de catálogo que coincida con `*`imageId`*`, el servidor puede hacer una de las dos cosas:

Si `attribute::FullMatch` no está establecido, el servidor utiliza los atributos del catálogo coincidente. En este caso, `*`rootId`*` se reemplaza por `attribute::RootPath` (o `default::RootPath`, si no se especifica en este catálogo).

Si `attribute::FullMatch` está establecido, el servidor ignora por completo el catálogo, como si no hubiera coincidido ningún catálogo, y continúa usando los atributos de catálogo predeterminados. En este caso, `*`rootId`*` sigue siendo parte de la ruta (que va precedida de `default::RootPath`).

## Propiedades {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Indicador. Establézcalo en 0 para el comportamiento predeterminado o en 1 para habilitar el comportamiento de coincidencia completa.

## Predeterminado {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Se hereda de `default::FullMatch` si no está definido o si está vacío.

## Véase también {#section-42da0ba53e0b4c089c62108785faf5a9}

[atributo::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ,  [catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
