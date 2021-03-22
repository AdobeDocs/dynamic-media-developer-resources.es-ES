---
description: Los datos de imagen intermedios producidos por solicitudes de servicio de imágenes anidadas/incrustadas y renderización de imágenes se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propietario en la caché de datos de respuesta.
seo-description: Los datos de imagen intermedios producidos por solicitudes de servicio de imágenes anidadas/incrustadas y renderización de imágenes se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propietario en la caché de datos de respuesta.
seo-title: Cachés de datos auxiliares
solution: Experience Manager
title: Cachés de datos auxiliares
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Cachés de datos auxiliares{#auxiliary-data-caches}

Los datos de imagen intermedios producidos por solicitudes de servicio de imágenes anidadas/incrustadas y renderización de imágenes se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propietario en la caché de datos de respuesta.

Las imágenes obtenidas de servidores HTTP externos también se almacenan en la caché de datos de respuesta. Estas imágenes se validan automáticamente con la utilidad validate antes de que se genere la entrada de caché.

Platform Server compila datos de catálogo de imágenes para un acceso eficiente. Estos datos se almacenan en `CS::CatalogCacheFolder`.
