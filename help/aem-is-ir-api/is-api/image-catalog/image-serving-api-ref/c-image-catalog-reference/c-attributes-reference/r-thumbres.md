---
description: Resolución de miniatura predeterminada. Proporciona un valor predeterminado para la resolución del objeto de miniatura en caso de que un registro de catálogo concreto no contenga un valor de catálogo ThumbRes válido.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# ThumbRes{#thumbres}

Resolución de miniatura predeterminada. Proporciona un valor predeterminado para la resolución del objeto de miniatura en caso de que un registro de catálogo concreto no contenga un valor de catálogo válido::ThumbRes.

Solo se usa para solicitudes de miniatura ( `req=tmb`) y cuando `catalog::ThumbType=3`.

## Propiedades {#section-88d37d0e030f4879a9e584dd2cc780f3}

Número real, mayor que 0.Normalmente expresado como píxeles por pulgada, pero también puede estar en otras unidades, como píxeles por metro.

## Predeterminado {#section-86588899ec9b4276a98b03d7faf64003}

Se hereda de `default::ThumbRes` si no está definido o si está vacío.

## Véase también {#section-a6d2cce2e404441a996dba98a95c8e16}

[catálogo::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
