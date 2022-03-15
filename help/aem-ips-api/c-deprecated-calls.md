---
title: Llamadas obsoletas
description: Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan ni admiten en Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 25d9de1d9ba727e72c031ab22c47bd2be5c11050
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Llamadas obsoletas{#deprecated-calls}

Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan.

## Llamadas obsoletas {#topic-654c0466e6434fe4a95953322255b08c}

Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan en Dynamic Media.

* `ExcludeMasterVideoFromAVS` - Obsoleto desde [Tipos de datos](/help/aem-ips-api/types/c-data-types/c-data-types.md). Este parámetro excluyó el vídeo principal del conjunto de vídeos adaptables.
   >[!IMPORTANT]
   >
   >Adobe dejará de ofrecer asistencia para este parámetro el 1 de septiembre de 2022. Consulte también [ExcludeMasterVideoFromAVS](/help/aem-ips-api/types/c-data-types/r-exclude-master-video-from-avs.md).

* `addMediaPortalEvent` - Obsoleto desde [Operaciones](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Este parámetro le permite agregar un evento de Media Portal a IPS.
* `getMediaPortalEvent` - Obsoleto desde [Operaciones](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Este parámetro le permite obtener eventos de portal de medios que coincidan con los criterios especificados.
* `getCdnCacheInvalidationStatus` - Obsoleto desde [Operaciones](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Este parámetro ya no se utiliza porque la variable `cdnCacheInvalidation` invalida la caché casi inmediatamente (~5 segundos). Como tal, ya no es necesario sondear para obtener el estado de invalidación.
