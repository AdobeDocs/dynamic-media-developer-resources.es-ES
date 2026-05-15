---
description: Habilitar encabezados de respuesta de última modificación. Habilita o deshabilita la inclusión del encabezado Última modificación en las respuestas HTTP almacenables en caché emitidas por el servicio de imágenes.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
TQID: 'https://experienceleague.adobe.com/jmwz9jThBnFtTZBRoI0kbKwoxf1MU7rn1CpKrSU4f04'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Habilitar encabezados de respuesta de última modificación. Habilita o deshabilita la inclusión del encabezado Última modificación en las respuestas HTTP almacenables en caché emitidas por el servicio de imágenes.

El servidor utiliza el valor `catalog::TimeStamp` más reciente de todos los catálogos o registros de catálogo involucrados en una respuesta como el valor del encabezado Última modificación.

Solo debe habilitarse si se utiliza una red de almacenamiento en caché distribuida u otro sistema de almacenamiento en caché que no admita encabezados de etiqueta.

>[!NOTE]
>
>Se debe tener cuidado al utilizar encabezados Last-Modified en un entorno de carga equilibrada que implica varios hosts del servicio de imágenes. El almacenamiento en caché de clientes puede no funcionar y la carga del servidor puede aumentar si, por alguna razón, los servidores tienen marcas de tiempo diferentes para las mismas entradas de catálogo. Esta situación puede ocurrir de la siguiente manera:
>
>* Ni `catalog::TimeStamp` ni `attribute::TimeStamp`, de modo que la hora de modificación del archivo [!DNL catalog.ini] se usa como predeterminada para `catalog::TimeStamp`.
>
>* En lugar de compartir los archivos de catálogo de imágenes mediante un montaje en red, cada servidor tiene su propia instancia de los archivos de catálogo en un sistema de archivos local.
>* Dos o más instancias del mismo archivo de [!DNL catalog.ini] tienen fechas de modificación de archivo diferentes, posiblemente a causa de una copia incorrecta de los archivos.
>

## Propiedades {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Indicador. 0 para deshabilitar, 1 para habilitar los encabezados HTTP de última modificación.

## Predeterminado {#section-4eb47aadab8b41609bef296a4115f9f4}

Se hereda de `default::UseLastModified` si no se ha definido o está vacío.

## Véase también {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
