---
title: IccProfileGray
description: Espacio de color predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta en escala de grises cuando no se especifique ningún espacio de color de salida con icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
TQID: 'https://experienceleague.adobe.com/ZZOkc6f5V3-Luuwr5ku38nIy8snq4kh2lR4dqunXvFc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 2%

---

# IccProfileGray{#iccprofilegray}

Espacio de color predeterminado de escala de grises. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta en escala de grises cuando no se especifique ningún espacio de color de salida con `icc=`.

## Propiedades {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de materiales, del catálogo predeterminado o una ruta de acceso de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil en escala de grises.

## Predeterminado {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Se hereda de `default::IccProfileGray` si no se ha definido o está vacío.

## Véase también {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [atributo::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2), [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
