---
description: Espacio de nombres del SDK del visor
solution: Experience Manager
title: Espacio de nombres del SDK del visor
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Developer,Business Practitioner
exl-id: 2b4b0b31-3c88-42a4-8a81-5534691e318f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Espacio de nombres del SDK del visor{#viewer-sdk-namespace}

El visor está integrado por muchos componentes del SDK de visor. En la mayoría de los casos, la página web no necesita interactuar directamente con la API de componentes del SDK; todas las necesidades comunes se cubren en la propia API del visor.

Sin embargo, algunos casos de uso avanzados requieren que la página web obtenga una referencia a un componente SDK interno mediante la API del visor `getComponent()` y, a continuación, utilice toda la flexibilidad de las API del propio SDK.

El espacio de nombres que utiliza el visor para cargar e inicializar componentes del SDK depende del entorno en el que funcione el visor. Si el visor se está ejecutando en AEM (Adobe Experience Manager), el visor carga los componentes del SDK en el espacio de nombres `s7viewers.s7sdk`. Del mismo modo, el visor servido desde Dynamic Media Classic carga el SDK en `s7classic.s7sdk`.

En cualquier caso, el espacio de nombres utilizado por el SDK dentro del visor tiene el prefijo `s7viewers` o `s7classic`. Además, es diferente del espacio de nombres simple `s7sdk` utilizado en la guía del usuario del SDK o en la documentación de la API del SDK. Por este motivo, es importante utilizar un espacio de nombres del SDK totalmente cualificado al escribir código de aplicación personalizado que se comunique con componentes del visor interno.

Por ejemplo, si planea escuchar el evento `StatusEvent.NOTF_VIEW_READY` y el visor se suministra desde AEM, el tipo de evento completo es `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` y el código del detector de eventos es similar al siguiente:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var spinView = <instance>.getComponent("spinView"); 
   spinView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var spinView = <instance>.getComponent("spinView"); 
   spinView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
