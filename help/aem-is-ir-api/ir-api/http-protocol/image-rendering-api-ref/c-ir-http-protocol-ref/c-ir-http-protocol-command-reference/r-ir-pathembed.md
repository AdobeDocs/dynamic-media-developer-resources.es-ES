---
description: Incrustar datos de rutas. Especifica si las rutas de Photoshop incrustadas en la viñeta deben incluirse en la imagen de respuesta.
seo-description: Incrustar datos de rutas. Especifica si las rutas de Photoshop incrustadas en la viñeta deben incluirse en la imagen de respuesta.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: d40ea1b5-f2d3-4f81-b96f-abb4eb7eb2b3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# pathEmbed{#pathembed}

Incrustar datos de rutas. Especifica si las rutas de Photoshop incrustadas en la viñeta deben incluirse en la imagen de respuesta.

`pathEmbed=0|1`

## Propiedades {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Solicitar atributo. Se omite si la viñeta no contiene datos de rutas de acceso. Los datos de las rutas se escalan a `wid=` y/o `hei=` si es necesario.

Se omite si el formato de imagen de salida no admite la incrustación de rutas. Consulte la descripción de `fmt=` para obtener una lista de los formatos de imagen de salida que admiten la incrustación de rutas.

## Predeterminado {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, para no incrustar rutas en imágenes de salida.

## Véase también {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
