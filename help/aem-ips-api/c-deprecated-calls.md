---
title: Llamadas obsoletas
description: Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan ni admiten en [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Llamadas obsoletas{#deprecated-calls}

Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan.

## Llamadas obsoletas {#topic-654c0466e6434fe4a95953322255b08c}

Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan en [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS` - Obsoleto desde [Tipos de datos](/help/aem-ips-api/types/c-data-types/c-data-types.md). Este parámetro excluía el vídeo principal del conjunto de vídeos adaptables. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Obsoleto desde [Operaciones](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Este parámetro permite agregar un evento de Media Portal a IPS.
* `getMediaPortalEvent` - Obsoleto desde [Operaciones](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Este parámetro permite obtener eventos de portal de medios que coincidan con los criterios especificados.
* `getCdnCacheInvalidationStatus` - Obsoleto desde [Operaciones](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Este parámetro está obsoleto porque el `cdnCacheInvalidation` El parámetro invalida la caché casi inmediatamente (~5 segundos). Como tal, ya no es necesario sondear para obtener el estado de invalidación.
