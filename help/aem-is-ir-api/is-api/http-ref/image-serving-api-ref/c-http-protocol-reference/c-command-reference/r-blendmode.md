---
description: Modo de fusión. Especifica el tipo de fusión utilizado cuando se compone la capa. Simula los modos de mezcla más utilizados disponibles en Photoshop. Consulte la documentación de Photoshop para obtener más información.
seo-description: Modo de fusión. Especifica el tipo de fusión utilizado cuando se compone la capa. Simula los modos de mezcla más utilizados disponibles en Photoshop. Consulte la documentación de Photoshop para obtener más información.
seo-title: blendMode
solution: Experience Manager
title: blendMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ae30495-c10b-4c55-968e-effb602a0857
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# blendMode{#blendmode}

Modo de fusión. Especifica el tipo de fusión utilizado cuando se compone la capa. Simula los modos de mezcla más utilizados disponibles en Photoshop. Consulte la documentación de Photoshop para obtener más información.

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## Propiedades {#section-418aad5a417f49929d1953e226e5c8dd}

Atributo de capa. Omitido por `layer=0` y `layer=comp`.

## Predeterminado {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## Ejemplo {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## Véase también {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
