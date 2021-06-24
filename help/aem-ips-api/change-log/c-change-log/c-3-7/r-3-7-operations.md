---
description: Describe los métodos de operaciones nuevos y modificados para la API IPS versión 3.7.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '53'
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
