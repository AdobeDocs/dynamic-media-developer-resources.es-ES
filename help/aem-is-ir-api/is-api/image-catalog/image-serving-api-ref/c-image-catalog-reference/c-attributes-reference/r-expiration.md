---
description: Tiempo de vida predeterminado de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en caso de que un registro de catálogo en particular no contenga un valor de caducidad de catálogo válido.
solution: Experience Manager
title: Vencimiento
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---


# Caducidad{#expiration}

Tiempo de vida predeterminado de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en caso de que un registro de catálogo en particular no contenga un valor de catálogo válido::Expiration .

## Propiedades {#section-063be3b2f13a48a3a5ab8080718e9812}

Número real, 0 o bueno. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Establézcalo en 0 para que siempre caduque la imagen de respuesta inmediatamente, lo que deshabilita efectivamente el almacenamiento en caché del cliente. Configúrelo en -1 para marcar como `never expire`.

## Predeterminado {#section-f55308b195c04083996f6717c8537634}

Se hereda de `default::Expiration` si no está definido o si está vacío.

TTL (Tiempo de vida) es la duración antes de que caduque la caché. El TTL predeterminado es de 10 horas.

## Véase también {#section-b2411d99ddb14115ad475d506efd8967}

[catálogo::Caducidad](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [atributo::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [atributo::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
