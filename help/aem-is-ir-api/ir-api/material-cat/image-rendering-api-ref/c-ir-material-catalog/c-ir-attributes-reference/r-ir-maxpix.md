---
title: MaxPix
description: Responder límite de tamaño de imagen. Anchura y altura máxima de la imagen de respuesta que se puede devolver al cliente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# MaxPix{#maxpix}

Responder límite de tamaño de imagen. Anchura y altura máxima de la imagen de respuesta que se puede devolver al cliente.

El servidor devuelve un error si una solicitud provoca una imagen de respuesta cuyo ancho o alto es mayor que `attribute::MaxSize`.

## Propiedades {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Dos números enteros, mayores que 0, separados por coma. Anchura y altura en píxeles. También se puede establecer en 0,0 para permitir cualquier tamaño de imagen de respuesta sin limitaciones.

## Predeterminado {#section-45b38dc661854d11b97df5709f4f3434}

Heredado del valor predeterminado::MaxPix si no está definido o si está vacío.

## Véase también {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
