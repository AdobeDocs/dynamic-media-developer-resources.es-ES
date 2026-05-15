---
title: op_sharpen
description: Enfocar imagen. Aplica un filtro de enfoque básico a la capa o a la imagen de vista final, después de todo el escalado, si layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
TQID: 'https://experienceleague.adobe.com/CLyNZKJir4mYZ2L04ZKpnkNk6LX9xs8VUwnwwPrs-Zc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 3%

---

# op_sharpen{#op-sharpen}

Enfocar imagen. Aplica un filtro de enfoque básico a la capa o a la imagen de vista final, después de todo el escalado, si layer=comp.

`op_sharpen=0|1`

La máscara de capa o la máscara compuesta también se enfoca.

## Propiedades {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Atributo de capa o atributo de vista. Se aplica a la capa actual o a la imagen de vista final si `layer=comp`. Ignorado por las capas de efecto.

## Predeterminado {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, sin efecto de enfoque.

## Ejemplo {#section-3202122df5db4e14b358ecabfb6d8b85}

Compensa el ligero desenfoque causado por el remuestreo de imágenes. También aumentamos la calidad del JPEG para evitar artefactos de JPEG adicionales a lo largo de los bordes afilados.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Véase también {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
