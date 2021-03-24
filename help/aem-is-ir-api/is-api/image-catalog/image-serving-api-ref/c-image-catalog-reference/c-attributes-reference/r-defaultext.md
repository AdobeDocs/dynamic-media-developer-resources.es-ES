---
description: Sufijo de archivo de imagen predeterminado. Se adjunta al valor del campo Ruta del catálogo (o catálogo MaskPath) si la ruta no incluye un sufijo de archivo
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# DefaultExt{#defaultext}

Sufijo de archivo de imagen predeterminado. Se anexa al valor del campo catálogo::Path (o catálogo::MaskPath) si la ruta no incluye un sufijo de archivo

Un sufijo de archivo consta de un punto y uno o más caracteres entre el punto y el final de la cadena. El sufijo se anexa a la ruta http si la ruta no se resuelve en una entrada de catálogo y si el último elemento de ruta no incluye un sufijo de archivo.

## Propiedades {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Cadena de texto. Debe incluir un &quot;.&quot; y uno o más caracteres.

## Predeterminado {#section-1194c36ffe0748c5b9ff7d732a506588}

Se hereda de `default::DefaultExt` si no se define. Si se define pero está vacío, no se aplica ningún sufijo predeterminado a los nombres de imagen al utilizar este catálogo.

## Véase también {#section-d7c408b979844643adff8258f500eb7c}

[catálogo::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catálogo::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
