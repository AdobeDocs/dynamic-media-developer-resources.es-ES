---
description: Tiempo de espera predeterminado de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en caso de que un registro de catálogo en particular no contenga un valor de caducidad de catálogo válido.
seo-description: Tiempo de espera predeterminado de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en caso de que un registro de catálogo en particular no contenga un valor de caducidad de catálogo válido.
seo-title: Vencimiento
solution: Experience Manager
title: Vencimiento
topic: Scene7 Image Serving - Image Rendering API
uuid: 26b2abee-8bd1-4011-90ff-f5143826ac0d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Caducidad{#expiration}

Tiempo de espera predeterminado de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en caso de que un registro de catálogo en particular no contenga un valor de catálogo válido::Expiration.

## Propiedades {#section-063be3b2f13a48a3a5ab8080718e9812}

Número real, 0 o bueno. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Establezca el valor 0 para que la imagen de respuesta caduque siempre inmediatamente, lo que deshabilita el almacenamiento en caché del cliente. Establezca en -1 para marcar como `never expire`.

## Predeterminado {#section-f55308b195c04083996f6717c8537634}

Se hereda de `default::Expiration` si no está definida o si está vacía.

TTL (Tiempo de vida) es la duración antes de que caduque la caché. El TTL predeterminado es de 10 horas.

## Véase también {#section-b2411d99ddb14115ad475d506efd8967}

[catálogo::Caducidad](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [atributo::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [atributo::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
