---
description: Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el servicio de imágenes.
seo-description: Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el servicio de imágenes.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables emitidas por el servicio de imágenes.

El servidor utiliza el valor más reciente `catalog::TimeStamp` de todos los catálogos o registros de catálogo implicados en una respuesta como el valor del encabezado Última modificación.

Solo debe habilitarse si se utiliza una red de almacenamiento en caché distribuida u otro sistema de almacenamiento en caché que no admita encabezados de etiqueta.

>[!NOTE]
>
>Se debe tener cuidado al usar encabezados de última modificación en un entorno de equilibrio de carga que incluya varios hosts de servicio de imágenes. El almacenamiento en caché del cliente puede fallar y aumentar la carga del servidor si, por alguna razón, los servidores tienen diferentes marcas de hora para las mismas entradas de catálogo. Esta situación puede darse de la siguiente manera:
>
>* Ni `catalog::TimeStamp` ni `attribute::TimeStamp`, de modo que el tiempo de modificación del [!DNL catalog.ini] archivo se utilice como valor predeterminado para `catalog::TimeStamp`.
   >
   >
* En lugar de compartir los archivos de catálogo de imágenes mediante un montaje en red, cada servidor tiene su propia instancia de los archivos de catálogo en un sistema de archivos local.
>* Dos o más instancias del mismo [!DNL catalog.ini] archivo tienen fechas de modificación de archivo diferentes, posiblemente debido a una copia incorrecta de los archivos.
>



## Propiedades {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Indicador. 0 para deshabilitar, 1 para habilitar los encabezados HTTP de última modificación.

## Predeterminado {#section-4eb47aadab8b41609bef296a4115f9f4}

Se hereda de `default::UseLastModified` si no está definida o si está vacía.

## Véase también {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catálogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
