---
description: TTL de caché del cliente para respuestas que no sean de imagen. Proporciona el intervalo de caducidad para determinadas respuestas que no son de imagen.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
TQID: 'https://experienceleague.adobe.com/A21KkwsYFIMp9Pw0WyX-c-3UVlFg2FacObh2jjRVTwA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 2%

---

# NonImgExpiration{#nonimgexpiration}

TTL de caché del cliente para respuestas que no sean de imagen. Proporciona el intervalo de caducidad para determinadas respuestas que no son de imagen.

Proporciona el intervalo de caducidad para determinadas respuestas que no son de imagen, incluidas las enviadas en respuesta a los siguientes comandos:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Propiedades {#section-d37e3113f4b1468b86b5a14e80d94c83}

Número real, 0 o superior. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Establezca el valor en 0 para que la imagen de respuesta siempre caduque inmediatamente, lo que deshabilita de forma efectiva el almacenamiento en caché del cliente para las respuestas de imagen predeterminadas. Definir en -1 para marcar como *nunca caduca*.

## Predeterminado {#section-96981360c0234b7f824d2ff7c25a7954}

Se hereda de `default::NonImgExpiration` si no se ha definido o está vacío.

TTL (Tiempo de vida) es la duración antes de que caduque la caché. El TTL predeterminado es de 6 minutos.

## Véase también {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catálogo::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [atributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
