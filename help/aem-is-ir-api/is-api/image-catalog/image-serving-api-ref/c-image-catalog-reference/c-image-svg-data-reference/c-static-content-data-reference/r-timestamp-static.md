---
title: TimeStamp
description: Si se establece attribute::UseLastModified, el valor catalog::TimeStamp se devuelve en la respuesta HTTP como un encabezado HTTP de Última modificación. El encabezado Última modificación siempre se devuelve para el contenido estático, incluso si no se ha establecido "attribute::UseLastModified".
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3c47b14d-b629-474d-952a-b09e1b1162b4
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Si se establece `attribute::UseLastModified`, el valor `catalog::TimeStamp` se devuelve en la respuesta HTTP como un encabezado HTTP de última modificación. El encabezado Última modificación siempre se devuelve para el contenido estático, aunque no se haya establecido `attribute::UseLastModified`.

Para el contenido de imágenes y SVG, `catalog::TimeStamp` también se usa para la validación de caché basada en catálogos (vea [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Propiedades {#section-2298a384b5cb43929542655c5a49beb2}

Valor de fecha y hora en formato Java. Puede ser el número entero de milisegundos desde la medianoche del 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* está en el intervalo de 0 a 23.

*`zzz`* es un código de zona horaria de tres o cuatro caracteres como &quot;GMT&quot; o &quot;PST&quot;. Cuenta el horario de verano en el código de zona horaria. Por ejemplo, &quot;PST&quot; para la hora estándar del Pacífico frente a &quot;PDT&quot; para el horario de verano del Pacífico).

*`offset`* es un desplazamiento de zona horaria en horas o `hours:minutes`, en relación con GMT. Por ejemplo, &quot;PDT&quot; equivale a &quot;GMT -7&quot;.

Todos los elementos de los valores de fecha y hora con formato de cadena deben estar presentes. Si el valor de fecha y hora no tiene el formato correcto, se omitirá y se utilizará en su lugar la hora de modificación del archivo `*`catalog`*.ini`.

## Predeterminado {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` si el campo está vacío o no está presente.

## Véase también {#section-c42a427aa4794c548408dc4de028d578}

[atributo::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [atributo::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [atributo::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
