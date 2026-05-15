---
description: Límite de tamaño de imagen de respuesta. Anchura y altura máximas para la imagen de respuesta que se devuelve al cliente.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
TQID: 'https://experienceleague.adobe.com/lX4ooC7B0VIJDRr0yZJVmp45qnXbSuimMZSyU9rWLcw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
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
