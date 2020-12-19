---
description: Tamaño de imagen. Tamaño de píxel de la imagen de resolución completa a la que hace referencia la ruta de catálogo.
seo-description: Tamaño de imagen. Tamaño de píxel de la imagen de resolución completa a la que hace referencia la ruta de catálogo.
seo-title: Tamaño
solution: Experience Manager
title: Tamaño
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 11%

---


# Tamaño{#size}

Tamaño de imagen. Tamaño de píxel de la imagen de resolución completa a la que hace referencia el catálogo::Path.

Si se proporciona este valor, el servicio de imágenes lo utiliza para evitar tener que abrir la imagen para obtener el tamaño real de la imagen.

>[!NOTE]
>
>Si se proporciona `catalog::Size`y no es el mismo que el tamaño real de la imagen de resolución completa, puede producirse un comportamiento no definido.

## Propiedades {#section-5c914ec8b1444a8e99d811b647cd42a3}

Dos números enteros, cada uno bueno que 0, separados por coma. Opcional.

## Predeterminado {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Si el campo no está presente o si el campo está vacío, se utiliza el tamaño real de la imagen.

## Véase también {#section-e63797357d5a4119a10db1e6e088f6e9}

[catálogo::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ,  [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
