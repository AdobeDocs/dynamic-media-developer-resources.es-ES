---
title: init
description: Referencia de la API de JavaScript para el visor de giros.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
TQID: 'https://experienceleague.adobe.com/BfId4EhSvlyMT-vHJ0rDS-FqpXHeE-krXrvyCevgUKU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# init{#init}

Referencia de la API de JavaScript para el visor de giros.

`init()`

Inicia la inicialización del visor de giros. Para este momento, se debe crear el elemento contenedor `DOM` para que el código de visor pueda encontrarlo por su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web (por ejemplo, si se oculta con el estilo `display:none`), el visor suspende el proceso de inicialización. Se suspende hasta el momento en que la página web devuelve el elemento contenedor al diseño, momento en el que la carga del visualizador se reanuda automáticamente.

Llame a este método solo una vez durante el ciclo de vida del visor; las llamadas posteriores se omiten.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Una referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
