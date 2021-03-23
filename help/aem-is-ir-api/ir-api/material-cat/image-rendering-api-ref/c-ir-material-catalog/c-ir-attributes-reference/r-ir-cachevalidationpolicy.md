---
description: Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.
seo-description: Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
uuid: 299dd5fe-9a0c-43df-a4c8-6b9e9c24003b
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.

Con la validación basada en la caducidad, los materiales de origen y las viñetas se comprueban periódicamente para comprobar si han cambiado. Con la validación basada en el catálogo, las imágenes de origen se comprueban solo después de cambiar el valor `catalog::TimeStamp`.

Se recomienda la validación basada en el catálogo cuando se utilizan catálogos de material y viñetas. La validación basada en la caducidad debe utilizarse cuando se haga referencia a las viñetas en las solicitudes de renderización de imágenes directamente por ruta.

## Propiedades {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 para seleccionar la validación basada en la caducidad. 1 para seleccionar la validación de caché basada en catálogo.

## Predeterminado {#section-e09f3af8b6b3497d963199988dc5345d}

Se hereda de `default::CacheValidationPolicy` si no está definido o si está vacío.

## Véase también {#section-b374e4d908e24af8995b2b376ca1be8b}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
