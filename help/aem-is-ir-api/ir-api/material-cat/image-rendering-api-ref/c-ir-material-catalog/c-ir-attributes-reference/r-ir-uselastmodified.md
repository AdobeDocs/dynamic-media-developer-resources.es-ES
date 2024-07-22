---
title: UseLastModified
description: Habilitar encabezados de respuesta de última modificación. Habilita o deshabilita la inclusión del encabezado Última modificación en las respuestas HTTP almacenables en caché emitidas por el procesamiento de imágenes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Habilitar encabezados de respuesta de última modificación. Habilita o deshabilita la inclusión del encabezado Última modificación en las respuestas HTTP almacenables en caché emitidas por el procesamiento de imágenes.

El servidor usa el valor `vignette::TimeStamp` y `catalog::TimeStamp` más reciente de todos los registros de catálogo o catálogos de material y viñetas implicados en una respuesta como valor del encabezado Última modificación.

Solo debe habilitarse si se utiliza una red de almacenamiento en caché distribuida, como Akamai, que no admite encabezados de etiqueta.

>[!NOTE]
>
>Se debe tener cuidado al utilizar encabezados Last-Modified en un entorno de equilibrio de carga que implica varios hosts de servicio/renderización de imágenes. El almacenamiento en caché de clientes puede no funcionar y la carga del servidor puede aumentar si, por alguna razón, los servidores tienen marcas de tiempo diferentes para las mismas entradas de catálogo. Esta situación puede ocurrir de la siguiente manera:

* `catalog::TimeStamp`, `vignette::TimeStamp` o `attribute::TimeStamp` no están definidos, de modo que la hora de modificación del archivo [!DNL catalog.ini] se usa como predeterminada para `catalog::TimeStamp`.

* En lugar de compartir los archivos del catálogo de materiales mediante un montaje en red, cada servidor tiene su propia instancia de los archivos de catálogo en un sistema de archivos local.
* Dos o más instancias del mismo archivo de [!DNL catalog.ini] tienen fechas de modificación de archivo diferentes, posiblemente a causa de una copia incorrecta de los archivos.

## Propiedades {#section-453952244193452caccfaf7f601007c1}

Indicador. 0 para deshabilitar, 1 para habilitar los encabezados HTTP de última modificación.

## Predeterminado {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Se hereda de `default::UseLastModified` si no se ha definido o está vacío.

## Véase también {#section-1536715169da48b0aecc4ab7326c86db}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [viñeta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
