---
description: Resolución. La resolución de imagen "real", normalmente expresada como píxeles por pulgada, pero también puede estar en otras unidades, como píxeles por metro.
seo-description: Resolución. La resolución de imagen "real", normalmente expresada como píxeles por pulgada, pero también puede estar en otras unidades, como píxeles por metro.
seo-title: Resolución
solution: Experience Manager
title: Resolución
topic: Scene7 Image Serving - Image Rendering API
uuid: 281c7ff6-8f78-4654-98ec-0db4299b80d9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Resolución{#resolution}

Resolución. La resolución de imagen &quot;real&quot;, normalmente expresada como píxeles por pulgada, pero también puede estar en otras unidades, como píxeles por metro.

## Propiedades {#section-985ca2ad858c4e9c9cbb303f55447553}

Número real, mayor que 0. Necesario para materiales de textura y calado, a menos que la resolución de la imagen sea la misma que el atributo::Resolution. Se ignora con materiales de color sólido y de gabinete.

## Predeterminado {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` se utiliza si el campo no está presente, si el valor es 0 o negativo o si el campo está vacío.

## Véase también {#section-2d04df523d7345f6929178cbc637da78}

[atributo::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) ,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
