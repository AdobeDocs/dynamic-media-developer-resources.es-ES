---
description: Los datos de imagen intermedios producidos por las solicitudes de servicio de imágenes y procesamiento de imágenes anidadas/incrustadas se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propio en la caché de datos de respuesta.
solution: Experience Manager
title: Cachés de datos auxiliares
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
TQID: 'https://experienceleague.adobe.com/oRZFSXKaBE9q7liBPRVCheL-NPTriPJkWZFqgMBcoaQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# Cachés de datos auxiliares{#auxiliary-data-caches}

Los datos de imagen intermedios producidos por las solicitudes de servicio de imágenes y procesamiento de imágenes anidadas/incrustadas se pueden almacenar en caché especificando cache=on en la solicitud anidada/incrustada. Estos datos se almacenan en formato propio en la caché de datos de respuesta.

Las imágenes obtenidas de servidores HTTP externos también se almacenan en la caché de datos de respuesta. Estas imágenes se validan automáticamente con la utilidad validate antes de generar la entrada de caché.

[!DNL Platform Server] compila los datos del catálogo de imágenes para obtener un acceso eficiente. Estos datos se almacenan en `CS::CatalogCacheFolder`.
