---
description: Rutas del archivo de datos de SVG. Especifica los archivos que contienen los datos de SVG para este catálogo.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# SvgCatalogFile{#svgcatalogfile}

Rutas del archivo de datos de SVG. Especifica los archivos que contienen los datos de SVG para este catálogo.

Los archivos de datos de SVG se cargan después de todos los archivos de datos de imagen, en el orden exacto especificado. Si el mismo valor `catalog::Id` aparece en más de un registro (en la misma imagen o en distintos archivos de catálogo de SVG), prevalecerá la última instancia.

## Propiedades {#section-fc2d549f76474792837b2b92ec2087ea}

Uno o más valores de cadena de texto, separados por comas. Opcional. Cada valor debe ser una ruta absoluta o una ruta relativa a la carpeta del catálogo.

## Predeterminado {#section-a4e58951f3c249599665b823566433c9}

Empty, lo que indica que este catálogo de imágenes no incluye datos de SVG.

## Véase también {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Datos de catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [Archivo de catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
