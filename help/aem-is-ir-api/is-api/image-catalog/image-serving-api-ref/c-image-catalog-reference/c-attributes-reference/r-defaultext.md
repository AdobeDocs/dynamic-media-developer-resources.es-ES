---
description: Sufijo de archivo de imagen predeterminado. Se añade al valor del campo Ruta del catálogo (o Ruta de máscara de catálogo) si la ruta no incluye un sufijo de archivo
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# DefaultExt{#defaultext}

Sufijo de archivo de imagen predeterminado. Se añade al valor del campo catalog::Path (o catalog::MaskPath) si la ruta no incluye un sufijo de archivo

Un sufijo de archivo consta de un punto y uno o más caracteres entre el punto y el final de la cadena. El sufijo se anexa a la ruta http, si la ruta no se resuelve en una entrada de catálogo y si el último elemento de ruta no incluye un sufijo de archivo.

## Propiedades {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Cadena de texto. Debe incluir un &#39;.&#39; inicial y uno o más caracteres.

## Predeterminado {#section-1194c36ffe0748c5b9ff7d732a506588}

Se hereda de `default::DefaultExt` si no se define. Si se define pero está vacío, no se aplica ningún sufijo predeterminado a los nombres de imagen al utilizar este catálogo.

## Véase también {#section-d7c408b979844643adff8258f500eb7c}

[catálogo::Ruta](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catálogo::RutaMáscara](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
