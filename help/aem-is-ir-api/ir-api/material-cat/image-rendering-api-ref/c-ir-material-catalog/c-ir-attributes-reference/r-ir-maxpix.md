---
description: Límite de tamaño de la imagen de respuesta. Ancho y altura máximos de la imagen de respuesta que se pueden devolver al cliente.
seo-description: Límite de tamaño de la imagen de respuesta. Ancho y altura máximos de la imagen de respuesta que se pueden devolver al cliente.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 8fc5e032-cfbb-40b5-9c3a-a2ec1bc4c3e2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# MaxPix{#maxpix}

Límite de tamaño de la imagen de respuesta. Ancho y altura máximos de la imagen de respuesta que se pueden devolver al cliente.

El servidor devuelve un error si una solicitud provoca una imagen de respuesta cuya anchura y/o altura sean mayores que `attribute::MaxSize`.

## Propiedades {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Dos números enteros, mayores que 0, separados por coma. Anchura y altura en píxeles. También se puede establecer en 0,0 para permitir cualquier tamaño de imagen de respuesta sin limitaciones.

## Predeterminado {#section-45b38dc661854d11b97df5709f4f3434}

Se hereda del valor predeterminado::MaxPix si no está definido o si está vacío.

## Véase también {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
