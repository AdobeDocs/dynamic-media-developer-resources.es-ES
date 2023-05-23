---
title: DefaultPix
description: Tamaño de imagen de procesamiento predeterminado. El servidor limita el tamaño de las imágenes de respuesta a esta altura y anchura máximas, a no ser que la solicitud especifique el tamaño de vista por medio de wid= o hei=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 2%

---

# DefaultPix{#defaultpix}

Tamaño de imagen de procesamiento predeterminado. El servidor limita el tamaño de las imágenes de respuesta a esta altura y anchura máximas, a no ser que la solicitud especifique el tamaño de vista por medio de wid= o hei=.

## Propiedades {#section-9dc5474fc75842308796ab6440b29611}

Dos números enteros, 0 o más, separados por una coma. Ancho y alto en píxeles. Uno o ambos valores pueden establecerse en 0 para mantenerlos sin restricciones.

No aplicable a solicitudes anidadas/incrustadas.

## Predeterminado {#section-1935781c561e4679aa87a5bcced8df90}

Heredado de `default::DefaultPix` si no se define o si está vacío.

## Véase también {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
