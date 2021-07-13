---
description: Tiempo de vida predeterminado de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en caso de que un registro de catálogo concreto no contenga un valor de caducidad de catálogo válido o de caducidad de viñeta, o si se accede directamente a un archivo de viñeta o a un archivo de material, en lugar de hacerlo mediante un registro de catálogo.
solution: Experience Manager
title: Vencimiento
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---

# Vencimiento{#expiration}

Tiempo de vida predeterminado de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en caso de que un registro de catálogo concreto no contenga un valor de catálogo válido::Caducidad o viñeta::Caducidad, o si se accede directamente a un archivo de viñeta o a un archivo de material, en lugar de hacerlo mediante un registro de catálogo.

## Propiedades {#section-8e2bade105ec4905ae5c4911f500279f}

Número real, 0 o bueno. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Establézcalo en 0 para que siempre caduque la imagen de respuesta inmediatamente, lo que deshabilita efectivamente el almacenamiento en caché del cliente. Configúrelo en -1 para marcar como *nunca caduca*.

## Predeterminado {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Heredado del valor predeterminado::Expiration si no está definido o si está vacío.

## Véase también {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catálogo::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [viñeta::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
