---
title: pathEmbed
description: Incrustar datos de rutas. Especifica si las rutas Photoshop del archivo de imagen de origen de nivel 0 deben incluirse en la imagen de respuesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
TQID: 'https://experienceleague.adobe.com/ES7nAoYjO6Y4naU2c5TIPotPUTjncwjRMLL7-4--XpE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 2%

---

# pathEmbed{#pathembed}

Incrustar datos de rutas. Especifica si las rutas Photoshop del archivo de imagen de origen de nivel 0 deben incluirse en la imagen de respuesta.

`pathEmbed=0|1`

## Propiedades {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Atributo de solicitud. Se ignora si la imagen de origen no contiene datos de rutas. Los datos de rutas se escalan y giran como los datos de imagen. Solo se procesan las rutas de acceso de la imagen de origen de `layer=0`; las rutas de acceso de otras imágenes de capa se omiten.

Se ignora si el formato de imagen de salida no admite la incrustación de rutas. Consulte la descripción de `fmt=` para obtener una lista de los formatos de imagen de salida que admiten la incrustación de rutas.

## Restricciones {#section-697cddb79a1542bc8457d2f4f59eec69}

Las rutas de Photoshop abiertas (rutas que no forman bucles cerrados) no son compatibles con la incrustación en la imagen de respuesta en este momento.

## Predeterminado {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, para no incrustar rutas en imágenes de salida.

## Véase también {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
