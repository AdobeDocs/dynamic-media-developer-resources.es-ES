---
description: Resolución de miniatura predeterminada. Proporciona un valor predeterminado para la resolución del objeto de miniatura en caso de que un registro de catálogo concreto no contenga un valor de catálogo ThumbRes válido.
seo-description: Resolución de miniatura predeterminada. Proporciona un valor predeterminado para la resolución del objeto de miniatura en caso de que un registro de catálogo concreto no contenga un valor de catálogo ThumbRes válido.
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
uuid: 4a77d673-9d2e-4e62-a014-c99fa3df294a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

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
