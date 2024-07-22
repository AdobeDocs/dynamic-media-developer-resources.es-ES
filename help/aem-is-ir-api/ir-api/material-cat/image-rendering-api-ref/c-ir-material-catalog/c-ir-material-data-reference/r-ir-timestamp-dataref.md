---
title: TimeStamp
description: Marca de tiempo de modificación de archivo. Especifica la fecha y la hora en que se modificaron por última vez los archivos de datos o imagen adjuntos a este registro de catálogo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Marca de tiempo de modificación de archivo. Especifica la fecha y la hora en que se modificaron por última vez los archivos de datos o imagen adjuntos a este registro de catálogo.

Si se establece `attribute::UseLastModified`, el valor más reciente de `catalog::TimeStamp` y `vignette::TimeStamp` de todos los materiales y la viñeta involucrados en la solicitud se devuelven en la respuesta HTTP como un encabezado modificado por última vez.

>[!NOTE]
>
>Las horas reales de archivo de los archivos de datos o de imagen adjuntos a este registro de catálogo nunca se utilizan para este fin.

`catalog::TimeStamp` también se usa para la validación de caché basada en catálogo (consulte [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Propiedades {#section-42f09e375e72492b87a3a486da7df808}

Valor de fecha y hora en formato Java™. Puede ser el número entero de milisegundos desde la medianoche del 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* está en el rango de 0 a 23.
* *[!DNL zzz]* es un código de zona horaria de tres o cuatro caracteres como &quot;GMT&quot; o &quot;PST&quot;. El horario de verano debe contabilizarse en el código de zona horaria. Por ejemplo, &quot;PST&quot; para la hora estándar del Pacífico frente a &quot;PDT&quot; para el horario de verano del Pacífico.
* *[!DNL offset]* es un desplazamiento de zona horaria en horas u horas:minutos, en relación con la hora GMT. Por ejemplo, &quot;PDT&quot; equivale a &quot;GMT -7&quot;.

Todos los elementos de los valores de fecha y hora con formato de cadena deben estar presentes. Si el valor de fecha y hora no tiene el formato correcto, se omitirá y se utilizará en su lugar la hora de modificación del archivo *catalog*.ini.

## Predeterminado {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` es el campo que está vacío o no está presente.

## Véase también {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [viñeta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
