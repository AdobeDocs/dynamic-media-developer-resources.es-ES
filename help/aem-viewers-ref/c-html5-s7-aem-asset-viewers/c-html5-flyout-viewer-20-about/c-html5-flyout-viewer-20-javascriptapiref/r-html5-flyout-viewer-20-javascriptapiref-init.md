---
description: Referencia de la API de JavaScript para el visor flotante.
seo-description: Referencia de la API de JavaScript para el visor flotante.
seo-title: init
solution: Experience Manager
title: init
uuid: e5d990af-1c5a-4253-8ecd-b51119cee3a2
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flotante
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# init{#init}

Referencia de la API de JavaScript para el visor flotante.

`init()`

Inicia la inicialización del visor flotante. Para este momento, se debe crear el elemento DOM contenedor para que el código del visor pueda encontrarlo con su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web (por ejemplo, puede que esté oculto empleando el estilo `display:none` asignado), el visor suspende su proceso de inicialización hasta el momento en que la página web devuelva el elemento contenedor al diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

Se debe llamar a este método solo una vez durante el ciclo de vida del visualizador; las llamadas consiguientes se ignoran.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

