---
description: Rutas de archivo de datos del catálogo de contenido estático. Especifica los archivos que contienen los datos de contenido estático para este catálogo.
seo-description: Rutas de archivo de datos del catálogo de contenido estático. Especifica los archivos que contienen los datos de contenido estático para este catálogo.
seo-title: StaticContentCatalogFile
solution: Experience Manager
title: StaticContentCatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 82d2a68a-255a-4e65-a29f-7022e7f0f5ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

Rutas de archivo de datos del catálogo de contenido estático. Especifica los archivos que contienen los datos de contenido estático para este catálogo.

Los archivos de datos del catálogo de contenido estático se cargan en el orden especificado. Si el mismo `static::Id` valor se produce en más de un registro (en el mismo archivo de catálogo o en diferentes archivos), prevalecerá la última instancia.

## Propiedades {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Uno o más valores de cadena de texto, separados por comas. Opcional. Cada valor debe ser una ruta absoluta del archivo o una ruta relativa a la carpeta del catálogo.

## Predeterminado {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vacío, que indica que este catálogo de imágenes no incluye datos de contenido estático.

## Véase también {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Datos del catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
