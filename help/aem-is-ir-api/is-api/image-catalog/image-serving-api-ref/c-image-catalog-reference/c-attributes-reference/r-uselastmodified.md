---
description: Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables en caché emitidas por el servicio de imágenes.
seo-description: Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables en caché emitidas por el servicio de imágenes.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 2%

---


# UseLastModified{#uselastmodified}

Habilite los encabezados de respuesta modificados por última vez. Activa o desactiva la inclusión del encabezado Última modificación en las respuestas HTTP almacenables en caché emitidas por el servicio de imágenes.

El servidor utiliza el valor `catalog::TimeStamp` más reciente de todos los catálogos o registros de catálogo implicados en una respuesta como valor del encabezado Última modificación.

Solo debe habilitarse si se utiliza una red de almacenamiento en caché distribuida u otro sistema de almacenamiento en caché que no admita encabezados de etiqueta.

>[!NOTE]
>
>Se debe tener cuidado al usar encabezados de Última modificación en un entorno de carga equilibrada que incluya varios hosts de servicio de imágenes. El almacenamiento en caché del cliente puede ser rechazado y la carga del servidor aumenta si, por alguna razón, los servidores tienen diferentes marcas de tiempo para las mismas entradas de catálogo. Esta situación puede ocurrir de la siguiente manera:
>
>* Ni `catalog::TimeStamp` ni `attribute::TimeStamp`, de modo que el tiempo de modificación del archivo [!DNL catalog.ini] se utilice como valor predeterminado para `catalog::TimeStamp`.
   >
   >
* En lugar de compartir los archivos de catálogo de imágenes a través de un montaje de red, cada servidor tiene su propia instancia de los archivos de catálogo en un sistema de archivos local.
>* Dos o más instancias del mismo archivo [!DNL catalog.ini] tienen fechas de modificación de archivo diferentes, posiblemente debido a la copia incorrecta de los archivos.

>



## Propiedades {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Indicador. 0 para deshabilitar, 1 para habilitar los encabezados HTTP de última modificación.

## Predeterminado {#section-4eb47aadab8b41609bef296a4115f9f4}

Se hereda de `default::UseLastModified` si no está definido o si está vacío.

## Véase también {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catálogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
