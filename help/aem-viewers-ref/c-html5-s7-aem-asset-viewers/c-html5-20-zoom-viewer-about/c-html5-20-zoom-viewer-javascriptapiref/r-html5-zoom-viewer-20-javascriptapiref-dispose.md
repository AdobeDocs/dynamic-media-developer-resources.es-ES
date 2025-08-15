---
title: disponer
description: Referencia de la API de JavaScript para el visor de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c796943e-8ea8-4a97-a1ff-09676204150a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# disponer{#dispose}

Referencia de la API de JavaScript para el visor de zoom.

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
