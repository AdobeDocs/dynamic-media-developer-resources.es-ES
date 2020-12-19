---
description: Los datos de imagen intermedios generados por solicitudes de procesamiento de imágenes y servicio de imágenes anidadas/incrustadas se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propio en la caché de datos de respuesta.
seo-description: Los datos de imagen intermedios generados por solicitudes de procesamiento de imágenes y servicio de imágenes anidadas/incrustadas se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propio en la caché de datos de respuesta.
seo-title: Cachés de datos auxiliares
solution: Experience Manager
title: Cachés de datos auxiliares
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Cachés de datos auxiliares{#auxiliary-data-caches}

Los datos de imagen intermedios generados por solicitudes de procesamiento de imágenes y servicio de imágenes anidadas/incrustadas se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propio en la caché de datos de respuesta.

Las imágenes obtenidas de servidores HTTP externos también se almacenan en la caché de datos de respuesta. Estas imágenes se validan automáticamente con la utilidad validate antes de que se genere la entrada de caché.

Platform Server recopila datos del catálogo de imágenes para un acceso eficaz. Estos datos se almacenan en `CS::CatalogCacheFolder`.
