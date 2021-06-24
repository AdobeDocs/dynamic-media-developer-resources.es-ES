---
description: Interpretación de la conversión de color. Proporciona la interpretación predeterminada para conversiones de color cuando la interpretación no se especifica con icc=.
solution: Experience Manager
title: IccRenderIntent
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# IccRenderIntent{#iccrenderintent}

Interpretación de la conversión de color. Proporciona la interpretación predeterminada para conversiones de color cuando la interpretación no se especifica con icc=.

## Propiedades {#section-2540099fb2fc47d29b04642da4f5922a}

Enum. Se establece en 0 para perceptual, 1 para colorimétrico relativo, 2 para saturación, 3 para colorimétrico absoluto.

## Predeterminado {#section-61a05067905b44099c228e15de279dbd}

Se hereda de `default::IccRenderIntent` si no está definido o si está vacío.

## Véase también {#section-7da9ff3038ca452a9f7375a1ca0581af}

[atributo::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) *,  [atributo::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
