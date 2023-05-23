---
description: Rugosidad superficial. Especifica el brillo relativo de la superficie de material. Se utiliza junto con el Tipo de catálogo y el Brillo de catálogo para controlar los efectos de procesamiento de reflexión 3D.
solution: Experience Manager
title: Rugosidad
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---

# Rugosidad{#roughness}

Rugosidad superficial. Especifica el brillo relativo de la superficie de material. Se utiliza junto con catalog::Type y catalog::Gloss para controlar los efectos de procesamiento de la reflexión 3D.

## Propiedades {#section-70c3f2394fd8477ca83a369448907971}

Número entero. Valor de porcentaje dentro del rango 0...100. Opcional para todos los materiales. Solo se utiliza para viñetas con varios mapas de reflexión o viñetas con capacidad de reflexión 3D. Dejar vacío o establecer en -1 si no se conoce o no es necesario.

## Predeterminado {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; se utiliza un servidor predeterminado.

## Véase también {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[áspero=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [catalog::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
