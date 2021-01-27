---
description: Referencia de la API de JavaScript para el visor flotante.
seo-description: Referencia de la API de JavaScript para el visor flotante.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic Media
uuid: e5d990af-1c5a-4253-8ecd-b51119cee3a2
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 2%

---


# init{#init}

Referencia de la API de JavaScript para el visor flotante.

`init()`

Inicio la inicialización del visor flotante. Para este momento, se debe crear el elemento DOM de contenedor para que el código del visor pueda encontrarlo por su ID.

Si el elemento contenedor no forma parte del diseño de página web todavía (por ejemplo, puede ocultarse con el estilo `display:none` asignado), el visor suspende el proceso de inicialización hasta el momento en que la página web vuelve a colocar el elemento contenedor en el diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

Este método solo debe llamarse una vez durante el ciclo de vida del visor; se omiten las llamadas consiguientes.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

