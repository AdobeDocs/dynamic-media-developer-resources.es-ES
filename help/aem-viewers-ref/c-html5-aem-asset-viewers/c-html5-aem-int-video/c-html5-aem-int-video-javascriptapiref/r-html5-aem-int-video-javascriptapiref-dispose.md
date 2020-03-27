---
description: Referencia de la API de JavaScript para el visor de vídeo interactivo.
seo-description: Referencia de la API de JavaScript para el visor de vídeo interactivo.
seo-title: eliminar
solution: Experience Manager
title: eliminar
topic: Dynamic media
uuid: 95046b8c-1277-4954-b13d-329994d0cb04
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# eliminar{#dispose}

Referencia de la API de JavaScript para el visor de vídeo interactivo.

`dispose()`

Desecha esta instancia de visor liberando todos los recursos utilizados por la lógica del visor y eliminando todos los objetos y componentes internos creados por el visor en tiempo de ejecución.

El código de página web también debe eliminar la variable de instancia del visor para eliminar completamente el visor de la memoria del navegador web.

Si el código de la página web tiene detectores de evento registrados directamente en los componentes del SDK de visor utilizados por el visor o las referencias externas almacenadas a dichos componentes, estos detectores deben quedar explícitamente sin registrar en el código de la página web y dichas referencias de componentes externos deben eliminarse antes de llamar `dispose()`.

Ya no acceda a la API de visor después de `dispose()` llamar.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

