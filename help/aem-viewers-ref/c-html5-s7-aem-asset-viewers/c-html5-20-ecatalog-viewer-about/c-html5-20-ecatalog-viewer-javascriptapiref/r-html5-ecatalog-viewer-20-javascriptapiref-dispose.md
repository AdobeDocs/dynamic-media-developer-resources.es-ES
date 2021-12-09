---
title: dispose
description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 827decd9-1f6c-4ac1-8fcc-acc93cfb859d
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# dispose{#dispose}

Referencia de la API de JavaScript para el visor de catálogos electrónicos.

`dispose()`

Elimina esta instancia del visor liberando todos los recursos utilizados por la lógica del visor y eliminando todos los objetos y componentes internos creados por el mismo durante la ejecución.

El código de la página web también debe eliminar la variable de instancia del visor para eliminarlo completamente de la memoria del explorador web.

Si el código de la página web ha registrado oyentes de eventos directamente en los componentes del SDK de visor utilizados por el visor (o si se han almacenado referencias externas a dichos componentes), el código de la página web debe anular explícitamente el registro de dichos oyentes. Además, dichas referencias de componentes externos deben eliminarse antes de llamar a `dispose()`.

No acceda a la API del visor después de `dispose()` se llama.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
