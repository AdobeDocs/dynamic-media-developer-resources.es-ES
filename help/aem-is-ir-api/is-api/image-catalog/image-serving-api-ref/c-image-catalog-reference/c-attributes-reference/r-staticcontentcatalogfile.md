---
description: Rutas de archivo de datos del catálogo de contenido estático. Especifica los archivos que contienen los datos de contenido estático de este catálogo.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

Rutas de archivo de datos del catálogo de contenido estático. Especifica los archivos que contienen los datos de contenido estático de este catálogo.

Los archivos de datos del catálogo de contenido estático se cargan en el orden especificado. Si el mismo valor `static::Id` se produce en más de un registro (ya sea en los mismos archivos de catálogo o en diferentes archivos), prevalecerá la última instancia.

## Propiedades {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Uno o más valores de cadena de texto, separados por comas. Opcional. Cada valor debe ser una ruta absoluta del archivo o una ruta relativa a la carpeta del catálogo.

## Predeterminado {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vacío, lo que indica que este catálogo de imágenes no incluye datos de contenido estático.

## Véase también {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Datos del catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
