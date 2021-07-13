---
description: Interpretación de la conversión de color. Proporciona la interpretación predeterminada para conversiones de color cuando la interpretación no se especifica con icc=.
solution: Experience Manager
title: IccRenderIntent
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

Interpretación de la conversión de color. Proporciona la interpretación predeterminada para conversiones de color cuando la interpretación no se especifica con icc=.

## Propiedades {#section-0a38c60e1525426185616c42824aee2c}

Enum. Se establece en 0 para perceptual, 1 para colorimétrico relativo, 2 para saturación, 3 para colorimétrico absoluto. Mantenga empty o establezca en cualquier otro valor para utilizar la interpretación predeterminada definida en el perfil de color.

## Predeterminado {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Se hereda de `default::IccRenderIntent`si no se define. Si está vacío, se aplica &quot;colorimétrico relativo&quot;.

## Véase también {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[atributo::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [atributo::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
