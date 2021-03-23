---
description: Responder límite de tamaño de imagen. Anchura y altura máxima de la imagen de respuesta que se puede devolver al cliente.
seo-description: Responder límite de tamaño de imagen. Anchura y altura máxima de la imagen de respuesta que se puede devolver al cliente.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# MaxPix{#maxpix}

Responder límite de tamaño de imagen. Anchura y altura máxima de la imagen de respuesta que se puede devolver al cliente.

El servidor devuelve un error si una solicitud provoca una imagen de respuesta cuyo ancho o alto sea mayor que `attribute::MaxPix`.

## Propiedades {#section-b175425b9e9f48e0b1a71640f6a9e936}

Dos números enteros, mayores que 0, separados por coma. Anchura y altura en píxeles. También se puede configurar en `0,0` para permitir cualquier tamaño de imagen de respuesta sin limitaciones.

## Predeterminado {#section-1003537434da432fb2af100ecdbf9d72}

Se hereda de `default::MaxPix` si no está definido o si está vacío.

## Véase también {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
