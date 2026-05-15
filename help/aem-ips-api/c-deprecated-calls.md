---
title: Llamadas obsoletas
description: Llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se usan ni admiten en  [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
autotag-review: '2026-05-13T21:03:57.183Z'
TQID: 'https://experienceleague.adobe.com/JLoyXksHQ-LAXXxfY71Dv-FOE0trpt-RzcKcV-Pv96I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 0%

---

# Llamadas obsoletas{#deprecated-calls}

Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan.

## Llamadas obsoletas {#topic-654c0466e6434fe4a95953322255b08c}

Llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se usan en [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS` - Obsoleto de [tipos de datos](/help/aem-ips-api/types/c-data-types/c-data-types.md). Este parámetro excluía el vídeo principal del conjunto de vídeos adaptables. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Obsoleto de [operaciones](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Este parámetro permite agregar un evento de Media Portal a IPS.
* `getMediaPortalEvent` - Obsoleto de [operaciones](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Este parámetro permite obtener eventos de portal de medios que coincidan con los criterios especificados.
* `getCdnCacheInvalidationStatus` - Obsoleto de [operaciones](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Este parámetro está obsoleto porque el parámetro `cdnCacheInvalidation` invalida la caché casi inmediatamente (~5 segundos). Como tal, ya no es necesario sondear para obtener el estado de invalidación.
