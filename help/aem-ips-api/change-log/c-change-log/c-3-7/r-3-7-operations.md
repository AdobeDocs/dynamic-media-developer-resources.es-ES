---
description: Describe los métodos de operaciones nuevos y modificados para la API IPS versión 3.7.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 5%

---


# Operaciones: Nuevo y modificado{#operations-new-and-modified}

Describe los métodos de operaciones nuevos y modificados para la API IPS versión 3.7.

Sintaxis

## Nuevas operaciones {#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## Operaciones modificadas {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* Se ha eliminado el parámetro `name`.
* Agregado `excludeFieldArray`.

**getFolders**

* Agregado `excludeFieldArray`.

**getFolderTree**

* Se agregaron `excludeFieldArray` y `getUniqueMetadataValues`.
* Se ha convertido `fieldHandle` en un parámetro obligatorio.

