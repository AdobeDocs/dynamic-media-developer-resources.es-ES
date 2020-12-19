---
description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: b01f1497-8bee-4e01-8f92-272b324cb2dd
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# init{#init}

Referencia de la API de JavaScript para el visor de catálogos electrónicos.

[!DNL `init()`]

Inicio la inicialización del visor de catálogos electrónicos. Para este momento, se debe crear el elemento DOM de contenedor para que el código del visor pueda encontrarlo por su ID.

Si el elemento contenedor no forma parte del diseño de página web todavía (por ejemplo, puede ocultarse con el estilo [!DNL `display:none`] asignado), el visor suspende el proceso de inicialización hasta el momento en que la página web vuelve a colocar el elemento contenedor en el diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

Llame a este método una sola vez durante el ciclo de vida del visor; las llamadas subsiguientes se omiten.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

