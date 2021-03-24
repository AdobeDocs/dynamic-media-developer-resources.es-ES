---
description: Espacio de color predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta de escala de grises cuando no se especifique ningún espacio de color de salida con icc=.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# IccProfileCmyk{#iccprofilecmyk}

Espacio de color predeterminado CMYK. Especifica el nombre del perfil de color ICC que se utilizará para las imágenes de respuesta de escala de grises cuando no se especifique ningún espacio de color de salida con icc=.

## Propiedades {#section-849678b272954bdcb236f49aa54f1609}

Cadena de texto. Si se especifica, debe ser un valor `icc::Name` válido del mapa de perfiles ICC de este catálogo de imágenes o del catálogo predeterminado, o una ruta de archivo relativa a `attribute::RootPath`. El perfil ICC al que se hace referencia debe ser un perfil CMYK.

## Predeterminado {#section-55026b7454af4d868bcb47f7743c9c5b}

Se hereda de `default::IccProfileCmyk` si no está definido o si está vacío.

## Véase también {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [atributo::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
