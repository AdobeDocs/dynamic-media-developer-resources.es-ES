---
description: Marca de tiempo de modificación de archivo. Especifica la fecha/hora en la que se modificaron por última vez los archivos de imagen o datos adjuntos a este registro de catálogo.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Marca de tiempo de modificación de archivo. Especifica la fecha/hora en la que se modificaron por última vez los archivos de imagen o datos adjuntos a este registro de catálogo.

If `attribute::UseLastModified` está configurado, el más reciente de los `catalog::TimeStamp` y `vignette::TimeStamp` los valores de todos los materiales y la viñeta implicados en la solicitud se devuelven en la respuesta HTTP como encabezado modificado por última vez.

>[!NOTE]
>
>Con este fin, nunca se utilizan los tiempos reales de archivo de la imagen o los archivos de datos adjuntos a este registro de catálogo.

`catalog::TimeStamp` también se utiliza para la validación de caché basada en catálogo (consulte [atributo::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Propiedades {#section-42f09e375e72492b87a3a486da7df808}

Valor de fecha y hora en formato Java. Puede ser el número entero de milisegundos desde la medianoche, el 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* está en el rango de 0 a 23.
* *[!DNL zzz]* es un código de zona horaria de 3 o 4 caracteres como &quot;GMT&quot; o &quot;PST&quot;. El horario de verano debe contabilizarse en el código de zona horaria (por ejemplo, &quot;PST&quot; para la hora estándar del Pacífico, en comparación con &quot;PDT&quot; para la hora de verano del Pacífico).
* *[!DNL offset]* es un desplazamiento de zona horaria en horas u horas:minutos, en relación con GMT. Por ejemplo, &quot;PDT&quot; es equivalente a &quot;GMT -7&quot;.

Deben estar presentes todos los elementos de los valores de fecha y hora con formato de cadena. Si el valor de fecha y hora no tiene el formato correcto, se ignora y la hora de modificación del *catálogo* En su lugar, se utiliza el archivo .ini.

## Predeterminado {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` es que el campo está vacío o no está presente.

## Véase también {#section-876f1d1b50dc4501b605820015a29451}

[atributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [atributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [viñeta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
