---
title: UseLastModified
description: Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el procesamiento de imágenes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 2%

---

# UseLastModified{#uselastmodified}

Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el procesamiento de imágenes.

El servidor utiliza el `vignette::TimeStamp` y `catalog::TimeStamp` valor de todos los catálogos de viñetas y materiales/registros de catálogo implicados en una respuesta como el valor del encabezado Última modificación.

Solo debe habilitarse si se utiliza una red de almacenamiento en caché distribuida, como Akamai, que no admita encabezados de etiqueta.

>[!NOTE]
>
>Se debe tener cuidado al usar encabezados de Última modificación en un entorno de carga equilibrada que incluya varios hosts de servicio/renderización de imágenes. El almacenamiento en caché del cliente puede ser rechazado y la carga del servidor aumenta si, por alguna razón, los servidores tienen diferentes marcas de tiempo para las mismas entradas de catálogo. Esta situación puede ocurrir de la siguiente manera:

* `catalog::TimeStamp`, `vignette::TimeStamp`o `attribute::TimeStamp` no está definida, de modo que la hora de modificación de la variable [!DNL catalog.ini] se utiliza como valor predeterminado para `catalog::TimeStamp`.

* En lugar de compartir los archivos de catálogo de material a través de un montaje de red, cada servidor tiene su propia instancia de los archivos de catálogo en un sistema de archivos local.
* Dos o más instancias del mismo [!DNL catalog.ini] tiene diferentes fechas de modificación del archivo, posiblemente debido a una copia incorrecta de los archivos.

## Propiedades {#section-453952244193452caccfaf7f601007c1}

Indicador. 0 para deshabilitar, 1 para habilitar los encabezados HTTP de última modificación.

## Predeterminado {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Heredado de `default::UseLastModified` si no está definida o si está vacío.

## Véase también {#section-1536715169da48b0aecc4ab7326c86db}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [viñeta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
