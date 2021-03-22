---
description: Rutas de archivo de datos SVG. Especifica los archivos que contienen los datos SVG para este catálogo.
seo-description: Rutas de archivo de datos SVG. Especifica los archivos que contienen los datos SVG para este catálogo.
seo-title: ArchivoCatálogoSvg
solution: Experience Manager
title: ArchivoCatálogoSvg
uuid: f0c8e687-77cc-4ca7-b2c2-6ba8960e11e6
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 3%

---


# ArchivoCatálogoSvg{#svgcatalogfile}

Rutas de archivo de datos SVG. Especifica los archivos que contienen los datos SVG para este catálogo.

Los archivos de datos SVG se cargan después de todos los archivos de datos de imagen, en el orden exacto especificado. Si el mismo valor `catalog::Id` se produce en más de un registro (ya sea en la misma imagen o en archivos de catálogo SVG diferentes), prevalecerá la última instancia.

## Propiedades {#section-fc2d549f76474792837b2b92ec2087ea}

Uno o más valores de cadena de texto, separados por comas. Opcional. Cada valor debe ser una ruta absoluta del archivo o una ruta relativa a la carpeta del catálogo.

## Predeterminado {#section-a4e58951f3c249599665b823566433c9}

Vacío, lo que indica que este catálogo de imágenes no incluye datos SVG.

## Véase también {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Datos](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29) del catálogo,  [Archivo del catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
