---
description: Marca de hora de modificación predeterminada. Proporciona un valor predeterminado para el registro TimeStamp y la viñeta TimeStamp. Si no se especifica, el servidor utilizará la fecha y hora de modificación de este archivo catalog.ini.
seo-description: Marca de hora de modificación predeterminada. Proporciona un valor predeterminado para el registro TimeStamp y la viñeta TimeStamp. Si no se especifica, el servidor utilizará la fecha y hora de modificación de este archivo catalog.ini.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ceb600-1ed9-46a1-ae07-889d601ac0f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

Marca de hora de modificación predeterminada. Proporciona un valor predeterminado para catálogo::TimeStamp y vignette::TimeStamp. Si no se especifica, el servidor utilizará la fecha y hora de modificación de este archivo catalog.ini.

## Propiedades {#section-910e2562b41c47b78ee6216deeabbbd5}

Valor de fecha y hora en formato Java. Puede ser el número entero de milisegundos desde la medianoche, el 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* está en el rango de 0 a 23.

*[!DNL zzz]* es un código de zona horaria de 3 o 4 caracteres como &quot;GMT&quot; o &quot;PST&quot;. El horario de verano se debe contabilizar en el código de zona horaria (por ejemplo, &#39;PST&#39; para la hora estándar del Pacífico en comparación con &#39;PDT&#39; para la hora de verano del Pacífico).

*[!DNL offset]* es un huso horario compensado en horas u horas:minutos, en relación con GMT. Por ejemplo, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Deben estar presentes todos los elementos de los valores de fecha y hora con formato de cadena. Si el valor de fecha y hora no tiene el formato correcto, se ignora y se utiliza la hora de modificación del archivo [!DNL *[!DNL catalog]*.ini].

## Predeterminado {#section-65fb29a9ea2044df8cb9fe295eb14872}

Si está vacío o no está definido, el servidor utilizará el tiempo de modificación de archivo de este archivo [!DNL *[!DNL catalog]*.ini].

## Véase también {#section-764188f9b1734ad1a6270f5fecd28532}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [viñeta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [atributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
