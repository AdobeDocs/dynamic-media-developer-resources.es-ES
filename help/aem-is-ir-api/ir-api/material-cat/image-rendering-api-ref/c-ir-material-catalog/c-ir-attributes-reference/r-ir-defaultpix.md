---
description: Tamaño de imagen de renderización predeterminado. El servidor restringe el tamaño de las imágenes de respuesta a un tamaño no mayor que este ancho y alto si la solicitud no especifica el tamaño de vista explícitamente mediante wid= o hei=.
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# DefaultPix{#defaultpix}

Tamaño de imagen de renderización predeterminado. El servidor restringe el tamaño de las imágenes de respuesta a un tamaño no mayor que este ancho y alto si la solicitud no especifica el tamaño de vista explícitamente mediante wid= o hei=.

## Propiedades {#section-9dc5474fc75842308796ab6440b29611}

Dos números enteros, 0 o más grandes, separados por coma. Anchura y altura en píxeles. Puede que ambos valores estén establecidos en 0 para mantenerlos sin restricciones.

No aplicable a solicitudes anidadas/incrustadas.

## Predeterminado {#section-1935781c561e4679aa87a5bcced8df90}

Se hereda de `default::DefaultPix` si no está definido o si está vacío.

## Véase también {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
