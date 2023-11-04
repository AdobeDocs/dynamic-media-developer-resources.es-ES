---
description: Espacio de nombres del SDK de visor
solution: Experience Manager
title: Espacio de nombres del SDK de visor
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Espacio de nombres del SDK de visor{#viewer-sdk-namespace}

El visor está formado por muchos componentes del SDK del visor. En la mayoría de los casos, la página web no necesita interactuar directamente con la API de componentes del SDK; todas las necesidades comunes se cubren en la propia API de visor.

Sin embargo, algunos casos de uso avanzados requieren que la página web obtenga una referencia a un componente de SDK interno mediante la variable `getComponent()` y, a continuación, utilice toda la flexibilidad de las API del propio SDK.

El área de nombres que utiliza el visor para cargar e inicializar los componentes del SDK depende del entorno en el que opera el visor. AEM Si el visor se está ejecutando en la (Adobe Experience Manager), carga componentes del SDK en `s7viewers.s7sdk` namespace. Y el visor servido desde Dynamic Media Classic carga el SDK en `s7classic.s7sdk`.

En cualquier caso, el área de nombres utilizada por el SDK dentro del visor tiene `s7viewers` o `s7classic` como prefijo. Y, es diferente de la llanura `s7sdk` espacio de nombres utilizado en la Guía del usuario de SDK o en la documentación de la API de SDK.

Por este motivo, es importante utilizar un área de nombres de SDK completa al escribir código de aplicación personalizado que se comunique con componentes del visor interno.

Por ejemplo, si planea escuchar a `StatusEvent.NOTF_VIEW_READY` y el visor se proporciona desde Dynamic Media Classic, el tipo de evento completo es `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`y el código del detector de eventos tiene un aspecto similar al siguiente:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
