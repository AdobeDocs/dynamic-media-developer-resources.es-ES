---
description: Describe los métodos de operaciones nuevos y modificados para la versión 3.7 de la API de IPS.
solution: Experience Manager
title: Operaciones nuevas y modificadas
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 6%

---


# Operaciones: Nuevo y modificado{#operations-new-and-modified}

Describe los métodos de operaciones nuevos y modificados para la versión 3.7 de la API de IPS.

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

* Se eliminó el parámetro `name`.
* Agregado `excludeFieldArray`.

**getFolders**

* Agregado `excludeFieldArray`.

**getFolderTree**

* Se añadieron `excludeFieldArray` y `getUniqueMetadataValues`.
* Se ha convertido `fieldHandle` en un parámetro requerido.

