---
description: Ruta raíz de datos de origen. Valor de cadena de texto. Ruta absoluta o segmento de ruta relativa para la carpeta raíz de todos los archivos de datos de viñeta, textura, imagen y ICC a los que hace referencia este catálogo de imágenes.
seo-description: Ruta raíz de datos de origen. Valor de cadena de texto. Ruta absoluta o segmento de ruta relativa para la carpeta raíz de todos los archivos de datos de viñeta, textura, imagen y ICC a los que hace referencia este catálogo de imágenes.
seo-title: RootPath *
solution: Experience Manager
title: RootPath *
topic: Scene7 Image Serving - Image Rendering API
uuid: a23ea524-8ca4-47c4-83a5-64a174d8767e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# RootPath *{#rootpath}

Ruta raíz de datos de origen. Valor de cadena de texto. Ruta absoluta o segmento de ruta relativa para la carpeta raíz de todos los archivos de datos de viñeta, textura, imagen y ICC a los que hace referencia este catálogo de imágenes.

## Propiedades {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Cadena de texto. Debe estar vacío, tener un segmento de ruta válido relativo a la configuración del servidor de procesamiento de imágenes `ir.resourceRootPaths` o una ruta de acceso de archivo absoluta válida. No debe incluir delimitadores de elementos de ruta de acceso al inicio y al final.

## Predeterminado {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Se hereda de `default::RootPath` si no se define. Si se define pero está vacío, no contribuirá a la ruta raíz del archivo de origen.

## Véase también {#section-92012cc1ce32448ea977e7e0484857e2}

[catálogo::Ruta](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ,  [catálogo::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969),  `ir.resourceRootPaths`
