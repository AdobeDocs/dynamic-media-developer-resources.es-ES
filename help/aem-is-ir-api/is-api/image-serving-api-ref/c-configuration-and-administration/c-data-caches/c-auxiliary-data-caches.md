---
description: Los datos de imagen intermedios producidos por las solicitudes de servicio de imágenes y procesamiento de imágenes anidadas/incrustadas se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propio en la caché de datos de respuesta.
solution: Experience Manager
title: Cachés de datos auxiliares
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Cachés de datos auxiliares{#auxiliary-data-caches}

Los datos de imagen intermedios producidos por las solicitudes de servicio de imágenes y procesamiento de imágenes anidadas/incrustadas se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propio en la caché de datos de respuesta.

Las imágenes obtenidas de servidores HTTP externos también se almacenan en la caché de datos de respuesta. Estas imágenes se validan automáticamente con la utilidad validate antes de generar la entrada de caché.

[!DNL Platform Server] compila los datos del catálogo de imágenes para obtener un acceso eficiente. Estos datos se almacenan en `CS::CatalogCacheFolder`.
