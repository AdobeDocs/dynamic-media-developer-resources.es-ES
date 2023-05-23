---
description: Información de usuario de Digimarc. Especifica la información de usuario para la incrustación de Digimarc.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Información de usuario de Digimarc. Especifica la información de usuario para la incrustación de Digimarc.

## Propiedades {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinco o seis números enteros separados por comas. Los números tercero y cuarto ya no se usan:

`creator-id, creator-pin, durability [ , chroma ]`

El `creator-id` y `creator-pin` son proporcionados por Digimarc cuando se adquiere el servicio. Los valores no utilizados deben dejarse vacíos.

`durability` especifica la intensidad de incrustación de la marca de agua Digimarc. Puede ser 1, 2, 3 o 4, con 1 que indica la durabilidad más débil y 4 más fuerte.

Establecer `chroma` en 1 para codificar la marca de agua en los datos de crominancia de la imagen o en 0 (valor predeterminado) para codificarla en la luminancia. Esta configuración se ignora al generar imágenes en escala de grises.

## Predeterminado {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Heredado de `default::DigimarcId` si no se define o si está vacío.

## Ejemplo {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Especifique un ID de creador de Digimarc de prueba con la durabilidad establecida en 4.

`DigimarcId= 404407,32,,,4`

## Véase también {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
