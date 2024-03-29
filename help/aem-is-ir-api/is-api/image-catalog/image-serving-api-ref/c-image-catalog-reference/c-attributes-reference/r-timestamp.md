---
title: TimeStamp
description: Marca de tiempo de modificación de imagen predeterminada. Proporciona un valor predeterminado para la marca de tiempo del catálogo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Marca de tiempo de modificación de imagen predeterminada. Proporciona un valor predeterminado para catalog::TimeStamp.

Si no se especifica, el servidor utiliza la fecha y hora de modificación de este [!DNL *`catalog`*.ini] archivo.

## Propiedades {#section-647066e62ce44a84b627fdd0b2f7cfec}

Valor de fecha y hora. Puede ser el número entero de milisegundos desde la medianoche del 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

El valor de fecha y hora *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

El valor de fecha y hora *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

El valor de tiempo *`hh`* está entre 0 y 23.

El valor de tiempo *`zzz`* es un código de zona horaria de tres o cuatro caracteres como `GMT` o `PST`. El horario de verano debe contabilizarse en el código de zona horaria (por ejemplo, `PST` para la hora estándar del Pacífico, frente a `PDT` horario de verano del Pacífico).

El valor de tiempo *`offset`* es un desplazamiento de zona horaria en horas u horas:minutos, en relación con GMT. Por ejemplo, `PDT` es equivalente a `GMT -7`.

Todos los elementos de los valores de fecha y hora con formato de cadena deben estar presentes. Si el valor de fecha y hora no tiene el formato correcto, se ignora y se modifica la hora del [!DNL *`catalog`*.ini] se utiliza el archivo en su lugar.

## Predeterminado {#section-ac465313c97943ed97d41ea852329177}

Si está vacío o no está definido, el servidor utiliza el tiempo de modificación de archivos de este `*`catalogar`*.ini` archivo.

## Véase también {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
