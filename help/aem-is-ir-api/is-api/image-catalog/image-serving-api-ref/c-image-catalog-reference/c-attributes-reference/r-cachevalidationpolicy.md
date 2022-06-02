---
title: CacheValidationPolicy
description: Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.

Con la validación basada en la caducidad, las imágenes de origen se comprueban periódicamente si han cambiado. Con la validación basada en el catálogo, las imágenes de origen se comprueban solo después de la función `catalog::TimeStamp` ha cambiado.

Se recomienda la validación basada en el catálogo cuando se utilizan catálogos de imágenes. La validación basada en la caducidad debe utilizarse cuando se haga referencia a las imágenes directamente, sin necesidad de utilizar un catálogo de imágenes.

## Propiedades {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 para seleccionar la validación basada en la caducidad, 1 para seleccionar la validación de caché basada en el catálogo.

## Predeterminado {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Heredado de `default::CacheValidationPolicy` si no está definida o si está vacío.

## Véase también {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catálogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
