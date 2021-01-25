---
description: Límite de tamaño de la imagen de respuesta. Ancho y altura máximos de la imagen de respuesta que se pueden devolver al cliente.
seo-description: Límite de tamaño de la imagen de respuesta. Ancho y altura máximos de la imagen de respuesta que se pueden devolver al cliente.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# MaxPix{#maxpix}

Límite de tamaño de la imagen de respuesta. Ancho y altura máximos de la imagen de respuesta que se pueden devolver al cliente.

El servidor devuelve un error si una solicitud provoca una imagen de respuesta cuyo ancho o alto sea mayor que `attribute::MaxPix`.

## Propiedades {#section-b175425b9e9f48e0b1a71640f6a9e936}

Dos números enteros, mayores que 0, separados por coma. Anchura y altura en píxeles. También se puede establecer en `0,0` para permitir cualquier tamaño de imagen de respuesta sin limitaciones.

## Predeterminado {#section-1003537434da432fb2af100ecdbf9d72}

Se hereda de `default::MaxPix` si no está definida o si está vacía.

## Véase también {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
