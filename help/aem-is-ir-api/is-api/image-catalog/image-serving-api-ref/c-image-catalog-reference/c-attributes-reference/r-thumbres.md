---
description: Resolución de miniatura predeterminada. Proporciona una resolución de miniatura predeterminada en el caso de que el valor de catálogo ThumbRes no sea válido en un registro de catálogo determinado.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
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
