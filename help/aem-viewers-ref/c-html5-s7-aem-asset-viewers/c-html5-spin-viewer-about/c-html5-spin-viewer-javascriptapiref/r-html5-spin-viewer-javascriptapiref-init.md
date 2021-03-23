---
description: Referencia de la API de JavaScript para el visualizador de giros.
seo-description: Referencia de la API de JavaScript para el visualizador de giros.
seo-title: init
solution: Experience Manager
title: init
uuid: 1803028f-dcba-49da-9fb7-78bfd64fc47d
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---


# init{#init}

Referencia de la API de JavaScript para el visualizador de giros.

`init()`

Inicia la inicialización del visualizador de giros. Para este momento, se debe crear el elemento contenedor `DOM` para que el código del visor pueda encontrarlo con su ID.

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

