---
description: Rutas de archivo de datos SVG. Especifica los archivos que contienen los datos SVG de este catálogo.
seo-description: Rutas de archivo de datos SVG. Especifica los archivos que contienen los datos SVG de este catálogo.
seo-title: SvgCatalogFile
solution: Experience Manager
title: SvgCatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: f0c8e687-77cc-4ca7-b2c2-6ba8960e11e6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---


# SvgCatalogFile{#svgcatalogfile}

Rutas de archivo de datos SVG. Especifica los archivos que contienen los datos SVG de este catálogo.

Los archivos de datos SVG se cargan después de todos los archivos de datos de imagen, en el orden exacto especificado. Si el mismo valor `catalog::Id` se produce en más de un registro (ya sea en la misma imagen o en archivos de catálogo SVG diferentes), prevalecerá la última instancia.

## Propiedades {#section-fc2d549f76474792837b2b92ec2087ea}

Uno o más valores de cadena de texto, separados por comas. Opcional. Cada valor debe ser una ruta absoluta del archivo o una ruta relativa a la carpeta del catálogo.

## Predeterminado {#section-a4e58951f3c249599665b823566433c9}

Vacío, que indica que este catálogo de imágenes no incluye datos SVG.

## Véase también {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Datos](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29) de catálogo,  [archivo de catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
