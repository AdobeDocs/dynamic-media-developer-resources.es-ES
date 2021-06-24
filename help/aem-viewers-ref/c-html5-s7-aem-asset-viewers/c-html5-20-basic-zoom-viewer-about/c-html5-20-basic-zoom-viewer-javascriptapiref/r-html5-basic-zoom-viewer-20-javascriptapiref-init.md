---
description: Referencia de la API de JavaScript para el visor de zoom básico.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Developer,Business Practitioner
exl-id: cef585ae-44d7-406c-96f9-e03959a8e518
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# init{#init}

Referencia de la API de JavaScript para el visor de zoom básico.

`init()`

Inicia la inicialización del visor de zoom básico. Para este momento, se debe crear el elemento DOM contenedor para que el código del visor pueda encontrarlo con su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web (por ejemplo, puede que esté oculto empleando el estilo `display:none` asignado), el visor suspende su proceso de inicialización hasta el momento en que la página web devuelva el elemento contenedor al diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

Llame a este método solo una vez durante el ciclo de vida del visor; las llamadas subsiguientes se ignoran.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
