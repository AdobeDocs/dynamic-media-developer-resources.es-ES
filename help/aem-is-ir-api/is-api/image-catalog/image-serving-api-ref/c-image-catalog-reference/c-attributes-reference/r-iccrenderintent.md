---
title: IccRenderIntent
description: Interpretación de la conversión de color. Proporciona la interpretación predeterminada para las conversiones de color cuando `icc=` no se especifica para la interpretación.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# IccRenderIntent{#iccrenderintent}

Interpretación de la conversión de color. Proporciona la interpretación predeterminada para las conversiones de color cuando la interpretación no se especifica con `icc=`.

## Propiedades {#section-2540099fb2fc47d29b04642da4f5922a}

Enumeración. Establezca el valor en 0 para perceptual, 1 para colorimétrico relativo, 2 para saturación y 3 para colorimétrico absoluto.

## Predeterminado {#section-61a05067905b44099c228e15de279dbd}

Heredado de `default::IccRenderIntent` si no se define o si está vacío.

## Véase también {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
