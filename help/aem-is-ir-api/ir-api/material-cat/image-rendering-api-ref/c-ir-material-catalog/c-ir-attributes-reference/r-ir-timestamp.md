---
title: TimeStamp
description: Marca de tiempo de modificación predeterminada. Proporciona un valor predeterminado para TimeStamp del catálogo y TimeStamp de la viñeta. Si no se especifica, el servidor utiliza la fecha y hora de modificación de este archivo catalog.ini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Marca de tiempo de modificación predeterminada. Proporciona un valor predeterminado para `catalog::TimeStamp` y `vignette::TimeStamp`. Si no se especifica, el servidor utiliza la fecha y hora de modificación de este archivo catalog.ini.

## Propiedades {#section-910e2562b41c47b78ee6216deeabbbd5}

Valor de fecha y hora en formato Java™. Puede ser el número entero de milisegundos desde la medianoche del 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* está en el intervalo de 0 a 23.

*[!DNL zzz]* es un código de zona horaria de tres o cuatro caracteres como &quot;GMT&quot; o &quot;PST&quot;. El horario de verano se debe contabilizar en el código de zona horaria (por ejemplo, &quot;PST&quot; para el horario estándar del Pacífico frente a &quot;PDT&quot; para el horario de verano del Pacífico).

*[!DNL offset]* es un desplazamiento de zona horaria en horas u horas:minutos, en relación con la hora GMT. Por ejemplo, &quot;PDT&quot; equivale a &quot;GMT -7&quot;.

Todos los elementos de los valores de fecha y hora con formato de cadena deben estar presentes. Si el valor de fecha y hora no tiene el formato correcto, se omitirá y se utilizará en su lugar la hora de modificación del archivo [!DNL *[!DNL catalog]*.ini].

## Predeterminado {#section-65fb29a9ea2044df8cb9fe295eb14872}

Si está vacío o no está definido, el servidor utiliza la hora de modificación del archivo de este archivo de [!DNL *[!DNL catalog]*.ini].

## Véase también {#section-764188f9b1734ad1a6270f5fecd28532}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [viñeta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [atributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
