---
title: Llamadas obsoletas
description: Llamadas a la API de Image Production System y sus parámetros asociados que ya no se utilizan en Dynamic Media.
solution: Experience Manager
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Llamadas obsoletas{#deprecated-calls}

Llamadas a la API de Image Production System y sus parámetros asociados que ya no se utilizan.

## Llamadas obsoletas {#topic-654c0466e6434fe4a95953322255b08c}

Llamadas a la API de Image Production System y sus parámetros asociados que ya no se utilizan en Dynamic Media.

* `addMediaPortalEvent` - Obsoleto de Operaciones. Esta llamada le permite agregar un Evento de Media Portal a IPS.
* `getMediaPortalEvent` - Obsoleto de Operaciones. Esta llamada le permite obtener eventos del portal de medios que coincidan con los criterios especificados.
* `getCdnCacheInvalidationStatus` - Obsoleto de Operaciones. Esta API ahora está en desuso porque la API `cdnCacheInvalidation` invalida la caché casi inmediatamente (~5 segundos). Como tal, ya no es necesario sondear para obtener la invalidación.

