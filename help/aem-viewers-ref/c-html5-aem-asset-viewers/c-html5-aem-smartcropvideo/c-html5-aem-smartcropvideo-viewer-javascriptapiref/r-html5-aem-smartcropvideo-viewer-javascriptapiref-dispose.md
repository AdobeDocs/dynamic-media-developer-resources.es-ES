---
description: Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente.
solution: Experience Manager
title: dispose
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: c4bcccdc-6f23-4213-a1d1-03c5c62ba484
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# dispose{#dispose}

Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente.

`dispose()`

Elimina esta instancia del visor liberando todos los recursos utilizados por la lógica del visor y eliminando todos los objetos y componentes internos creados por el mismo durante la ejecución.

El código de la página web también debe eliminar la variable de instancia del visor para eliminarlo completamente de la memoria del explorador web.

Si el código de la página web tiene detectores de eventos registrados directamente en los componentes del SDK de visor utilizados por el visor o las referencias externas almacenadas a dichos componentes, dichos oyentes deben no estar registrados explícitamente en el código de la página web, y dichas referencias de componentes externos deben eliminarse antes de llamar a `dispose()`.

No acceda más a la API del visor después de `dispose()` se llama.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
