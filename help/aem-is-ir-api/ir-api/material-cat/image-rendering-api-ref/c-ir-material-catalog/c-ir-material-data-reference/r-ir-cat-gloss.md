---
description: Luminosidad de la superficie Especifica el brillo relativo de la superficie del material.
seo-description: Luminosidad de la superficie Especifica el brillo relativo de la superficie del material.
seo-title: Brillo
solution: Experience Manager
title: Brillo
topic: Scene7 Image Serving - Image Rendering API
uuid: 7db83f99-15ab-4c43-adfb-07ad0b0c9707
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Brillo{#gloss}

Luminosidad de la superficie Especifica el brillo relativo de la superficie del material.

El procesador utiliza este valor para los siguientes fines:

* Seleccione el mapa de iluminación cuando `catalog::Illum` sea -1.
* Controla el procesamiento del efecto de brillo (reflejo especular) junto con `catalog::Type`.
* Controla los efectos de procesamiento de reflejo 3D junto con `catalog::Type` y `catalog::Roughness`.

## Propiedades {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Número entero. Número de porcentaje en el rango 0...100. Opcional para todos los materiales. Se utiliza únicamente para viñetas con varios mapas de reflexión o viñetas con capacidad de reflexión 3D. Deje vacío o defina en -1 si no se conoce o no es necesario.

## Predeterminado {#section-2352721073524f1a8d461f64a363aac9}

La viñeta proporciona un valor predeterminado si este valor se establece en -1.

## Véase también {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catálogo::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catálogo::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
