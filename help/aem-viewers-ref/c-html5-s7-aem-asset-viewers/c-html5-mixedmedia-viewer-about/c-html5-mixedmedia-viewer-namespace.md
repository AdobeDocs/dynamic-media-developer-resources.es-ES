---
title: Área de nombres de SDK de visor
description: Área de nombres de SDK de visor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 570f8eee-a7dd-40aa-b732-03f97d2544c0
TQID: 'https://experienceleague.adobe.com/O-geIzN1KtPJNHuFzq-b9-TPnyAlevGMpvXJcRJmakM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 0%

---

# Área de nombres de SDK de visor{#viewer-sdk-namespace}

El visor está formado por muchos componentes de Viewer SDK. Normalmente, la página web no necesita interactuar directamente con la API de componentes de SDK; todas las necesidades comunes se cubren en la propia API de visor.

Sin embargo, algunos casos de uso avanzados requieren que la página web haga referencia a un componente SDK interno mediante la API de visor `getComponent()` y, a continuación, utilice toda la flexibilidad de las API de SDK.

El área de nombres que el usuario utiliza para cargar e inicializar los componentes de SDK depende del entorno en el que funcione el usuario. Si el visor se está ejecutando en Adobe Experience Manager, cargará componentes de SDK en el espacio de nombres `s7viewers.s7sdk`. Del mismo modo, el visor servido desde Dynamic Media Classic carga SDK en `s7classic.s7sdk`.

En cualquier caso, el espacio de nombres utilizado por SDK dentro del visor tiene `s7viewers` o `s7classic` como prefijo. Además, es diferente del área de nombres `s7sdk` sin formato que se usa en la Guía del usuario de SDK o en la documentación de la API de SDK. Por este motivo, es importante utilizar un área de nombres de SDK completa al escribir código de aplicación personalizado que se comunique con componentes del visor interno.

Por ejemplo, si planea escuchar el evento `StatusEvent.NOTF_VIEW_READY` y el visor se proporciona desde Experience Manager, el tipo de evento completo es `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` y el código del detector de eventos tiene un aspecto similar al siguiente:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
