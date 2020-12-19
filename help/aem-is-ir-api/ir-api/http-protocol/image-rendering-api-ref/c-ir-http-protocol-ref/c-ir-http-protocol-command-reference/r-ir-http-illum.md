---
description: Selector de mapa de iluminación. Especifica el mapa de iluminación con el que este material prefiere procesarse.
seo-description: Selector de mapa de iluminación. Especifica el mapa de iluminación con el que este material prefiere procesarse.
seo-title: illum
solution: Experience Manager
title: illum
topic: Scene7 Image Serving - Image Rendering API
uuid: 16c7144f-7f16-47d1-8140-fd679e702660
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# illum{#illum}

Selector de mapa de iluminación. Especifica el mapa de iluminación con el que este material prefiere procesarse.

`illum=-1|0|1|2`

Si el mapa de iluminación especificado no está disponible en la viñeta destinatario, se utiliza el mapa disponible más cercano.

`illum=-1` especifica que el mapa de iluminación se selecciona automáticamente en función del  `gloss=` valor.

## Propiedades {#section-aace8466566e4cf1a0c5a6c0167245c9}

Atributo Material. Se omite si la viñeta no define varios mapas de iluminación.

## Predeterminado {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Véase también {#section-9132e60381c64aa3a8ed1319690db55e}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
