---
description: TTL de caché de cliente para respuestas de imagen predeterminadas. Proporciona el intervalo de caducidad para las respuestas de imagen predeterminadas (respuestas que devuelven una imagen predeterminada especificada con defaultImage= o atributo DefaultImage).
seo-description: TTL de caché de cliente para respuestas de imagen predeterminadas. Proporciona el intervalo de caducidad para las respuestas de imagen predeterminadas (respuestas que devuelven una imagen predeterminada especificada con defaultImage= o atributo DefaultImage).
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultExpiration{#defaultexpiration}

TTL de caché de cliente para respuestas de imagen predeterminadas. Proporciona el intervalo de caducidad para las respuestas de imagen predeterminadas (respuestas que devuelven una imagen predeterminada especificada con defaultImage= o attribute::DefaultImage).

Solo se aplica cuando la imagen predeterminada no está asociada a un registro de catálogo o cuando el registro de catálogo de imágenes predeterminado no proporciona un valor específico `catalog::Expiration` .

## Propiedades {#section-e564512476604fd7b964f9f2903d6d33}

Número real, 0 o bueno. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Establezca el valor 0 para que la imagen de respuesta caduque siempre inmediatamente, lo que deshabilita el almacenamiento en caché del cliente para las respuestas de imagen predeterminadas. Establezca en `-1` marcar como `never expire`.

## Predeterminado {#section-131cd32c2e214391857dba5af321f8cd}

Se hereda de `default::DefaultExpiration` si no está definida o si está vacía.

TTL (Tiempo de vida) es la duración antes de que caduque la caché. El TTL predeterminado es 1 hora.

## Véase también {#section-d8642c22e3d947129367dd76366963d6}

[catálogo::Caducidad](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [atributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
