---
description: Área de nombres del SDK del visor
solution: Experience Manager
title: Área de nombres del SDK del visor
topic: Dynamic media
uuid: 29987da2-4535-47f3-a5ae-912c7cd10c86
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# Área de nombres del SDK del visor{#viewer-sdk-namespace}

El visor está integrado por varios componentes del SDK de visor. En la mayoría de los casos, la página web no necesita interactuar directamente con la API de componentes del SDK; todas las necesidades comunes se cubren en la propia API del visor.

Sin embargo, algunos casos de uso avanzados requieren que la página web obtenga una referencia a un componente de SDK interno mediante la API de visor `getComponent()` y, a continuación, utilice toda la flexibilidad de las API del propio SDK.

La Área de nombres que el visor utiliza para cargar e inicializar los componentes del SDK depende del entorno en el que funciona el visor. Si el visor se está ejecutando en AEM (Adobe Experience Manager), el visor carga los componentes del SDK en la Área de nombres `s7viewers.s7sdk`. Del mismo modo, el visor que se proporciona desde Scene7 Publishing System carga el SDK en `s7classic.s7sdk`.

En cualquier caso, la Área de nombres utilizada por el SDK dentro del visor tiene el prefijo `s7viewers` o `s7classic`. Además, es diferente de la Área de nombres `s7sdk` sin formato utilizada en la Guía del usuario del SDK o en la documentación de la API del SDK. Por este motivo, es importante utilizar una Área de nombres de SDK totalmente cualificada al escribir código de aplicación personalizado que se comunique con los componentes del visor interno.

Por ejemplo, si planea escuchar el evento `StatusEvent.NOTF_VIEW_READY` y el visor se suministra desde AEM, el tipo de evento completo será `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` y el código del oyente de evento será similar al siguiente:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Scene7 Publishing System will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

