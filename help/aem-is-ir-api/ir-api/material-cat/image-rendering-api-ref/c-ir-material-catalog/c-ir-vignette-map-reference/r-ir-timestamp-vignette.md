---
description: Marca de tiempo de modificación. Especifica la fecha y la hora de la última modificación de esta viñeta.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Marca de tiempo de modificación. Especifica la fecha y la hora de la última modificación de esta viñeta.

If `attribute::UseLastModified` está configurado, el más reciente `vignette::TimeStamp` y `catalog::TimeStamp`de la viñeta y todos los materiales involucrados en la solicitud se devuelven en la respuesta HTTP como encabezado modificado por última vez.

>[!NOTE]
>
>Con este fin, nunca se utiliza la hora real del archivo de la viñeta.

`catalog::TimeStamp` también se utiliza para la validación de caché basada en catálogo (consulte [atributo::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Propiedades {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valor de fecha y hora en formato Java. Puede ser el número entero de milisegundos desde la medianoche, el 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* está en el rango de 0 a 23.
* *[!DNL zzz]* es un código de zona horaria de 3 o 4 caracteres como &quot;GMT&quot; o &quot;PST&quot;. El horario de verano debe contabilizarse en el código de zona horaria (por ejemplo, &quot;PST&quot; para la hora estándar del Pacífico, en comparación con &quot;PDT&quot; para la hora de verano del Pacífico).
* *[!DNL offset]* es un desplazamiento de zona horaria en horas u horas:minutos, en relación con GMT. Por ejemplo, &quot;PDT&quot; es equivalente a &quot;GMT -7&quot;.

Deben estar presentes todos los elementos de los valores de fecha y hora con formato de cadena. Si el valor de fecha y hora no tiene el formato correcto, se ignora y la hora de modificación del [!DNL *[!DNL catalog]*.ini] se utiliza en su lugar.

## Predeterminado {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` es que el campo está vacío o no está presente.

## Véase también {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[atributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
