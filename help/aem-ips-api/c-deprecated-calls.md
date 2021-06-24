---
title: Llamadas obsoletas
description: Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan en Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Llamadas obsoletas{#deprecated-calls}

Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan.

## Llamadas obsoletas {#topic-654c0466e6434fe4a95953322255b08c}

Las llamadas a la API del sistema de producción de imágenes y sus parámetros asociados que ya no se utilizan en Dynamic Media.

* `addMediaPortalEvent` - Obsoleto de Operaciones. Esta llamada le permite agregar un evento de Media Portal a IPS.
* `getMediaPortalEvent` - Obsoleto de Operaciones. Esta llamada le permite obtener eventos de portal de medios que coincidan con los criterios especificados.
* `getCdnCacheInvalidationStatus` - Obsoleto de Operaciones. Esta API ya no se utiliza porque la API `cdnCacheInvalidation` invalida la caché casi inmediatamente (~5 segundos). Como tal, ya no es necesario sondear para obtener el estado de invalidación.
