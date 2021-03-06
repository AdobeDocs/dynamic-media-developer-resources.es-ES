---
description: Describe los tipos nuevos y modificados para la API IPS versión 6.
solution: Experience Manager
title: Tipos de datos nuevos y modificados
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 4%

---

# Tipos de datos: Nuevo y modificado{#data-types-new-and-modified}

Describe los tipos nuevos y modificados para la API IPS versión 6.

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

* Se ha agregado `numUrls` a `UploadUrlsJob`.

* Se ha agregado `fileName` a `Asset.`

* Se ha agregado `isHidden` a `MetadataField`.

* Se ha agregado `taskState` a `TaskProgress`.

* Se ha agregado `exportJob` a `ActiveJob` y `ScheduledJob`.

* Se agregaron `optmizedPath` y `optimizedFile` a `PsdInfo`.

* Se ha agregado `contextHandle` a:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Se agregaron los siguientes parámetros a `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Se cambió**

* En `User`, cambió `role` a `defaultRole`.

* En `Folder`, cambió `permissions` a `permissionsSetHandle`.

* En `AssetSummary`, `type` y `name` ahora son opcionales.
