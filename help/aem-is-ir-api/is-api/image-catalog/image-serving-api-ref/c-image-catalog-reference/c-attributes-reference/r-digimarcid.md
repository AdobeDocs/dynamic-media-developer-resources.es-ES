---
description: Información de usuario de Digimarc. Especifica la información de usuario para la incrustación de Digimarc.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
TQID: 'https://experienceleague.adobe.com/2kkvN1RLEhbDEmN4cA6lE5nGe9d-T3qcdxgGqF7L3Ig'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 2%

---

# DigimarcId{#digimarcid}

Información de usuario de Digimarc. Especifica la información de usuario para la incrustación de Digimarc.

## Propiedades {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinco o seis números enteros separados por comas. Los números tercero y cuarto ya no se usan:

`creator-id, creator-pin, durability [ , chroma ]`

Digimarc proporciona `creator-id` y `creator-pin` cuando se adquiere el servicio. Los valores no utilizados deben dejarse vacíos.

`durability` especifica la intensidad de incrustación de la marca de agua Digimarc. Puede ser 1, 2, 3 o 4, con 1 que indica la durabilidad más débil y 4 más fuerte.

Establezca `chroma` en 1 para codificar la marca de agua en los datos de crominancia de la imagen o en 0 (valor predeterminado) para codificarla en la luminancia. Esta configuración se ignora al generar imágenes en escala de grises.

## Predeterminado {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Se hereda de `default::DigimarcId` si no se ha definido o está vacío.

## Ejemplo {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Especifique un ID de creador de Digimarc de prueba con la durabilidad establecida en 4.

`DigimarcId= 404407,32,,,4`

## Véase también {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
