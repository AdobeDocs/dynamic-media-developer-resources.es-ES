---
description: Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el procesamiento de imágenes.
seo-description: Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el procesamiento de imágenes.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el procesamiento de imágenes.

El servidor utiliza los valores más recientes `vignette::TimeStamp` y `catalog::TimeStamp` de todos los catálogos de viñetas y materiales/registros de catálogo implicados en una respuesta como el valor del encabezado Última modificación.

Solo debe habilitarse si se utiliza una red de almacenamiento en caché distribuida, como Akamai, que no admita encabezados de etiqueta.

>[!NOTE]
>
>Se debe tener cuidado al usar encabezados de Última modificación en un entorno de carga equilibrada que incluya varios hosts de servicio/renderización de imágenes. El almacenamiento en caché del cliente puede ser rechazado y la carga del servidor aumenta si, por alguna razón, los servidores tienen diferentes marcas de tiempo para las mismas entradas de catálogo. Esta situación puede ocurrir de la siguiente manera:

* Ni `catalog::TimeStamp`, `vignette::TimeStamp` ni `attribute::TimeStamp` están definidos, de modo que el tiempo de modificación del archivo [!DNL catalog.ini] se utilice como valor predeterminado para `catalog::TimeStamp`.

* En lugar de compartir los archivos de catálogo de material a través de un montaje de red, cada servidor tiene su propia instancia de los archivos de catálogo en un sistema de archivos local.
* Dos o más instancias del mismo archivo [!DNL catalog.ini] tienen fechas de modificación de archivo diferentes, posiblemente debido a la copia incorrecta de los archivos.

## Propiedades {#section-453952244193452caccfaf7f601007c1}

Indicador. 0 para deshabilitar, 1 para habilitar los encabezados HTTP de última modificación.

## Predeterminado {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Se hereda de `default::UseLastModified` si no está definido o si está vacío.

## Véase también {#section-1536715169da48b0aecc4ab7326c86db}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [viñeta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
