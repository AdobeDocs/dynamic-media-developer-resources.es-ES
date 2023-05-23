---
description: Describe métodos de operaciones nuevos y modificados para la versión 3.8 de la API de IPS.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 1%

---

# Operaciones: nuevas y modificadas{#operations-new-and-modified}

Describe métodos de operaciones nuevos y modificados para la versión 3.8 de la API de IPS.

Sintaxis

## Nuevas operaciones {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## Operaciones modificadas {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* El opcional `publishState` El parámetro permite buscar en `MarkedForPublish/NotMarkedForPublish` estado del recurso.

**getJobLogs**

* El opcional `userHandle` El parámetro permite recuperar los registros de trabajos enviados por un usuario específico.
