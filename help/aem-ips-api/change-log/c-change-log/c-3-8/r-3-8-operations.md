---
description: Describe los métodos de operaciones nuevos y modificados para la API IPS versión 3.8.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# Operaciones: Nuevo y modificado{#operations-new-and-modified}

Describe los métodos de operaciones nuevos y modificados para la API IPS versión 3.8.

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

* El parámetro opcional `publishState` permite buscar en el estado del recurso `MarkedForPublish/NotMarkedForPublish`.

**getJobLogs**

* El parámetro opcional `userHandle` permite recuperar los registros de trabajo enviados por un usuario específico.

