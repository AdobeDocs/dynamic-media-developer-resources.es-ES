---
description: Sufijo de archivo de imagen predeterminado. Se adjunta al valor del campo Ruta del catálogo (o rutaDeMáscara del catálogo) si la ruta no incluye un sufijo de archivo
seo-description: Sufijo de archivo de imagen predeterminado. Se adjunta al valor del campo Ruta del catálogo (o rutaDeMáscara del catálogo) si la ruta no incluye un sufijo de archivo
seo-title: DefaultExt
solution: Experience Manager
title: DefaultExt
topic: Scene7 Image Serving - Image Rendering API
uuid: aa245d18-15cc-41cb-a49d-757d74fe6231
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# DefaultExt{#defaultext}

Sufijo de archivo de imagen predeterminado. Se adjunta al valor del campo catálogo::Path (o catálogo::MaskPath) si la ruta no incluye un sufijo de archivo

Un sufijo de archivo consiste en un punto y uno o más caracteres entre el punto y el final de la cadena. El sufijo se anexa a la ruta http, si la ruta no se resuelve en una entrada de catálogo y si el último elemento de ruta no incluye un sufijo de archivo.

## Propiedades {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Cadena de texto. Debe incluir un encabezado &#39;.&#39; y uno o más caracteres.

## Predeterminado {#section-1194c36ffe0748c5b9ff7d732a506588}

Se hereda de `default::DefaultExt` si no se define. Si se define pero está vacío, no se aplica ningún sufijo predeterminado a los nombres de imagen al utilizar este catálogo.

## Véase también {#section-d7c408b979844643adff8258f500eb7c}

[catálogo::Ruta](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catálogo::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
