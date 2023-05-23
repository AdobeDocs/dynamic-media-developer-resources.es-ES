---
title: Vencimiento
description: Duración predeterminada de la caché del cliente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---

# Vencimiento{#expiration}

Duración predeterminada de la caché del cliente. Proporciona un intervalo de caducidad predeterminado en el caso de que un registro de catálogo determinado no contenga un `catalog::Expiration` o `vignette::Expiration` valor. O bien, si se accede directamente a un archivo de viñeta o archivo de material, en lugar de hacerlo mediante un registro de catálogo.

## Propiedades {#section-8e2bade105ec4905ae5c4911f500279f}

Número real, `0` o bueno. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Configure como. `0` para que siempre caduque la imagen de respuesta inmediatamente, lo que deshabilita el almacenamiento en caché del cliente. Configure como. `-1` para marcar como *nunca caducar*.

## Predeterminado {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Heredado de `default::Expiration` si no se define o si está vacío.

## Véase también {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [viñeta::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
