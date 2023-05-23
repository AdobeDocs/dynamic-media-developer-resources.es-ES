---
description: Describe tipos nuevos y cambiados para la versión 6 de la API de IPS.
solution: Experience Manager
title: Tipos de datos nuevos y modificados
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

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

**Agregado**

* Añadido `numUrls` hasta `UploadUrlsJob`.

* Añadido `fileName` hasta `Asset.`

* Añadido `isHidden` hasta `MetadataField`.

* Añadido `taskState` hasta `TaskProgress`.

* Añadido `exportJob` hasta `ActiveJob` y `ScheduledJob`.

* Añadido `optmizedPath` y `optimizedFile` hasta `PsdInfo`.

* Añadido `contextHandle` hasta:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Se agregaron los siguientes parámetros a `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Se cambió**

* Entrada `User`, cambiado `role` hasta `defaultRole`.

* Entrada `Folder`, cambiado `permissions` hasta `permissionsSetHandle`.

* Entrada `AssetSummary`, `type` y `name` ahora son opcionales.
