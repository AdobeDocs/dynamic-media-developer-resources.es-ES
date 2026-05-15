---
title: Materiales
description: El procesamiento de imágenes aplica materiales a grupos u objetos en viñetas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
TQID: 'https://experienceleague.adobe.com/MNCMxRxVGLF2rsr7NsuTGLzWxM9zkR42MI9MLdaW6G8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 0%

---

# Materiales{#materials}

El procesamiento de imágenes aplica materiales a grupos u objetos en viñetas.

Un material consiste en un conjunto de *atributos*. Algunos atributos son necesarios para ciertos materiales, otros son opcionales y algunos se omiten si están presentes. Muchos atributos tienen valores predeterminados. No todos los materiales pueden aplicarse a todos los objetos (por ejemplo, un material de gabinete no puede aplicarse a un sofá).

El servidor ignora cualquier atributo que aparezca dentro de un segmento de especificación de material (MSS) pero que no aparezca en la lista anterior o en las tablas de material específicas siguientes.

En las tablas siguientes se enumeran los atributos de material básicos. IR admite atributos adicionales para controlar [efectos de procesamiento avanzados](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

A menos que se indique lo contrario, todos los atributos de material son opcionales, con valores por defecto adecuados.

* [Colores sólidos](r-ir-solid-colors.md)
* [Texturas repetibles](r-ir-repeatable-textures.md)
* [Bordes de pared](r-ir-wall-borders.md)
* [Calcomanía](r-ir-decals.md)
* [Armarios](r-ir-cabinets.md)
* [Revestimientos para ventanas](r-ir-window-coverings.md)
