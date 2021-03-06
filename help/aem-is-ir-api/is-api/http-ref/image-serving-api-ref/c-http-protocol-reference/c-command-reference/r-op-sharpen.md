---
description: Enfoque la imagen. Aplica un filtro de enfoque básico a la capa o a la imagen de vista final, después de todo el escalado, si layer=comp.
solution: Experience Manager
title: op_sharpen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# op_sharpen{#op-sharpen}

Enfoque la imagen. Aplica un filtro de enfoque básico a la capa o a la imagen de vista final, después de todo el escalado, si layer=comp.

`op_sharpen=0|1`

La máscara de capa o la máscara compuesta también se endurecen.

## Propiedades {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Atributo de capa o atributo de vista. Se aplica a la capa actual o a la imagen de vista final si es `layer=comp`. Ignorado por capas de efecto.

## Predeterminado {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, para que no se produzca ningún efecto de nitidez.

## Ejemplo {#section-3202122df5db4e14b358ecabfb6d8b85}

Compensa el ligero desenfoque causado por el remuestreo de la imagen. También aumentamos la calidad JPEG para evitar artefactos JPEG adicionales a lo largo de los bordes afilados.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Véase también {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
