---
description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-title: dispose
solution: Experience Manager
title: dispose
uuid: 791c47e9-daab-4500-9cd0-e56ee6fc830e
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# eliminar{#dispose}

Referencia de la API de JavaScript para el visor de catálogos electrónicos.

[!DNL `dispose()`]

Elimina esta instancia del visor liberando todos los recursos utilizados por la lógica del visor y eliminando todos los objetos y componentes internos creados por el mismo durante la ejecución.

El código de la página web también debe eliminar la variable de instancia del visor para eliminarlo completamente de la memoria del explorador web.

Si el código de la página web ha registrado oyentes de eventos directamente en los componentes del SDK de visor utilizados por el visor o las referencias externas almacenadas a dichos componentes, dichos oyentes deben no estar registrados explícitamente en el código de la página web y dichas referencias de componentes externos deben eliminarse antes de llamar a [!DNL `dispose()`].

No acceda más a la API del visor después de llamar a [!DNL `dispose()`].

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

