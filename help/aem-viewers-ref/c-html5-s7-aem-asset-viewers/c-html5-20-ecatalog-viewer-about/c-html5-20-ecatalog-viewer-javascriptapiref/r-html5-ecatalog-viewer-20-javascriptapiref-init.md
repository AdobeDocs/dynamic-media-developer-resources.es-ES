---
description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 142381e4-aa3c-46dd-a0bd-4e090d0003e4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

Referencia de la API de JavaScript para el visor de catálogos electrónicos.

`init()`

Inicio la inicialización del visor de catálogos electrónicos. Para este momento, se debe crear el elemento DOM de contenedor para que el código del visor pueda encontrarlo por su ID.

Si el elemento de contenedor no forma parte del diseño de página web todavía (por ejemplo, puede estar oculto con `display:none` el estilo asignado), el visor suspende el proceso de inicialización hasta el momento en que la página web vuelve a colocar el elemento de contenedor en el diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

Llame a este método una sola vez durante el ciclo de vida del visor; las llamadas subsiguientes se omiten.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```

