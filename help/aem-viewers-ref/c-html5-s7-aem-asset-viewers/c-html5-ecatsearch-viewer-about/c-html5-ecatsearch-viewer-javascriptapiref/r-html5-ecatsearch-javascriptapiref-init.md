---
description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# init{#init}

Referencia de la API de JavaScript para el visor de catálogos electrónicos.

[!DNL `init()`]

Inicia la inicialización del visor del catálogo electrónico. Para este momento, se debe crear el elemento DOM del contenedor para que el código del visor pueda encontrarlo con su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web (por ejemplo, puede que esté oculto empleando el estilo [!DNL `display:none`] asignado), el visor suspende su proceso de inicialización hasta el momento en que la página web devuelva el elemento contenedor al diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

Llame a este método solo una vez durante el ciclo de vida del visor; las llamadas subsiguientes se ignoran.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
