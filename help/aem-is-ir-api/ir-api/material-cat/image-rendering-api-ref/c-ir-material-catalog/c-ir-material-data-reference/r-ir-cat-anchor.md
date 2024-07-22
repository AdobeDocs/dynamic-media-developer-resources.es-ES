---
description: Anclaje de imagen. Especifica el punto de anclaje (punto interactivo) de una textura, borde de pared o imagen adhesiva repetible.
solution: Experience Manager
title: Anclaje
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---

# Anclaje{#anchor}

Anclaje de imagen. Especifica el punto de anclaje (punto interactivo) de una textura, borde de pared o imagen adhesiva repetible.

Se aplica una textura repetible a un objeto de viñeta de modo que el punto de anclaje de la textura se encuentre en el punto de origen de la textura del objeto. Se aplica una imagen de calcomanía a un objeto de viñeta de modo que el punto de anclaje de calcomanía se encuentre en el punto de origen de calcomanía del objeto. Para los bordes de pared, sólo se utiliza el valor x; se omite el valor y.

## Propiedades {#section-bc4bc8b897c64535b88681e57d72942f}

Dos números enteros, separados por una coma. Desplazamiento de píxel relativo a la esquina superior izquierda de la imagen. Se omitió si `catalog::Alignment=3` y por el color sólido y los materiales del gabinete.

## Predeterminado {#section-b7ccc419a356415294706cd295ae96c9}

Si el campo está vacío o no está presente, se utiliza la esquina superior izquierda (0,0) de la imagen para materiales de textura repetible o el centro de la imagen en el caso de materiales calcomanías.

## Véase también {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catálogo::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
