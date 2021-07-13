---
description: Rutas de archivo de datos de imagen. Especifica los archivos que contienen los datos de imagen para este catálogo.
solution: Experience Manager
title: ArchivoCatálogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 4%

---

# ArchivoCatálogo{#catalogfile}

Rutas de archivo de datos de imagen. Especifica los archivos que contienen los datos de imagen para este catálogo.

Los archivos de datos de imagen se cargan en el orden especificado. Si el mismo valor `catalog::Id` se produce en más de un registro (ya sea en los mismos archivos de catálogo o en diferentes archivos), prevalecerá la última instancia.

## Propiedades {#section-6da55f145ecd4e31a5de52637a436983}

Uno o más valores de cadena de texto, separados por comas. Opcional. Cada valor debe ser una ruta absoluta del archivo o una ruta relativa a la carpeta del catálogo.

## Predeterminado {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vacío, lo que indica que este catálogo de imágenes no incluye datos de imágenes.

## Véase también {#section-910b67c5041d44d99a105ad43ff63a37}

[Campos de datos del catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
