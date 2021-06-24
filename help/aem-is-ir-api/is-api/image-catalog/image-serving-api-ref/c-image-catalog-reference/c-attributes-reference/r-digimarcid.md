---
description: Información de usuario de Digimarc. Especifica la información del usuario para la incrustación de Digimarc.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Información de usuario de Digimarc. Especifica la información del usuario para la incrustación de Digimarc.

## Propiedades {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinco o seis números enteros separados por comas. Los números tercero y cuarto ya no se utilizan:

`creator-id, creator-pin, durability [ , chroma ]`

Digimarc proporciona los `creator-id` y `creator-pin` cuando se compra el servicio. Los valores no utilizados deben dejarse vacíos.

`durability` especifica la fuerza de incrustación de la marca de agua Digimarc. Puede ser 1, 2, 3 ó 4, con 1 indicando la menor durabilidad y 4 la más fuerte.

Establezca `chroma` en 1 para codificar la marca de agua en los datos de crominancia de la imagen o en 0 (predeterminado) para codificarla en la luminancia. Esta configuración se ignora al generar imágenes en escala de grises.

## Predeterminado {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Se hereda de `default::DigimarcId` si no está definido o si está vacío.

## Ejemplo {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Especifique un id de creador de Digimarc de prueba con la durabilidad establecida en 4.

`DigimarcId= 404407,32,,,4`

## Véase también {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catálogo::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
