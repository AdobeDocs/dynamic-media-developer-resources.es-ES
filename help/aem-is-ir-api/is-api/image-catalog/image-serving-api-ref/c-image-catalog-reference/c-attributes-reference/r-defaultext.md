---
description: Sufijo de archivo de imagen predeterminado. Se añade al valor del campo Ruta del catálogo (o Ruta de máscara de catálogo) si la ruta no incluye un sufijo de archivo
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
TQID: 'https://experienceleague.adobe.com/3juJVbcGdP1Z-F5inwe-Do7vkk80T-SNJmAiotjU6iw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 2%

---

# DefaultExt{#defaultext}

Sufijo de archivo de imagen predeterminado. Se añade al valor del campo catalog::Path (o catalog::MaskPath) si la ruta no incluye un sufijo de archivo

Un sufijo de archivo consta de un punto y uno o más caracteres entre el punto y el final de la cadena. El sufijo se anexa a la ruta http, si la ruta no se resuelve en una entrada de catálogo y si el último elemento de ruta no incluye un sufijo de archivo.

## Propiedades {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Cadena de texto. Debe incluir &quot;.&quot; inicial y uno o más caracteres.

## Predeterminado {#section-1194c36ffe0748c5b9ff7d732a506588}

Se hereda de `default::DefaultExt` si no se define. Si se define pero está vacío, no se aplica ningún sufijo predeterminado a los nombres de imagen al utilizar este catálogo.

## Véase también {#section-d7c408b979844643adff8258f500eb7c}

[catálogo::Ruta](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catálogo::RutaMáscara](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
