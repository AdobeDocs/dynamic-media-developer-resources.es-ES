---
description: Describe los tipos nuevos y modificados para la versión 6 de la API de IPS.
solution: Experience Manager
title: Tipos de datos nuevos y modificados
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---


# Tipos de datos: Nuevo y modificado{#data-types-new-and-modified}

Describe los tipos nuevos y modificados para la versión 6 de la API de IPS.

Sintaxis

## Nuevos tipos {#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## Tipos modificados {#section-56b834b1a3b843279d8715b4a4f3890b}

**Agregado**

* Se añadió `numUrls` a `UploadUrlsJob`.

* Añadido `fileName` a `Asset.`

* Se añadió `isHidden` a `MetadataField`.

* Se añadió `taskState` a `TaskProgress`.

* Se añadió `exportJob` a `ActiveJob` y `ScheduledJob`.

* Se añadieron `optmizedPath` y `optimizedFile` a `PsdInfo`.

* Se añadió `contextHandle` en:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Se añadieron los siguientes parámetros en `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Se cambió**

* En `User`, cambió `role` a `defaultRole`.

* En `Folder`, cambió `permissions` a `permissionsSetHandle`.

* En `AssetSummary`, `type` y `name` son ahora opcionales.

