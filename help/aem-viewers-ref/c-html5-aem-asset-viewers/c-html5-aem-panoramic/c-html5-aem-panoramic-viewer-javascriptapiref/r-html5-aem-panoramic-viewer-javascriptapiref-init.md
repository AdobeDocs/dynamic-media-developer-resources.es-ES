---
title: init
description: Referencia de la API de JavaScript para el visor panorámico.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
autotag-review: '2026-05-13T22:09:33.410Z'
TQID: 'https://experienceleague.adobe.com/rpwcZhdc6cNM27k-LER-Bd8giGQkDzQTxJp0ejCDA8s'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
    internal-label: Dynamic Media Classic
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%
---
# init{#init}

Referencia de la API de JavaScript para el visor panorámico.

`init()`

Inicia la inicialización del visor panorámico. Para este momento, se debe crear el elemento DOM contenedor para que el código del visor pueda encontrarlo por su ID.

Si el elemento contenedor aún no forma parte del diseño de la página web (por ejemplo, puede estar oculto mediante el estilo `display:none` asignado a él), el visor suspende su proceso de inicialización. Lo hace hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando este evento se produce, la carga del visor se reanuda automáticamente.

Se debe llamar a este método solo una vez durante el ciclo de vida del visualizador, y se omiten las llamadas posteriores.

## Parámetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Ninguno.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Una referencia a la instancia del visor.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
