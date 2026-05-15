---
title: init
description: Referencia de la API de JavaScript para el visor de Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
TQID: 'https://experienceleague.adobe.com/oQ58fSdlQSgf4Hv58vEdJtI7u23lJzr6U5uSIhvTfEU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 2%

---

# init{#init}

Referencia de la API de JavaScript para el visor de Video360.

`init()`

Inicia la inicialización del visor de Video360. Para este momento, se debe crear el elemento DOM contenedor para que el código del visor pueda encontrarlo por su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web (por ejemplo, puede estar oculto mediante el estilo `display:none` asignado a él), el visor suspende su proceso de inicialización. Lo hace hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando este evento se produce, la carga del visor se reanuda automáticamente.

Llame a este método solo una vez durante el ciclo de vida del visor; las llamadas posteriores se omiten.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Una referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
