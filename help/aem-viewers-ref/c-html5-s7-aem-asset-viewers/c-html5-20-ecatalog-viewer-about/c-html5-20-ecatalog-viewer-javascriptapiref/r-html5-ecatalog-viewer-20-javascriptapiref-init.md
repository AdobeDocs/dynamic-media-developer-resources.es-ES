---
title: init
description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e7775a65-67bf-4ad6-8e51-1fdf141946bc
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# init{#init}

Referencia de la API de JavaScript para el visor de catálogos electrónicos.

`init()`

Inicia la inicialización del visor del catálogo electrónico. Para este momento, se debe crear el elemento DOM del contenedor para que el código del visor pueda encontrarlo con su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web, por ejemplo, puede ocultarse utilizando `display:none` estilo asignado a él : el visor suspende su proceso de inicialización. Lo hace hasta el momento en que la página web vuelve a mostrar el elemento contenedor al diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

Llame a este método solo una vez durante el ciclo de vida del visor; las llamadas subsiguientes se ignoran.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```
