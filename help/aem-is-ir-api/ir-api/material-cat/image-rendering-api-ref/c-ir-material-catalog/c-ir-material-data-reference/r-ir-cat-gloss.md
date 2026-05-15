---
description: Brillo de superficie Especifica el brillo relativo de la superficie de material.
solution: Experience Manager
title: Brillo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
TQID: 'https://experienceleague.adobe.com/Q1mOPjFXFnSPVRsvYpKs3a-15g1BfxQRCsFaMRBZNTw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# Brillo{#gloss}

Brillo de superficie Especifica el brillo relativo de la superficie de material.

Este valor lo utiliza el procesador para los siguientes fines:

* Seleccione el mapa de iluminación cuando `catalog::Illum` sea -1.
* Controla la representación del efecto de brillo (reflexión especular) junto con `catalog::Type`.
* Controla los efectos de representación de reflexión 3D junto con `catalog::Type` y `catalog::Roughness`.

## Propiedades {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Número entero. Número de porcentaje en el rango 0...100. Opcional para todos los materiales. Solo se utiliza para viñetas con varios mapas de reflexión o viñetas con capacidad de reflexión 3D. Dejar vacío o establecer en -1 si no se conoce o no es necesario.

## Predeterminado {#section-2352721073524f1a8d461f64a363aac9}

La viñeta proporciona un valor predeterminado si este valor se establece en -1.

## Véase también {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catálogo::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catálogo::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
