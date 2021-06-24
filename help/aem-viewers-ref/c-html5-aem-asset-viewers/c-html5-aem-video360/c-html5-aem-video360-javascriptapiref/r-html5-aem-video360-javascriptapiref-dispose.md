---
description: Referencia de la API de JavaScript para el visualizador de Video360.
solution: Experience Manager
title: dispose
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Developer,Business Practitioner
exl-id: 4e6ad465-36df-49e2-8c9e-722e8aa9063e
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---

# dispose{#dispose}

Referencia de la API de JavaScript para el visualizador de Video360.

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
