---
description: Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el procesamiento de imágenes.
seo-description: Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el procesamiento de imágenes.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el procesamiento de imágenes.

El servidor utiliza el valor más reciente `vignette::TimeStamp` y `catalog::TimeStamp` el valor de todos los catálogos de viñetas y materiales o registros de catálogo que intervienen en una respuesta como el valor del encabezado Última modificación.

Solo debe habilitarse si se utiliza una red de almacenamiento en caché distribuida, como Akamai, que no admite encabezados de etiqueta.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Se debe tener cuidado al utilizar encabezados de última modificación en un entorno de equilibrio de carga que incluya varios hosts de servicio o procesamiento de imágenes. El almacenamiento en caché del cliente puede fallar y aumentar la carga del servidor si, por alguna razón, los servidores tienen diferentes marcas de hora para las mismas entradas de catálogo. Esta situación puede darse de la siguiente manera:

* Ni `catalog::TimeStamp`, `vignette::TimeStamp`ni `attribute::TimeStamp` se define, de modo que la hora de modificación del [!DNL catalog.ini] archivo se utilice como valor predeterminado para `catalog::TimeStamp`.

* En lugar de compartir los archivos de catálogo de material mediante un montaje en red, cada servidor tiene su propia instancia de los archivos de catálogo en un sistema de archivos local.
* Dos o más instancias del mismo [!DNL catalog.ini] archivo tienen fechas de modificación de archivo diferentes, posiblemente debido a una copia incorrecta de los archivos.

## Propiedades {#section-453952244193452caccfaf7f601007c1}

Indicador. 0 para deshabilitar, 1 para habilitar los encabezados HTTP de última modificación.

## Predeterminado {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Se hereda de `default::UseLastModified` si no está definida o si está vacía.

## Véase también {#section-1536715169da48b0aecc4ab7326c86db}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [viñeta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
