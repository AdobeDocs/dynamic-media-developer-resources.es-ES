---
description: Incrustar datos de rutas. Especifica si las rutas de Photoshop incrustadas en la viñeta deben incluirse en la imagen de respuesta.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# pathEmbed{#pathembed}

Incrustar datos de rutas. Especifica si las rutas de Photoshop incrustadas en la viñeta deben incluirse en la imagen de respuesta.

`pathEmbed=0|1`

## Propiedades {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Atributo de solicitud. Se omite si la viñeta no contiene datos de rutas. Los datos de las rutas se escalan a `wid=` o `hei=` si es necesario.

Se omite si el formato de imagen de salida no admite la incrustación de rutas. Consulte la descripción de `fmt=` para obtener una lista de los formatos de imagen de salida que admiten la incrustación de rutas.

## Predeterminado {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, para no incrustar rutas en imágenes de salida.

## Véase también {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
