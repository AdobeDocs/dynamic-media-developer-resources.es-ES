---
title: TimeStamp
description: Marca de tiempo de modificación. Especifica la fecha y la hora de la última modificación de esta viñeta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Marca de tiempo de modificación. Especifica la fecha y la hora de la última modificación de esta viñeta.

Si se establece `attribute::UseLastModified`, el valor `vignette::TimeStamp` y `catalog::TimeStamp`más reciente de la viñeta y todos los materiales involucrados en la solicitud se devuelven en la respuesta HTTP como un encabezado modificado por última vez.

>[!NOTE]
>
>La hora real del archivo de viñeta nunca se utiliza para este fin.

`catalog::TimeStamp` también se usa para la validación de caché basada en el catálogo. Consulte [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Propiedades {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valor de fecha y hora en formato Java™. Puede ser el número entero de milisegundos desde la medianoche del 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* está en el rango de 0 a 23.
* *[!DNL zzz]* es un código de zona horaria de tres o cuatro caracteres como &quot;GMT&quot; o &quot;PST&quot;. El horario de verano se debe contabilizar en el código de zona horaria (por ejemplo, &quot;PST&quot; para el horario estándar del Pacífico frente a &quot;PDT&quot; para el horario de verano del Pacífico).
* *[!DNL offset]* es un desplazamiento de zona horaria en horas u horas:minutes, en relación con la zona GMT. Por ejemplo, &quot;PDT&quot; equivale a &quot;GMT -7&quot;.

Todos los elementos de los valores de fecha y hora con formato de cadena deben estar presentes. Si el valor de fecha y hora no tiene el formato correcto, se omitirá y se utilizará en su lugar la hora de modificación del archivo [!DNL *[!DNL catalog]*.ini].

## Predeterminado {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` es el campo que está vacío o no está presente.

## Véase también {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[atributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
