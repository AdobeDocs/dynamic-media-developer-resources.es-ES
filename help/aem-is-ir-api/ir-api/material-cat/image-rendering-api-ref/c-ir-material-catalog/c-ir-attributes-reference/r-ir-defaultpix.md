---
description: Tamaño de imagen de procesamiento predeterminado. El servidor restringe las imágenes de respuesta para que no superen este ancho y alto, si la solicitud no especifica el tamaño de vista que utiliza explícitamente wid= o hei=.
seo-description: Tamaño de imagen de procesamiento predeterminado. El servidor restringe las imágenes de respuesta para que no superen este ancho y alto, si la solicitud no especifica el tamaño de vista que utiliza explícitamente wid= o hei=.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 27574811-a920-4e54-8635-5a643b8655ef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# DefaultPix{#defaultpix}

Tamaño de imagen de procesamiento predeterminado. El servidor restringe las imágenes de respuesta para que no superen este ancho y alto, si la solicitud no especifica el tamaño de vista que utiliza explícitamente wid= o hei=.

## Propiedades {#section-9dc5474fc75842308796ab6440b29611}

Dos números enteros, 0 o más, separados por coma. Anchura y altura en píxeles. Puede que uno o ambos valores estén establecidos en 0 para mantenerlos sin restricciones.

No aplicable a solicitudes anidadas o incrustadas.

## Predeterminado {#section-1935781c561e4679aa87a5bcced8df90}

Se hereda de `default::DefaultPix` si no está definida o si está vacía.

## Véase también {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
