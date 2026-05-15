---
description: Rugosidad superficial. Especifica el brillo relativo de la superficie de material. Se utiliza junto con el Tipo de catálogo y el Brillo de catálogo para controlar los efectos de procesamiento de reflexión 3D.
solution: Experience Manager
title: Rugosidad
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
TQID: 'https://experienceleague.adobe.com/YvUmUkOLzzbM7Zs-7T35rwYRNrUeh6-QXW339AA3R8Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 2%

---

# Rugosidad{#roughness}

Rugosidad superficial. Especifica el brillo relativo de la superficie de material. Se utiliza junto con catalog::Type y catalog::Gloss para controlar los efectos de procesamiento de la reflexión 3D.

## Propiedades {#section-70c3f2394fd8477ca83a369448907971}

Número entero. Valor de porcentaje dentro del rango 0...100. Opcional para todos los materiales. Solo se utiliza para viñetas con varios mapas de reflexión o viñetas con capacidad de reflexión 3D. Dejar vacío o establecer en -1 si no se conoce o no es necesario.

## Predeterminado {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; se utiliza un servidor predeterminado.

## Véase también {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[áspero=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [catálogo::Brillo](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [catálogo::Tipo](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
