---
title: disponer
description: Referencia de la API de JavaScript para el visor flotante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: bf38d481-d8cc-400c-9017-bcb3471f2a10
TQID: 'https://experienceleague.adobe.com/YZaEBBBq9KjjVvbvOzyQzNw6-Vhs2VOS-pHP5Gn6AUE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 3%

---

# disponer{#dispose}

Referencia de la API de JavaScript para el visor flotante.

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
