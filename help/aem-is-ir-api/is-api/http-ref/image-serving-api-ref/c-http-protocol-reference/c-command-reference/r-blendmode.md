---
description: Modo de fusión. Especifica el tipo de fusión utilizado cuando se compone la capa. Simula los modos de mezcla más utilizados disponibles en Photoshop. Consulte la documentación de Photoshop para obtener más información.
solution: Experience Manager
title: blendMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 8f0b8b0a-a8ac-4932-986c-5d14d3311f1b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 15%

---

# mergeMode{#blendmode}

Modo de fusión. Especifica el tipo de fusión utilizado cuando se compone la capa. Simula los modos de mezcla más utilizados disponibles en Photoshop. Consulte la documentación de Photoshop para obtener más información.

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## Propiedades {#section-418aad5a417f49929d1953e226e5c8dd}

Atributo de capa. Ignorado por `layer=0` y `layer=comp`.

## Predeterminado {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## Ejemplo {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## Véase también {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
