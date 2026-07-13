---
description: Describe tipos nuevos y cambiados para la versión 6 de la API de IPS.
solution: Experience Manager
title: Tipos de datos nuevos y modificados
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
TQID: 'https://experienceleague.adobe.com/LI8xzlS2eACzYqcV3krzThLm77-z6imYLohPRCTHIYs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 1%

---

# Tipos de datos: nuevos y modificados{#data-types-new-and-modified}

Describe tipos nuevos y cambiados para la versión 6 de la API de IPS.

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

**Se agregó**

* Se agregó `numUrls` a `UploadUrlsJob`.

* Agregó `fileName` a `Asset.`

* Se agregó `isHidden` a `MetadataField`.

* Se agregó `taskState` a `TaskProgress`.

* Se agregó `exportJob` a `ActiveJob` y `ScheduledJob`.

* Se agregaron `optmizedPath` y `optimizedFile` a `PsdInfo`.

* Se agregó `contextHandle` a:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Se agregaron los siguientes parámetros a `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Cambiado**

* En `User`, cambió `role` a `defaultRole`.

* En `Folder`, cambió `permissions` a `permissionsSetHandle`.

* En `AssetSummary`, `type` y `name` son ahora opcionales.

