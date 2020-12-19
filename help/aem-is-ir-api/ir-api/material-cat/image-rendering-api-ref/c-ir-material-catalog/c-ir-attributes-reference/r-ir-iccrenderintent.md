---
description: Calidad de representación de conversión de color. Proporciona la interpretación predeterminada para las conversiones de color cuando la interpretación no se especifica con icc=.
seo-description: Calidad de representación de conversión de color. Proporciona la interpretación predeterminada para las conversiones de color cuando la interpretación no se especifica con icc=.
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
topic: Scene7 Image Serving - Image Rendering API
uuid: a9648405-32c3-4762-bbb2-11e97d4f8374
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# IccRenderIntent{#iccrenderintent}

Calidad de representación de conversión de color. Proporciona la interpretación predeterminada para las conversiones de color cuando la interpretación no se especifica con icc=.

## Propiedades {#section-0a38c60e1525426185616c42824aee2c}

Enum. Se establece en 0 para perceptual, 1 para colorimétrico relativo, 2 para saturación, 3 para colorimétrico absoluto. Mantenga vacío o defina cualquier otro valor para utilizar la interpretación predeterminada definida en el perfil de color.

## Predeterminado {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Se hereda de `default::IccRenderIntent`si no se define. Si está vacío, se aplica &#39;colorimétrico relativo&#39;.

## Véase también {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[atributo::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [atributo::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
