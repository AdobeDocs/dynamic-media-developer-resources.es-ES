---
description: Referencia de la API de JavaScript para el visor de giros.
seo-description: Referencia de la API de JavaScript para el visor de giros.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic Media
uuid: 1803028f-dcba-49da-9fb7-78bfd64fc47d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# init{#init}

Referencia de la API de JavaScript para el visor de giros.

`init()`

Inicio la inicialización del visor de giros. Para este momento, se debe crear el elemento contenedor `DOM` para que el código del visor pueda encontrarlo por su ID.

Si el elemento contenedor no forma parte del diseño de página web todavía (por ejemplo, puede ocultarse con el estilo `display:none` asignado), el visor suspende el proceso de inicialización hasta el momento en que la página web vuelve a colocar el elemento contenedor en el diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

Llame a este método solo una vez durante el ciclo de vida del visor; las llamadas subsiguientes se omiten.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

