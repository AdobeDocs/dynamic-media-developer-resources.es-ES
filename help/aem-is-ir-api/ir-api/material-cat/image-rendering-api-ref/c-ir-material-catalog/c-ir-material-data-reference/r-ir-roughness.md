---
description: Enrojecimiento de la superficie. Especifica el brillo relativo de la superficie del material. Se utiliza junto con el Tipo de catálogo y el Brillo del catálogo para controlar los efectos de procesamiento de reflejo 3D.
seo-description: Enrojecimiento de la superficie. Especifica el brillo relativo de la superficie del material. Se utiliza junto con el Tipo de catálogo y el Brillo del catálogo para controlar los efectos de procesamiento de reflejo 3D.
seo-title: Rugosidad
solution: Experience Manager
title: Rugosidad
topic: Scene7 Image Serving - Image Rendering API
uuid: d71e4411-dd59-4347-a7c2-132e130ff36b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Rugosidad{#roughness}

Enrojecimiento de la superficie. Especifica el brillo relativo de la superficie del material. Se utiliza junto con el catálogo::Type y catalog::Gloss para controlar los efectos de procesamiento de reflejo 3D.

## Propiedades {#section-70c3f2394fd8477ca83a369448907971}

Número entero. Valor de porcentaje en el rango 0...100. Opcional para todos los materiales. Se utiliza únicamente para viñetas con varios mapas de reflexión o viñetas con capacidad de reflexión 3D. Deje vacío o defina en -1 si no se conoce o no es necesario.

## Predeterminado {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; se utiliza un servidor predeterminado.

## Véase también {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[bold=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [catálogo::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [catálogo::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
