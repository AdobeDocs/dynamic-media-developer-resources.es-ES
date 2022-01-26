---
title: init
description: Referencia de la API de JavaScript para el visualizador de medios mixtos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4fb40cec-172a-41b3-98fc-927da88c7cb9
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# init{#init}

Referencia de la API de JavaScript para el visualizador de medios mixtos.

`init()`

Inicia la inicialización del visualizador de medios mixtos. Para este momento, se debe crear el elemento DOM contenedor para que el código del visor pueda encontrarlo con su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web, por ejemplo, puede ocultarse utilizando `display:none` style : el visor suspende su proceso de inicialización. Se suspende hasta el momento en que la página web vuelve a mostrar el elemento contenedor al diseño, momento en el que la carga del visor se reanuda automáticamente.

Llame a este método solo una vez durante el ciclo de vida del visor; las llamadas subsiguientes se ignoran.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
