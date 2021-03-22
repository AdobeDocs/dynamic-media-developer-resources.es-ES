---
description: Referencia de la API de JavaScript para el visor de carrusel.
seo-description: Referencia de la API de JavaScript para el visor de carrusel.
seo-title: init
solution: Experience Manager
title: init
uuid: f109d9ab-d5f0-462d-9e7d-c5e32629e449
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---


# init{#init}

Referencia de la API de JavaScript para el visor de carrusel.

`init()`

Inicia la inicialización del visor de carrusel. Para este momento, se debe crear el elemento DOM contenedor para que el código del visor pueda encontrarlo con su ID.

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

