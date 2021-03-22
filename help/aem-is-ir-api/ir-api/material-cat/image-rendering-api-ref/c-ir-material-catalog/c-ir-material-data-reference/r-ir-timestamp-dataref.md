---
description: Marca de tiempo de modificación de archivo. Especifica la fecha/hora en la que se modificaron por última vez los archivos de imagen o datos adjuntos a este registro de catálogo.
seo-description: Marca de tiempo de modificación de archivo. Especifica la fecha/hora en la que se modificaron por última vez los archivos de imagen o datos adjuntos a este registro de catálogo.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
uuid: 77ce8bee-7b55-4ff8-8dfb-ebd3ce9c7a8a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 1%

---


# TimeStamp{#timestamp}

Marca de tiempo de modificación de archivo. Especifica la fecha/hora en la que se modificaron por última vez los archivos de imagen o datos adjuntos a este registro de catálogo.

Si `attribute::UseLastModified` está establecido, los valores más recientes de `catalog::TimeStamp` y `vignette::TimeStamp` de todos los materiales y la viñeta involucrada en la solicitud se devuelven en la respuesta HTTP como un encabezado modificado por última vez.

>[!NOTE]
>
>Con este fin, nunca se utilizan los tiempos reales de archivo de la imagen o los archivos de datos adjuntos a este registro de catálogo.

`catalog::TimeStamp` también se utiliza para la validación de caché basada en catálogo (consulte  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Propiedades {#section-42f09e375e72492b87a3a486da7df808}

Valor de fecha y hora en formato Java. Puede ser el número entero de milisegundos desde la medianoche, el 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

* *[!DNL hh]* está en el rango de 0 a 23.
* *[!DNL zzz]* es un código de zona horaria de 3 o 4 caracteres como &quot;GMT&quot; o &quot;PST&quot;. El horario de verano debe contabilizarse en el código de zona horaria (por ejemplo, &quot;PST&quot; para la hora estándar del Pacífico, en comparación con &quot;PDT&quot; para la hora de verano del Pacífico).
* *[!DNL offset]* es un desplazamiento de zona horaria en horas u horas:minutos, en relación con GMT. Por ejemplo, &quot;PDT&quot; es equivalente a &quot;GMT -7&quot;.

Deben estar presentes todos los elementos de los valores de fecha y hora con formato de cadena. Si el valor de fecha y hora no tiene el formato correcto, se ignora y en su lugar se utiliza la hora de modificación del archivo *catalog*.ini.

## Predeterminado {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` es que el campo está vacío o no está presente.

## Véase también {#section-876f1d1b50dc4501b605820015a29451}

[atributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [atributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4),  [viñeta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
