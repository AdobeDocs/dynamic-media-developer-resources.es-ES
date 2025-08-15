---
title: disponer
description: Referencia de la API de JavaScript para el visualizador de imágenes de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 8af8506e-6b29-45ea-a70b-3eb3b2995047
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# disponer{#dispose}

Referencia de la API de JavaScript para el visualizador de imágenes de vídeo.

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
