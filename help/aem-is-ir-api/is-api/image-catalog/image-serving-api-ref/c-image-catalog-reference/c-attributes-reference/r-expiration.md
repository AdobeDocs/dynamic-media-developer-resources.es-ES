---
description: Duración predeterminada de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en el caso de que el valor de catálogo Expiration no sea válido en un registro de catálogo determinado.
solution: Experience Manager
title: Vencimiento
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---

# Vencimiento{#expiration}

Duración predeterminada de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en el caso de que el valor de catálogo::Expiration no sea válido en un registro de catálogo determinado.

## Propiedades {#section-063be3b2f13a48a3a5ab8080718e9812}

Número real, 0 o bueno. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Si se establece en 0, la imagen de respuesta siempre caducará inmediatamente, lo que deshabilita el almacenamiento en caché del cliente. Establezca en -1 para marcar como `never expire`.

## Predeterminado {#section-f55308b195c04083996f6717c8537634}

Heredado de `default::Expiration` si no se define o si está vacío.

TTL (Tiempo de vida) es la duración antes de que caduque la caché. El TTL predeterminado es 10 horas.

## Véase también {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
