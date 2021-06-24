---
description: TTL de caché de cliente para respuestas de imagen predeterminadas. Proporciona el intervalo de caducidad para las respuestas de imagen predeterminadas (respuestas que devuelven una imagen predeterminada especificada con defaultImage= o attribute DefaultImage).
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---

# DefaultExpiration{#defaultexpiration}

TTL de caché de cliente para respuestas de imagen predeterminadas. Proporciona el intervalo de caducidad para las respuestas de imagen predeterminadas (respuestas que devuelven una imagen predeterminada especificada con defaultImage= o attribute::DefaultImage).

Solo se aplica cuando la imagen predeterminada no está asociada con un registro de catálogo o cuando el registro de catálogo de imágenes predeterminado no proporciona un valor específico `catalog::Expiration`.

## Propiedades {#section-e564512476604fd7b964f9f2903d6d33}

Número real, 0 o bueno. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Si se establece en 0, la imagen de respuesta caducará siempre inmediatamente, lo que deshabilita efectivamente el almacenamiento en caché del cliente para las respuestas de imagen predeterminadas. Configúrelo en `-1` para marcar como `never expire`.

## Predeterminado {#section-131cd32c2e214391857dba5af321f8cd}

Se hereda de `default::DefaultExpiration` si no está definido o si está vacío.

TTL (Tiempo de vida) es la duración antes de que caduque la caché. El TTL predeterminado es 1 hora.

## Véase también {#section-d8642c22e3d947129367dd76366963d6}

[catálogo::Caducidad](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [atributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
