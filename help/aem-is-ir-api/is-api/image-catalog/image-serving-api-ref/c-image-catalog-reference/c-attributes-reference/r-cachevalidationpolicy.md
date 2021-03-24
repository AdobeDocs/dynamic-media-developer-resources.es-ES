---
description: Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.

Con la validación basada en la caducidad, las imágenes de origen se comprueban periódicamente si han cambiado. Con la validación basada en el catálogo, las imágenes de origen se comprueban solo después de cambiar el valor `catalog::TimeStamp`.

Se recomienda la validación basada en el catálogo cuando se utilizan catálogos de imágenes. La validación basada en la caducidad debe utilizarse cuando se haga referencia a las imágenes directamente, sin necesidad de utilizar un catálogo de imágenes.

## Propiedades {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 para seleccionar la validación basada en la caducidad, 1 para seleccionar la validación de caché basada en el catálogo.

## Predeterminado {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Se hereda de `default::CacheValidationPolicy` si no está definido o si está vacío.

## Véase también {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catálogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
