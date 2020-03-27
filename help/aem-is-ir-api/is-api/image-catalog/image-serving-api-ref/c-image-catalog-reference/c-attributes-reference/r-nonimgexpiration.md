---
description: TTL de caché de cliente para respuestas que no son de imagen. Proporciona el intervalo de caducidad para determinadas respuestas que no son de imagen.
seo-description: TTL de caché de cliente para respuestas que no son de imagen. Proporciona el intervalo de caducidad para determinadas respuestas que no son de imagen.
seo-title: NonImgExpiration
solution: Experience Manager
title: NonImgExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 19b37bd4-f7cf-4b5f-be1a-b2d9fda5b4b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# NonImgExpiration{#nonimgexpiration}

TTL de caché de cliente para respuestas que no son de imagen. Proporciona el intervalo de caducidad para determinadas respuestas que no son de imagen.

Proporciona el intervalo de caducidad para determinadas respuestas que no son de imagen, incluidas las enviadas como respuesta a los siguientes comandos:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Propiedades {#section-d37e3113f4b1468b86b5a14e80d94c83}

Número real, 0 o bueno. Número de horas hasta la caducidad desde que se generaron los datos de respuesta. Establezca el valor 0 para que la imagen de respuesta caduque siempre inmediatamente, lo que deshabilita el almacenamiento en caché del cliente para las respuestas de imagen predeterminadas. Establezca en -1 para marcar como *nunca caduca*.

## Predeterminado {#section-96981360c0234b7f824d2ff7c25a7954}

Se hereda de `default::NonImgExpiration` si no está definida o si está vacía.

TTL (Tiempo de vida) es la duración antes de que caduque la caché. El TTL predeterminado es de 6 minutos.

## Véase también {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catálogo::Caducidad](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [atributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
