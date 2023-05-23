---
description: Referencia de la API de JavaScript para el visor flotante.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# init{#init}

Referencia de la API de JavaScript para el visor flotante.

`init()`

Inicia la inicialización del visor flotante. Para este momento, se debe crear el elemento DOM contenedor para que el código del visor pueda encontrarlo por su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web (por ejemplo, puede ocultarse utilizando ) `display:none` estilo asignado a él), el visor suspende su proceso de inicialización hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando esto sucede, la carga del visualizador se reanuda automáticamente.

Se debe llamar a este método solo una vez durante el ciclo de vida del visualizador, y se omiten las llamadas consiguientes.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Una referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
