---
title: disponer
description: Referencia de la API de JavaScript para eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 827decd9-1f6c-4ac1-8fcc-acc93cfb859d
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# disponer{#dispose}

Referencia de la API de JavaScript para eCatalog Viewer.

`dispose()`

Desecha esta instancia del visor liberando todos los recursos utilizados por la lógica del visor y eliminando todos los objetos y componentes internos creados por el visor en tiempo de ejecución.

El código de la página web también debe eliminar la variable de la instancia del visor para eliminar por completo el visor de la memoria del explorador web.

Si el código de la página web ha registrado detectores de eventos directamente en los componentes del SDK del visor utilizados por el visor (o si ha almacenado referencias externas a dichos componentes), el código de la página web debe anular el registro de dichos detectores de forma explícita. Además, estas referencias de componentes externos deben eliminarse antes de llamar a `dispose()`.

Ya no acceda a la API del visor después de `dispose()` se llama.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
