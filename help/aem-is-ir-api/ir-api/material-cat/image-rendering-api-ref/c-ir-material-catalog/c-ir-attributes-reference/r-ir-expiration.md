---
description: Tiempo de vida predeterminado de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en caso de que un registro de catálogo concreto no contenga un valor de caducidad de catálogo válido o de caducidad de viñeta, o si se accede directamente a un archivo de viñeta o a un archivo de material, en lugar de hacerlo mediante un registro de catálogo.
seo-description: Tiempo de vida predeterminado de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en caso de que un registro de catálogo concreto no contenga un valor de caducidad de catálogo válido o de caducidad de viñeta, o si se accede directamente a un archivo de viñeta o a un archivo de material, en lugar de hacerlo mediante un registro de catálogo.
seo-title: Vencimiento
solution: Experience Manager
title: Vencimiento
uuid: 2b56f9ec-2b25-4e6a-aead-6dad3d2df975
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---


# Caducidad{#expiration}

Tiempo de vida predeterminado de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en caso de que un registro de catálogo concreto no contenga un valor de catálogo válido::Caducidad o viñeta::Caducidad, o si se accede directamente a un archivo de viñeta o a un archivo de material, en lugar de hacerlo mediante un registro de catálogo.

## Propiedades {#section-8e2bade105ec4905ae5c4911f500279f}

Número real, 0 o bueno. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Establézcalo en 0 para que siempre caduque la imagen de respuesta inmediatamente, lo que deshabilita efectivamente el almacenamiento en caché del cliente. Configúrelo en -1 para marcar como *nunca caduca*.

## Predeterminado {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Heredado del valor predeterminado::Expiration si no está definido o si está vacío.

## Véase también {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catálogo::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [viñeta::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
