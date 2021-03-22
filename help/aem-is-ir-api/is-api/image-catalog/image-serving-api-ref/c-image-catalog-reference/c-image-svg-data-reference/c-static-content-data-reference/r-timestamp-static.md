---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
uuid: fd60e5db-9219-41a8-947f-0d497b39e727
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# TimeStamp{#timestamp}

Si `attribute::UseLastModified` está establecido, el valor `catalog::TimeStamp` se devuelve en la respuesta HTTP como un encabezado HTTP de última modificación. El encabezado Última modificación siempre se devuelve para el contenido estático, aunque no esté establecido `attribute::UseLastModified`.

Para la imagen y el contenido SVG, `catalog::TimeStamp` también se utiliza para la validación de caché basada en catálogo (consulte ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`).

## Propiedades {#section-2298a384b5cb43929542655c5a49beb2}

Valor de fecha y hora en formato Java. Puede ser el número entero de milisegundos desde la medianoche, el 1 de enero de 1970 UTC/GMT, o un valor de cadena de fecha y hora con uno de los siguientes formatos:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* está en el rango 0 - 23.

*`zzz`* es un código de zona horaria de tres o cuatro caracteres, como &quot;GMT&quot; o &quot;PST&quot;. Cuenta para el horario de verano en el código de zona horaria. Por ejemplo, &quot;PST&quot; para la hora estándar del Pacífico, frente a &quot;PDT&quot; para la hora de verano del Pacífico).

*`offset`* es una compensación de zona horaria en horas o  `hours:minutes`, en relación con GMT. Por ejemplo, &quot;PDT&quot; es equivalente a &quot;GMT -7&quot;.

Deben estar presentes todos los elementos de los valores de fecha y hora con formato de cadena. Si el valor de fecha y hora no tiene el formato correcto, se ignora y se utiliza la hora de modificación del archivo `*`catálogo`*.ini` en su lugar.

## Predeterminado {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` si el campo está vacío o no está presente.

## Véase también {#section-c42a427aa4794c548408dc4de028d578}

[atributo::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [atributo::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [atributo::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
