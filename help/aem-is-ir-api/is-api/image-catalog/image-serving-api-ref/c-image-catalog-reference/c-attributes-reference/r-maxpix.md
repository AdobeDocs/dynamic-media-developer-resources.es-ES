---
description: Responder límite de tamaño de imagen. Anchura y altura máxima de la imagen de respuesta que se puede devolver al cliente.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
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
