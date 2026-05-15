---
title: disponer
description: Referencia de la API de JavaScript para el visor panorámico.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 4e6ad465-36df-49e2-8c9e-722e8aa9063e
autotag-review: '2026-05-13T22:08:54.657Z'
TQID: 'https://experienceleague.adobe.com/LIJyXNIBKd304RTksUCnN-g5vQjWBTvC-VWQNIgeKjo'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 3%

---

# disponer{#dispose}

Referencia de la API de JavaScript para el visor panorámico.

`dispose()`

Desecha esta instancia del visor liberando todos los recursos utilizados por la lógica del visor y eliminando todos los objetos y componentes internos creados por el visor en tiempo de ejecución.

El código de la página web también debe eliminar la variable de la instancia del visor para eliminar por completo el visor de la memoria del explorador web.

Si el código de la página web ha registrado detectores de eventos directamente en los componentes de Viewer SDK utilizados por el visor (o si ha almacenado referencias externas a dichos componentes), el código de la página web debe anular el registro de dichos detectores de forma explícita. Además, dichas referencias a componentes externos deben eliminarse antes de llamar a `dispose()`.

Ya no acceda a la API del visor después de llamar a `dispose()`.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
