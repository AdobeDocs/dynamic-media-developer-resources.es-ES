---
description: Resolución de miniatura predeterminada. Proporciona una resolución de miniatura predeterminada en el caso de que el valor de catálogo ThumbRes no sea válido en un registro de catálogo determinado.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
TQID: 'https://experienceleague.adobe.com/xMGMMjCIDWQJbJtLzatEiSEgdD5hQOkaOhKJbMYUyB0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 3%

---

# ThumbRes{#thumbres}

Resolución de miniatura predeterminada. Proporciona una resolución de miniatura predeterminada en el caso de que el valor de catálogo::ThumbRes no sea válido en un registro de catálogo determinado.

Solo se usa para solicitudes de miniaturas (`req=tmb`) y cuando `catalog::ThumbType=3`.

## Propiedades {#section-88d37d0e030f4879a9e584dd2cc780f3}

Número real, mayor de 0,Se expresa normalmente como píxeles por pulgada, pero también puede estar en otras unidades, como píxeles por metro.

## Predeterminado {#section-86588899ec9b4276a98b03d7faf64003}

Se hereda de `default::ThumbRes` si no se ha definido o está vacío.

## Véase también {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalog::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
