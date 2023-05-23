---
description: Rutas del archivo de datos de imagen. Especifica los archivos que contienen los datos de imagen para este catálogo.
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---

# CatalogFile{#catalogfile}

Rutas del archivo de datos de imagen. Especifica los archivos que contienen los datos de imagen para este catálogo.

Los archivos de datos de imagen se cargan en el orden especificado. Si es el mismo `catalog::Id` Si el valor aparece en más de un registro (en el mismo o en distintos archivos de catálogo), prevalecerá la última instancia.

## Propiedades {#section-6da55f145ecd4e31a5de52637a436983}

Uno o más valores de cadena de texto, separados por comas. Opcional. Cada valor debe ser una ruta absoluta o una ruta relativa a la carpeta del catálogo.

## Predeterminado {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vacío, lo que indica que este catálogo de imágenes no incluye datos de imagen.

## Véase también {#section-910b67c5041d44d99a105ad43ff63a37}

[Campos de datos de catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
