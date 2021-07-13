---
description: Referencia de la API de JavaScript para el visualizador de medios mixtos.
solution: Experience Manager
title: dispose
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de medios mixtos
role: Developer,User
exl-id: e09f73a9-a961-4188-b092-f7bbcae4946d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# dispose{#dispose}

Referencia de la API de JavaScript para el visualizador de medios mixtos.

`dispose()`

Elimina esta instancia del visor liberando todos los recursos utilizados por la lógica del visor y eliminando todos los objetos y componentes internos creados por el mismo durante la ejecución.

El código de la página web también debe eliminar la variable de instancia del visor para eliminarlo completamente de la memoria del explorador web.

Si el código de la página web ha registrado oyentes de eventos directamente en los componentes del SDK de visor utilizados por el visor o las referencias externas almacenadas a dichos componentes, dichos oyentes deben no estar registrados explícitamente en el código de la página web y dichas referencias de componentes externos deben eliminarse antes de llamar a `dispose()`.

No acceda más a la API del visor después de llamar a `dispose()`.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
