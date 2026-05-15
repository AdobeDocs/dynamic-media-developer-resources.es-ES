---
title: init
description: Referencia de la API de JavaScript para la inicialización del visor flotante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
TQID: 'https://experienceleague.adobe.com/vavSoeUebo8YrntPoPKm3why-Jbzrh4p6v8Eqmgsv1I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 2%

---

# init{#init}

Referencia de la API de JavaScript para el visor flotante.

`init()`

Inicia la inicialización del visor flotante. Para este momento, se debe crear el elemento DOM contenedor para que el código del visor pueda encontrarlo por su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web (por ejemplo, puede estar oculto al utilizar el estilo `display:none` asignado), el visor suspende el proceso de inicialización. Lo hace hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando esto sucede, la carga del visualizador se reanuda automáticamente.

Se debe llamar a este método solo una vez durante el ciclo de vida del visualizador, y se omiten las llamadas consiguientes.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Una referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
