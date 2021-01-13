---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 3148cc25-3b9a-499a-b0da-1ebe9ae99f69
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# TimeStamp{#timestamp}

Si `attribute::UseLastModified` está establecido, el valor `catalog::TimeStamp` se devuelve en la respuesta HTTP como encabezado HTTP de última modificación. El encabezado Última modificación siempre se devuelve para el contenido estático, aunque `attribute::UseLastModified` no esté establecido.

Para el contenido de imágenes y SVG, `catalog::TimeStamp` también se utiliza para la validación de caché basada en catálogo (consulte ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`).

## Propiedades {#section-2298a384b5cb43929542655c5a49beb2}

Valor de fecha y hora en formato Java. Puede ser el número entero de milisegundos desde la medianoche, el 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*::  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*::  *`ss`* GMT  *`offset`*

*`hh`* está en el intervalo 0 - 23.

*`zzz`* es un código de zona horaria de tres o cuatro caracteres, como &quot;GMT&quot; o &quot;PST&quot;. Cuenta para el horario de verano en el código de zona horaria. Por ejemplo, &#39;PST&#39; para la hora estándar del Pacífico en comparación con &#39;PDT&#39; para la hora de verano del Pacífico).

*`offset`* es un huso horario compensado en horas o  `hours:minutes`, en relación con GMT. Por ejemplo, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Deben estar presentes todos los elementos de los valores de fecha y hora con formato de cadena. Si el valor de fecha y hora no tiene el formato correcto, se ignora y se utiliza la hora de modificación del archivo ` *`catálogo`*.ini` en su lugar.

## Predeterminado {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` si el campo está vacío o no está presente.

## Véase también {#section-c42a427aa4794c548408dc4de028d578}

[atributo::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [atributo::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [atributo::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
