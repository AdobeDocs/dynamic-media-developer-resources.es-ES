---
description: Límite de tamaño de imagen de respuesta. Anchura y altura máximas para la imagen de respuesta que se devuelve al cliente.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# MaxPix{#maxpix}

Límite de tamaño de imagen de respuesta. Anchura y altura máximas para la imagen de respuesta que se devuelve al cliente.

El servidor devuelve un error si una solicitud origina una imagen de respuesta con una anchura o altura superior a `attribute::MaxPix`.

## Propiedades {#section-b175425b9e9f48e0b1a71640f6a9e936}

Dos números enteros mayores que 0 separados por una coma. Ancho y alto en píxeles. También se puede establecer en `0,0` para permitir cualquier tamaño de imagen de respuesta sin limitaciones.

## Predeterminado {#section-1003537434da432fb2af100ecdbf9d72}

Se hereda de `default::MaxPix` si no se ha definido o está vacío.

## Véase también {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
