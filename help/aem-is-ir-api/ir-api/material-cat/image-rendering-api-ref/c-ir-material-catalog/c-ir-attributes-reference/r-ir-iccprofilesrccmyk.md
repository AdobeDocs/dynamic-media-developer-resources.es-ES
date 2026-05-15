---
title: IccProfileSrcCmyk
description: Perfil de color de entrada predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material CMYK que no incrustan un perfil de color.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
TQID: 'https://experienceleague.adobe.com/AX-NqS0F7TjgfLR2S8xyrJukDlB8-n-d17Bcn--AFrg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Perfil de color de entrada predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de material CMYK que no incrustan un perfil de color.

## Propiedades {#section-0cee77438d914c319ec876edb3490821}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes, del catálogo predeterminado o una ruta de acceso de archivo relativa a `attribute::RootPath`. El perfil ICC referenciado debe ser un perfil CMYK.

## Predeterminado {#section-11f6239e0dd14827abf4a95c1b30161c}

Se hereda de `default::IccProfileSrcCmyk` si no se ha definido o está vacío. Si `attribute::IccProfileSrcCmyk` no se resuelve en un perfil válido, se utiliza `attribute::IccProfileCmyk` en su lugar.

## Véase también {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [atributo::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
