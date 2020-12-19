---
description: Marca de hora de modificación de imagen predeterminada. Proporciona un valor predeterminado para el TimeStamp del catálogo.
seo-description: Marca de hora de modificación de imagen predeterminada. Proporciona un valor predeterminado para el TimeStamp del catálogo.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 2%

---


# TimeStamp{#timestamp}

Marca de hora de modificación de imagen predeterminada. Proporciona un valor predeterminado para el catálogo::TimeStamp.

Si no se especifica, el servidor usará la fecha y hora de modificación de este archivo [!DNL *`catalog`*.ini].

## Propiedades {#section-647066e62ce44a84b627fdd0b2f7cfec}

Valor de fecha y hora. Puede ser el número entero de milisegundos desde la medianoche, el 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*::  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*::  *`ss`* GMT  *`offset`*

*`hh`* está en el rango de 0 a 23.

*`zzz`* es un código de zona horaria de 3 o 4 caracteres como  `GMT` o  `PST`. El horario de verano debe contabilizarse en el código de zona horaria (p. ej. `PST` para la hora estándar del Pacífico, vs `PDT` para la hora de verano del Pacífico).

*`offset`* es un huso horario compensado en horas u horas:minutos, en relación con GMT. Por ejemplo, `PDT` es equivalente a `GMT -7`.

Deben estar presentes todos los elementos de los valores de fecha y hora con formato de cadena. Si el valor de fecha y hora no tiene el formato correcto, se ignora y se utiliza la hora de modificación del archivo [!DNL *`catalog`*.ini] en su lugar.

## Predeterminado {#section-ac465313c97943ed97d41ea852329177}

Si está vacío o no está definido, el servidor utiliza la hora de modificación de archivos de este archivo ` *`catálogo`*.ini`.

## Véase también {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catálogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [atributo::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [atributo::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
