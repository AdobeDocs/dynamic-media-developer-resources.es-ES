---
description: Describe métodos de operaciones nuevos y modificados para la versión 3.7 de la API de IPS.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 6%

---

# Operaciones: nuevas y modificadas{#operations-new-and-modified}

Describe métodos de operaciones nuevos y modificados para la versión 3.7 de la API de IPS.

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

* Eliminado `name` parámetro.
* Agregado `excludeFieldArray`.

**getFolders**

* Agregado `excludeFieldArray`.

**getFolderTree**

* Añadido `excludeFieldArray` y `getUniqueMetadataValues`.
* Creado `fieldHandle` un parámetro requerido.
