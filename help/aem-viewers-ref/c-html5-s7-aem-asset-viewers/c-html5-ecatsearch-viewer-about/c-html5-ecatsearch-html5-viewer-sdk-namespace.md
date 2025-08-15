---
description: Área de nombres de SDK de visor
solution: Experience Manager
title: Área de nombres de SDK de visor
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Área de nombres de SDK de visor{#viewer-sdk-namespace}

El visor está formado por muchos componentes de Viewer SDK. En la mayoría de los casos, la página web no necesita interactuar directamente con la API de componentes de SDK; todas las necesidades comunes se cubren en la propia API de visor.

Sin embargo, algunos casos de uso avanzados requieren que la página web obtenga una referencia a un componente interno de SDK mediante la API de visor `getComponent()` y, a continuación, utilice toda la flexibilidad de las API de SDK.

El área de nombres que el usuario utiliza para cargar e inicializar los componentes de SDK depende del entorno en el que funcione el usuario. Si el visor se está ejecutando en AEM (Adobe Experience Manager), cargará componentes de SDK en el espacio de nombres `s7viewers.s7sdk`. Y el visor servido desde Dynamic Media Classic carga el SDK en `s7classic.s7sdk`.

En cualquier caso, el espacio de nombres utilizado por SDK dentro del visor tiene `s7viewers` o `s7classic` como prefijo. Además, es diferente del área de nombres `s7sdk` sin formato que se usa en la Guía del usuario de SDK o en la documentación de la API de SDK.

Por este motivo, es importante utilizar un área de nombres de SDK completa al escribir código de aplicación personalizado que se comunique con componentes del visor interno.

Por ejemplo, si planea escuchar el evento `StatusEvent.NOTF_VIEW_READY` y el visor se proporciona desde Dynamic Media Classic, el tipo de evento completo es `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY` y el código del detector de eventos tiene un aspecto similar al siguiente:

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
