---
description: Los datos de imagen intermedios producidos por solicitudes de servicio de imágenes anidadas/incrustadas y renderización de imágenes se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propietario en la caché de datos de respuesta.
solution: Experience Manager
title: Cachés de datos auxiliares
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Cachés de datos auxiliares{#auxiliary-data-caches}

Los datos de imagen intermedios producidos por solicitudes de servicio de imágenes anidadas/incrustadas y renderización de imágenes se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propietario en la caché de datos de respuesta.

Las imágenes obtenidas de servidores HTTP externos también se almacenan en la caché de datos de respuesta. Estas imágenes se validan automáticamente con la utilidad validate antes de que se genere la entrada de caché.

Platform Server compila datos de catálogo de imágenes para un acceso eficiente. Estos datos se almacenan en `CS::CatalogCacheFolder`.
