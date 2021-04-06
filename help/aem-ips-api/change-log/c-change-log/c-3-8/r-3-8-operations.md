---
description: Describe los métodos de operaciones nuevos y modificados para la API IPS versión 3.8.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
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
