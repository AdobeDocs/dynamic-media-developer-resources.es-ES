---
description: Habilitar encabezados de respuesta de última modificación. Habilita o deshabilita la inclusión del encabezado Última modificación en las respuestas HTTP almacenables en caché emitidas por el servicio de imágenes.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Habilitar encabezados de respuesta de última modificación. Habilita o deshabilita la inclusión del encabezado Última modificación en las respuestas HTTP almacenables en caché emitidas por el servicio de imágenes.

El servidor utiliza el más reciente `catalog::TimeStamp` valor de todos los catálogos/registros de catálogo implicados en una respuesta como valor del encabezado Última modificación.

Solo debe habilitarse si se utiliza una red de almacenamiento en caché distribuida u otro sistema de almacenamiento en caché que no admita encabezados de etiqueta.

>[!NOTE]
>
>Se debe tener cuidado al utilizar encabezados Last-Modified en un entorno de carga equilibrada que implica varios hosts del servicio de imágenes. El almacenamiento en caché de clientes puede no funcionar y la carga del servidor puede aumentar si, por alguna razón, los servidores tienen marcas de tiempo diferentes para las mismas entradas de catálogo. Esta situación puede ocurrir de la siguiente manera:
>
>* Ninguna `catalog::TimeStamp` ni `attribute::TimeStamp`, para que la hora de modificación del [!DNL catalog.ini] se utiliza como valor predeterminado para `catalog::TimeStamp`.
>
>* En lugar de compartir los archivos del catálogo de imágenes mediante un montaje en red, cada servidor tiene su propia instancia de los archivos de catálogo en un sistema de archivos local.
>* Dos o más instancias del mismo [!DNL catalog.ini] Los archivos tienen fechas de modificación diferentes, posiblemente a causa de una copia incorrecta de los archivos.
>


## Propiedades {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Indicador. 0 para deshabilitar, 1 para habilitar los encabezados HTTP de última modificación.

## Predeterminado {#section-4eb47aadab8b41609bef296a4115f9f4}

Heredado de `default::UseLastModified` si no se define o si está vacío.

## Véase también {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
