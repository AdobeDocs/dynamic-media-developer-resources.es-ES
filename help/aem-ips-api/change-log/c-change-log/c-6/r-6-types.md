---
description: Describe los tipos nuevos y modificados para la versión 6 de la API de IPS.
seo-description: Describe los tipos nuevos y modificados para la versión 6 de la API de IPS.
seo-title: Tipos de datos nuevos y modificados
solution: Experience Manager
title: Tipos de datos nuevos y modificados
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Tipos de datos: Nuevo y modificado{#data-types-new-and-modified}

Describe los tipos nuevos y modificados para la versión 6 de la API de IPS.

Sintaxis

## Tipos nuevos {#section-71ba6954339e4ba899acdf8a3212d6f3}

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

* Añadido `numUrls` a `UploadUrlsJob`.

* Añadido `fileName` a `Asset.`

* Añadido `isHidden` a `MetadataField`.

* Añadido `taskState` a `TaskProgress`.

* Añadido `exportJob` a `ActiveJob` y `ScheduledJob`.

* Añadido `optmizedPath` y `optimizedFile` a `PsdInfo`.

* Añadido `contextHandle` a:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Se Añadieron los siguientes parámetros en `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Se cambió**

* En `User`, cambió `role` a `defaultRole`.

* En `Folder`, cambió `permissions` a `permissionsSetHandle`.

* En `AssetSummary`, `type` y `name` ahora son opcionales.

