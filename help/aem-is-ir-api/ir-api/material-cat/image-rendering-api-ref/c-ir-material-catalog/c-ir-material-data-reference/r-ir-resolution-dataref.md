---
description: Resolución. Resolución de imagen "real", normalmente expresada como píxeles por pulgada, pero también puede expresarse en otras unidades, como píxeles por metro.
solution: Experience Manager
title: Resolución
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# Resolución{#resolution}

Resolución. Resolución de imagen &quot;real&quot;, normalmente expresada como píxeles por pulgada, pero también puede expresarse en otras unidades, como píxeles por metro.

## Propiedades {#section-985ca2ad858c4e9c9cbb303f55447553}

Número real, mayor que 0. Necesario para los materiales de textura y calcomanía, a menos que la resolución de imagen sea la misma que el atributo::Resolution. Ignorado por el color sólido y los materiales del gabinete.

## Predeterminado {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` se usa si el campo no está presente, si el valor es 0 o negativo o si el campo está vacío.

## Véase también {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) , [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
