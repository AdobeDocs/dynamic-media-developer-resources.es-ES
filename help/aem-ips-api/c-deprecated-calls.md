---
title: Llamadas obsoletas
description: Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan en Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# Llamadas obsoletas{#deprecated-calls}

Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan.

## Llamadas obsoletas {#topic-654c0466e6434fe4a95953322255b08c}

Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan en Dynamic Media.

* `addMediaPortalEvent` - Obsoleto de Operaciones. Esta llamada le permite agregar un evento de Media Portal a IPS.
* `getMediaPortalEvent` - Obsoleto de Operaciones. Esta llamada le permite obtener eventos de portal de medios que coincidan con los criterios especificados.
* `getCdnCacheInvalidationStatus` - Obsoleto de Operaciones. Esta API ya no se utiliza porque la API `cdnCacheInvalidation` invalida la caché casi inmediatamente (~5 segundos). Como tal, ya no es necesario sondear para obtener el estado de invalidación.

