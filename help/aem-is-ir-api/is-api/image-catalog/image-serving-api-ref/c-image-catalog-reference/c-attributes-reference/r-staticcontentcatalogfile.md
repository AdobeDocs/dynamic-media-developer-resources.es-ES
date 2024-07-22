---
description: Rutas del archivo de datos del catálogo de contenido estático. Especifica los archivos que contienen los datos de contenido estático para este catálogo.
solution: Experience Manager
title: ArchivoCatálogoContenidoEstático
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# ArchivoCatálogoContenidoEstático{#staticcontentcatalogfile}

Rutas del archivo de datos del catálogo de contenido estático. Especifica los archivos que contienen los datos de contenido estático para este catálogo.

Los archivos de datos del catálogo de contenido estático se cargan en el orden especificado. Si el mismo valor `static::Id` aparece en más de un registro (en el mismo archivo de catálogo o en varios), prevalecerá la última instancia.

## Propiedades {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Uno o más valores de cadena de texto, separados por comas. Opcional. Cada valor debe ser una ruta absoluta o una ruta relativa a la carpeta del catálogo.

## Predeterminado {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vacío, lo que indica que este catálogo de imágenes no incluye datos de contenido estático.

## Véase también {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Datos de catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
