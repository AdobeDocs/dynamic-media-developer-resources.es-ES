---
description: Selector de marca de agua. Especifica el ID de catálogo del registro de catálogo que se va a utilizar como imagen o plantilla de marca de agua.
solution: Experience Manager
title: Filigrana
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---

# Filigrana{#watermark}

Selector de marca de agua. Especifica el catálogo::Id del registro de catálogo que se utilizará como imagen o plantilla de marca de agua.

Si se especifica, el servidor aplica la marca de agua a los datos de imagen solicitados para todas las solicitudes de imagen ( `req=img`).

## Propiedades {#section-fad6ffff4c5f4b5c8010281bc1377055}

Cadena de texto. Si se especifica, debe ser un valor `Catalog::Id` válido en este catálogo de imágenes (o en el catálogo predeterminado, si se especifica en [!DNL default.ini]).

## Predeterminado {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Se hereda de `default::Watermark` si no se define. Si está definida pero está vacía, no se aplica ninguna marca de agua para este catálogo de imágenes, aunque `default::Watermark` esté definido.

## Véase también {#section-f15dbe31013849828d78588742dde58e}

[catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
