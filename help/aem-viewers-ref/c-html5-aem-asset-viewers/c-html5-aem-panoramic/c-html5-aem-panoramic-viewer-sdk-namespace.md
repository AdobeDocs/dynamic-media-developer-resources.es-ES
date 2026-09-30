---
title: Área de nombres de SDK de visor
description: Área de nombres de SDK de visor
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3360a3bd-8a4a-4bf9-98bf-ada7c35c58f4
autotag-review: '2026-05-13T22:16:34.426Z'
TQID: 'https://experienceleague.adobe.com/PVs-3zvwoKgc-rq6cssqCRnWH-SyyghZ5L-JguyZUl4'
product_v2:
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
source-wordcount: '220'
ht-degree: 0%
---
# Área de nombres de SDK de visor{#viewer-sdk-namespace}

El visor está formado por muchos componentes de Viewer SDK. Normalmente, la página web no necesita interactuar directamente con la API de componentes de SDK; todas las necesidades comunes se cubren en la propia API de visor.

Sin embargo, algunos casos de uso avanzados requieren que la página web haga referencia a un componente SDK interno mediante la API de visor `getComponent()` y, a continuación, utilice toda la flexibilidad de las API de SDK.

El área de nombres que el usuario utiliza para cargar e inicializar los componentes de SDK depende del entorno en el que funcione el usuario. Si el visor se está ejecutando en Adobe Experience Manager, cargará componentes de SDK en el espacio de nombres `s7viewers.s7sdk`. Del mismo modo, el visor servido desde Dynamic Media Classic carga SDK en `s7classic.s7sdk`.

En cualquier caso, el espacio de nombres utilizado por SDK dentro del visor tiene `s7viewers` o `s7classic` como prefijo. Además, es diferente del área de nombres `s7sdk` sin formato que se usa en la Guía del usuario de SDK o en la documentación de la API de SDK.

Por este motivo, es importante utilizar un área de nombres de SDK completa al escribir código de aplicación personalizado que se comunique con componentes del visor interno.

Por ejemplo, si planea escuchar el evento `StatusEvent.NOTF_VIEW_READY` y el visor se proporciona desde Experience Manager, el tipo de evento completo es `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` y el código del detector de eventos tiene un aspecto similar al siguiente:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
   panoramicView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
