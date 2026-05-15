---
description: TTL de caché del cliente para respuestas de imagen predeterminadas. Proporciona el intervalo de caducidad para las respuestas de imagen predeterminadas (respuestas que devuelven una imagen predeterminada especificada con defaultImage= o el atributo DefaultImage).
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
TQID: 'https://experienceleague.adobe.com/v-wtXCBtpHpf9mTjoQ58GZ9eXq-yR2tpGT0Kd-DTyNI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 1%

---

# DefaultExpiration{#defaultexpiration}

TTL de caché del cliente para respuestas de imagen predeterminadas. Proporciona el intervalo de caducidad para las respuestas de imagen predeterminadas (respuestas que devuelven una imagen predeterminada especificada con defaultImage= o attribute::DefaultImage).

Solo se aplica cuando la imagen predeterminada no está asociada a un registro de catálogo o cuando el registro de catálogo de imágenes predeterminado no proporciona un valor `catalog::Expiration` específico.

## Propiedades {#section-e564512476604fd7b964f9f2903d6d33}

Número real, 0 o superior. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Establezca el valor en 0 para que la imagen de respuesta siempre caduque inmediatamente, lo que deshabilita de forma efectiva el almacenamiento en caché del cliente para las respuestas de imagen predeterminadas. Se estableció en `-1` para marcar como `never expire`.

## Predeterminado {#section-131cd32c2e214391857dba5af321f8cd}

Se hereda de `default::DefaultExpiration` si no se ha definido o está vacío.

TTL (Tiempo de vida) es la duración antes de que caduque la caché. El TTL predeterminado es 1 hora.

## Véase también {#section-d8642c22e3d947129367dd76366963d6}

[catálogo::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [atributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
