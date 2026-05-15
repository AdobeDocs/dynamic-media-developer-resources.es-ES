---
description: Resolución de impresión. Resolución de impresión para la imagen a tamaño completo.
solution: Experience Manager
title: PrintResolution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2168d72a-1f2b-4833-9e6e-ba3d2ddb6d2b
TQID: 'https://experienceleague.adobe.com/ingyge8d-ePPNhXb-CY3KvO365zCVl7WIkS6ldxbOiI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 5%

---

# PrintResolution{#printresolution}

Resolución de impresión. Resolución de impresión para la imagen a tamaño completo.

Este valor está incrustado en el encabezado de la imagen de respuesta, a menos que se sobrescriba con `printRes=`.

## Propiedades {#section-de3c1f73da7b43208beeec841c1778c1}

Número entero mayor que 0. Se expresa en puntos por pulgada. Opcional.

## Predeterminado {#section-0cac992554ec4247ab05f70d9840a045}

`attribute::PrintResolution` se usa si el campo no está presente, si el valor es 0 o si el campo está vacío.

## Véase también {#section-0593faefffe341c5ab8a4aa5da589a04}

[attribute::PrintResolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-printresolution.md#reference-a53c6850077148c9bd88a8c5c1c400c5) , [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [printRes=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-printres.md#reference-84f52afff4704c4b9d58e4bbbaea1491)
