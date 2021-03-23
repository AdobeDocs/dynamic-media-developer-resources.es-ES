---
description: Anclaje de imagen. Especifica el punto de ancla (zona interactiva) de una textura, borde de pared o imagen de calco repetible.
seo-description: Anclaje de imagen. Especifica el punto de ancla (zona interactiva) de una textura, borde de pared o imagen de calco repetible.
seo-title: Anclaje
solution: Experience Manager
title: Anclaje
uuid: 0b1a0fea-b299-44dc-b9fd-5916130b2ef3
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# Anclaje{#anchor}

Anclaje de imagen. Especifica el punto de ancla (zona interactiva) de una textura, borde de pared o imagen de calco repetible.

Se aplica una textura repetible a un objeto de viñeta, de modo que el punto de ancla de textura se encuentra en el punto de origen de la textura del objeto. Se aplica una imagen de calco a un objeto de viñeta, de modo que el punto de ancla de calco se encuentra en el punto de origen de calco del objeto. Para los bordes de pared, solo se utiliza el valor x; se ignora el valor y .

## Propiedades {#section-bc4bc8b897c64535b88681e57d72942f}

Dos números enteros separados por coma. Desplazamiento de píxeles en relación con la esquina superior izquierda de la imagen. Se ignora si `catalog::Alignment=3` y por materiales de color sólido y gabinete.

## Predeterminado {#section-b7ccc419a356415294706cd295ae96c9}

Si el campo está vacío o no está presente, se utilizará la esquina superior izquierda (0,0) de la imagen para materiales de textura repetibles, o el centro de la imagen en caso de materiales de calco.

## Véase también {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catálogo::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
