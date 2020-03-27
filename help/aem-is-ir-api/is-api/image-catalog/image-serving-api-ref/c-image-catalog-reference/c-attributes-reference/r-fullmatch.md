---
description: Opción de coincidencia de catálogo.
seo-description: Opción de coincidencia de catálogo.
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# FullMatch{#fullmatch}

Opción de coincidencia de catálogo.

Una entrada de catálogo se especifica como un par ` *``*/ *`rootIdimageId`*` en las solicitudes HTTP. Al analizar, se selecciona un catálogo si ` *`rootId`*` coincide con el `attribute::RootId` valor del catálogo y el registro del catálogo se identifica mediante la coincidencia de ` *`imageId`*` con un `catalog::Id` valor. Si se encuentra un catálogo, pero no hay ninguna entrada de catálogo que coincida con ` *`imageId`*`, el servidor puede realizar una de estas acciones:

Si no `attribute::FullMatch` está configurado, el servidor utiliza los atributos del catálogo coincidente. En este caso, ` *`rootId`*` se reemplaza por `attribute::RootPath` (o `default::RootPath`, si no se especifica en este catálogo).

Si `attribute::FullMatch` está configurado, el servidor ignora completamente el catálogo, como si no hubiera coincidido ningún catálogo, y continúa usando los atributos predeterminados del catálogo. En este caso, ` *`rootId`*` sigue siendo parte de la ruta (que está precedida por `default::RootPath`).

## Propiedades {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Indicador. Establezca en 0 para el comportamiento predeterminado o en 1 para habilitar el comportamiento de coincidencia completa.

## Predeterminado {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Se hereda de `default::FullMatch` si no está definida o si está vacía.

## Véase también {#section-42da0ba53e0b4c089c62108785faf5a9}

[atributo::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
