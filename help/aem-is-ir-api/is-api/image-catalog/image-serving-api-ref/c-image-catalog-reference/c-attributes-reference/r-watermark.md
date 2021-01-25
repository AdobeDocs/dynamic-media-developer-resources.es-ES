---
description: Selector de marca de agua. Especifica el ID de catálogo del registro de catálogo que se va a utilizar como imagen o plantilla de marca de agua.
seo-description: Selector de marca de agua. Especifica el ID de catálogo del registro de catálogo que se va a utilizar como imagen o plantilla de marca de agua.
seo-title: Filigrana
solution: Experience Manager
title: Filigrana
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# Filigrana{#watermark}

Selector de marca de agua. Especifica el catálogo::Id del registro de catálogo que se va a utilizar como imagen o plantilla de marca de agua.

Si se especifica, el servidor aplica la marca de agua a los datos de imagen solicitados para todas las solicitudes de imagen ( `req=img`).

## Propiedades {#section-fad6ffff4c5f4b5c8010281bc1377055}

Cadena de texto. Si se especifica, debe ser un valor `Catalog::Id` válido en este catálogo de imágenes (o en el catálogo predeterminado, si se especifica en [!DNL default.ini]).

## Predeterminado {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Se hereda de `default::Watermark` si no se define. Si está definida pero está vacía, no se aplica ninguna marca de agua para este catálogo de imágenes, aunque se haya definido `default::Watermark`.

## Véase también {#section-f15dbe31013849828d78588742dde58e}

[catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
