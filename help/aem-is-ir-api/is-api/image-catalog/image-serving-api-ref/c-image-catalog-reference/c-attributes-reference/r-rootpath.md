---
description: Ruta raíz de datos de origen. Ruta absoluta o relativa de la carpeta raíz para los datos de origen de este catálogo de imágenes.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# RootPath{#rootpath}

Ruta raíz de datos de origen. Ruta absoluta o relativa de la carpeta raíz para los datos de origen de este catálogo de imágenes.

El `RootPath` es un valor de cadena de texto. Consulte [Administración de datos de origen](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) para obtener información adicional sobre las rutas raíz del servidor.

## Propiedades {#section-b41d7e0ea63143eb8034569706cad0c0}

Cadena de texto. Debe estar vacío, tener una ruta de carpeta relativa válida o una ruta de acceso absoluta válida a la que pueda acceder el servidor de imágenes.

## Predeterminado {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Se hereda de `default::RootPath` si no se define. Si se define pero está vacío, no contribuirá a la ruta raíz del archivo de origen.

## Véase también {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catálogo::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catálogo::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),   [conjunto de reglas::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [Administración de datos de origen](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
