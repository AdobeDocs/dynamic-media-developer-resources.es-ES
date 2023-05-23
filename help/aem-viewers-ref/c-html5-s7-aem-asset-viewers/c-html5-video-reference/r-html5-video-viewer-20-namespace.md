---
title: Espacio de nombres del SDK de visor
description: Espacio de nombres del SDK de visor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: d1f12c9d-9b00-44ee-bd91-76a4d882fecf
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Espacio de nombres del SDK de visor{#viewer-sdk-namespace}

El visor está formado por muchos componentes del SDK del visor. Normalmente, la página web no necesita interactuar directamente con la API de componentes del SDK; todas las necesidades comunes se cubren en la propia API de visor.

Sin embargo, algunos casos de uso avanzados requieren que la página web haga referencia a un componente interno del SDK mediante la variable `getComponent()` y, a continuación, utilice toda la flexibilidad de las API del propio SDK.

El área de nombres que utiliza el visor para cargar e inicializar los componentes del SDK depende del entorno en el que opera el visor. Si el visor se ejecuta en Adobe Experience Manager, carga componentes del SDK en `s7viewers.s7sdk` namespace. Del mismo modo, el visor servido desde Dynamic Media Classic carga el SDK en `s7classic.s7sdk`.

En cualquier caso, el área de nombres utilizada por el SDK dentro del visor tiene `s7viewers` o `s7classic` como prefijo. Y, es diferente de la llanura `s7sdk` espacio de nombres utilizado en la Guía del usuario de SDK o en la documentación de la API de SDK. Por este motivo, es importante utilizar un área de nombres de SDK completa al escribir código de aplicación personalizado que se comunique con componentes del visor interno.

Por ejemplo, si planea escuchar a `StatusEvent.NOTF_VIEW_READY` y el visor se suministra desde el Experience Manager, el tipo de evento completo es `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`y el código del detector de eventos tiene un aspecto similar al siguiente:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
