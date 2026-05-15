---
title: IccProfileSrcRgb
description: Perfil de color de entrada predeterminado de RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes y viñetas de material de RGB que no incrustan un perfil de color. También para valores de color de RGB especificados con varios comandos de procesamiento de imágenes, como bgc= y color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
TQID: 'https://experienceleague.adobe.com/P38eqZb2sT2vSm0qJDljwW319qWiCttn3V3CPwC-IWg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

Perfil de color de entrada predeterminado de RGB. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes y viñetas de material de RGB que no incrustan un perfil de color. También para los valores de color de RGB especificados con varios comandos de procesamiento de imágenes, como `bgc=` y `color=`.

## Propiedades {#section-c22966bba03e43c08e9d3fb91bfdd465}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes, del catálogo predeterminado o una ruta de acceso de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil de RGB.

## Predeterminado {#section-0171cd6680284bfa9844b9cc3644ca61}

Se hereda de `default::IccProfileSrcRgb` si no se ha definido o está vacío. Si `attribute::IccProfileSrcRgb` no se resuelve en un perfil válido, se utiliza `attribute::IccProfileRgb` en su lugar.

## Véase también {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [atributo::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
