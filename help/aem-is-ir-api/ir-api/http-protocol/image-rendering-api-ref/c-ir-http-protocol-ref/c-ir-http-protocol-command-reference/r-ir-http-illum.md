---
title: illum
description: Selector de mapa de iluminación. Especifica el mapa de iluminación con el que este material prefiere procesarse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# illum{#illum}

Selector de mapa de iluminación. Especifica el mapa de iluminación con el que este material prefiere procesarse.

`illum=-1|0|1|2`

Si el mapa de iluminación especificado no está disponible en la viñeta de destino, se utiliza el mapa disponible más cercano.

`illum=-1` Especifica que el mapa de iluminación se selecciona automáticamente en función del `gloss=` valor.

## Propiedades {#section-aace8466566e4cf1a0c5a6c0167245c9}

Atributo de material. Se omite si la viñeta no define varios mapas de iluminación.

## Predeterminado {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Véase también {#section-9132e60381c64aa3a8ed1319690db55e}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
