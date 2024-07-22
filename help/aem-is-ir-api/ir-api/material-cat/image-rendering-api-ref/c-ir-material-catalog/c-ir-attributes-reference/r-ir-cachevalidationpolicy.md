---
title: CacheValidationPolicy
description: Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Directiva de validación de caché del servidor. Especifica cuándo se validan las entradas de caché del lado del servidor.

Con la validación basada en la caducidad, los materiales de origen y las viñetas se comprueban periódicamente para ver si han cambiado. Con la validación basada en el catálogo, las imágenes de origen solo se comprueban después de que cambie el valor `catalog::TimeStamp`.

Se recomienda la validación basada en catálogo cuando se utilizan catálogos de material y de viñetas. La validación basada en la caducidad debe utilizarse cuando se haga referencia a las viñetas en las solicitudes de Image Rendering directamente por ruta.

## Propiedades {#section-46e13cb341eb442c86e0d8292de23ea0}

Enumeración. 0 para seleccionar la validación basada en la caducidad. 1 para seleccionar la validación de caché basada en el catálogo.

## Predeterminado {#section-e09f3af8b6b3497d963199988dc5345d}

Se hereda de `default::CacheValidationPolicy` si no se ha definido o está vacío.

## Véase también {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
