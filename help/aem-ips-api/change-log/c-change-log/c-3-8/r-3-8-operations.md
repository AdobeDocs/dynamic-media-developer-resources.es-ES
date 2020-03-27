---
description: Describe los métodos de operaciones nuevos y modificados para la versión 3.8 de la API de IPS.
seo-description: Describe los métodos de operaciones nuevos y modificados para la versión 3.8 de la API de IPS.
seo-title: Operaciones nuevas y modificadas
solution: Experience Manager
title: Operaciones nuevas y modificadas
topic: Scene7 Image Production System API
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Operaciones: Nuevo y modificado{#operations-new-and-modified}

Describe los métodos de operaciones nuevos y modificados para la versión 3.8 de la API de IPS.

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

* El `publishState` parámetro opcional permite buscar en el estado del `MarkedForPublish/NotMarkedForPublish` recurso.

**getJobLogs**

* El parámetro opcional `userHandle` permite recuperar registros de trabajo enviados por un usuario específico.

