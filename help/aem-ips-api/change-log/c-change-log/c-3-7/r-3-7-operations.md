---
description: Describe los métodos de operaciones nuevos y modificados para la versión 3.7 de la API de IPS.
seo-description: Describe los métodos de operaciones nuevos y modificados para la versión 3.7 de la API de IPS.
seo-title: Operaciones nuevas y modificadas
solution: Experience Manager
title: Operaciones nuevas y modificadas
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

* Se ha eliminado `name` el parámetro.
* Agregado `excludeFieldArray`.

**getFolders**

* Agregado `excludeFieldArray`.

**getFolderTree**

* Añadido `excludeFieldArray` y `getUniqueMetadataValues`.
* Se ha realizado `fieldHandle` un parámetro requerido.

