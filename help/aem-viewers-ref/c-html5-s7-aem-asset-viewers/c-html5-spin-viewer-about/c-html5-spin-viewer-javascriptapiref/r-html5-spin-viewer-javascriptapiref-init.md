---
title: init
description: Referencia de la API de JavaScript para el visualizador de giros.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# init{#init}

Referencia de la API de JavaScript para el visualizador de giros.

`init()`

Inicia la inicialización del visualizador de giros. Para este momento, el contenedor `DOM` debe crearse para que el código del visor pueda encontrarlo con su ID.

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
