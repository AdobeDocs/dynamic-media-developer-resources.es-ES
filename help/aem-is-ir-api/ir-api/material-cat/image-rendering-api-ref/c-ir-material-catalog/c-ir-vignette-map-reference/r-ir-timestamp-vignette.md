---
description: Marca de hora de modificación. Especifica la fecha y la hora de la última modificación de esta viñeta.
seo-description: Marca de hora de modificación. Especifica la fecha y la hora de la última modificación de esta viñeta.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: d2649e86-8a6f-4f63-ab6a-8b2d8c03f8c0
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# TimeStamp{#timestamp}

Marca de hora de modificación. Especifica la fecha y la hora de la última modificación de esta viñeta.

Si `attribute::UseLastModified` está establecido, los valores más recientes `vignette::TimeStamp` y `catalog::TimeStamp`de la viñeta y todos los materiales involucrados en la solicitud se devuelven en la respuesta HTTP como encabezado modificado por última vez.

>[!NOTE]
>
>El tiempo real de archivo del archivo de viñeta nunca se utiliza con este fin.

`catalog::TimeStamp` también se utiliza para la validación de caché basada en catálogo (consulte  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Propiedades {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valor de fecha y hora en formato Java. Puede ser el número entero de milisegundos desde la medianoche, el 1 de enero de 1970 UTC/GMT o un valor de cadena de fecha y hora con uno de los siguientes formatos:

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*::  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:: *[!DNL ss]*GMT  *[!DNL offset]*

* *[!DNL hh]* está en el rango de 0 a 23.
* *[!DNL zzz]* es un código de zona horaria de 3 o 4 caracteres como &quot;GMT&quot; o &quot;PST&quot;. El horario de verano se debe contabilizar en el código de zona horaria (por ejemplo, &#39;PST&#39; para la hora estándar del Pacífico en comparación con &#39;PDT&#39; para la hora de verano del Pacífico).
* *[!DNL offset]* es un huso horario compensado en horas u horas:minutos, en relación con GMT. Por ejemplo, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Deben estar presentes todos los elementos de los valores de fecha y hora con formato de cadena. Si el valor de fecha y hora no tiene el formato correcto, se ignora y se utiliza la hora de modificación del archivo [!DNL *[!DNL catalog]*.ini] en su lugar.

## Predeterminado {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` es que el campo está vacío o no está presente.

## Véase también {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[atributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319),  [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
