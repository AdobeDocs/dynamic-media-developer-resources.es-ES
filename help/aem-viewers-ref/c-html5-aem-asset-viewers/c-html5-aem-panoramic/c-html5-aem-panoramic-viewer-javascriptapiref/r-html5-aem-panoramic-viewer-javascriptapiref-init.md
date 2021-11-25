---
title: init
description: Referencia de la API de JavaScript para el visor panorámico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# init{#init}

Referencia de la API de JavaScript para el visor panorámico.

`init()`

Inicia la inicialización del Visor panorámico. Para este momento, se debe crear el elemento DOM contenedor para que el código del visor pueda encontrarlo con su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web (por ejemplo, puede ocultarse utilizando `display:none` le ha sido asignado), el visor suspende su proceso de inicialización. Lo hace hasta el momento en que la página web vuelve a mostrar el elemento contenedor al diseño. Cuando se produce este evento, la carga del visor se reanuda automáticamente.

Se debe llamar a este método solo una vez durante el ciclo de vida del visualizador; las llamadas posteriores se ignoran.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
