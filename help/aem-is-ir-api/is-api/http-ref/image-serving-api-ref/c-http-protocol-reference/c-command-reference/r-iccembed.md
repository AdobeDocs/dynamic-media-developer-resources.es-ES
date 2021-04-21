---
description: Incrustar perfil de color. Especifica si el perfil de color ICC de trabajo o el perfil especificado con icc= deben incrustarse en la imagen de respuesta.
solution: Experience Manager
title: iccEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---


# iccEmbed{#iccembed}

Incrustar perfil de color. Especifica si el perfil de color ICC de trabajo o el perfil especificado con icc= deben incrustarse en la imagen de respuesta.

`iccEmbed=0|1`

## Propiedades {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Atributo de solicitud. Se omite si no hay ningún perfil disponible para incrustar.

## Predeterminado {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`, para no incrustar perfiles ICC en imágenes de salida. Se omite si el formato de imagen de salida no admite la incrustación de perfiles ICC.

Consulte [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) para obtener más información.

## Véase también {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[atributo::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ,  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
