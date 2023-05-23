---
description: Selector de filigrana. Especifica el ID de catálogo del registro de catálogo que se utilizará como imagen o plantilla de filigrana.
solution: Experience Manager
title: Filigrana
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# Filigrana{#watermark}

Selector de filigrana. Especifica el catalog::Id del registro de catálogo que se utilizará como imagen o plantilla de filigrana.

Si se especifica, el servidor aplica la marca de agua a los datos de imagen solicitados para todas las solicitudes de imagen ( `req=img`).

## Propiedades {#section-fad6ffff4c5f4b5c8010281bc1377055}

Cadena de texto. Si se especifica, debe ser un válido `Catalog::Id` valor en este catálogo de imágenes (o en el catálogo predeterminado, si se especifica en [!DNL default.ini]).

## Predeterminado {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Heredado de `default::Watermark` si no está definido. Si se define pero está vacío, no se aplica ninguna marca de agua a este catálogo de imágenes, aunque `default::Watermark` está definida.

## Véase también {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
