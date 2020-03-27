---
description: Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.
seo-description: Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Scene7 Image Serving - Image Rendering API
uuid: 299dd5fe-9a0c-43df-a4c8-6b9e9c24003b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CacheValidationPolicy{#cachevalidationpolicy}

Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.

Con la validación basada en la caducidad, los materiales de origen y las viñetas se comprueban periódicamente para comprobar si han cambiado. Con la validación basada en catálogo, las imágenes de origen solo se comprueban después de cambiar el `catalog::TimeStamp` valor.

Se recomienda la validación basada en catálogo cuando se utilizan catálogos de material y de viñetas. La validación basada en la caducidad se debe utilizar cuando se haga referencia a las viñetas en solicitudes de procesamiento de imágenes directamente por ruta.

## Propiedades {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 para seleccionar la validación basada en la caducidad. 1 para seleccionar la validación de caché basada en catálogo.

## Predeterminado {#section-e09f3af8b6b3497d963199988dc5345d}

Se hereda de `default::CacheValidationPolicy` si no está definida o si está vacía.

## Véase también {#section-b374e4d908e24af8995b2b376ca1be8b}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
