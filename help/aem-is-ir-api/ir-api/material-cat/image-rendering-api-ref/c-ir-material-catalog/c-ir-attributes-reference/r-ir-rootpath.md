---
description: Ruta raíz de datos de origen. Valor de cadena de texto. Ruta absoluta o segmento de ruta relativa para la carpeta raíz de todos los archivos de datos de viñetas, texturas, imágenes y ICC a los que hace referencia este catálogo de imágenes.
solution: Experience Manager
title: RootPath *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# RootPath *{#rootpath}

Ruta raíz de datos de origen. Valor de cadena de texto. Ruta absoluta o segmento de ruta relativa para la carpeta raíz de todos los archivos de datos de viñetas, texturas, imágenes y ICC a los que hace referencia este catálogo de imágenes.

## Propiedades {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Cadena de texto. Debe estar vacío, tener un segmento de ruta válido relativo a la configuración del servidor de renderización de imágenes `ir.resourceRootPaths` o una ruta de archivo absoluta válida. No debe incluir delimitadores de elementos de ruta inicial y final.

## Predeterminado {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Se hereda de `default::RootPath` si no se define. Si se define pero está vacío, no contribuirá a la ruta raíz del archivo de origen.

## Véase también {#section-92012cc1ce32448ea977e7e0484857e2}

[catálogo::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ,  [catálogo::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969),  `ir.resourceRootPaths`
