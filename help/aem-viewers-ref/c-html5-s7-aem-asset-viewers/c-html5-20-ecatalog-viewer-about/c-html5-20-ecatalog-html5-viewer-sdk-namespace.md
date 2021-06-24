---
description: Espacio de nombres del SDK del visor
solution: Experience Manager
title: Espacio de nombres del SDK del visor
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Developer,Business Practitioner
exl-id: c5286e1f-1f43-4cb8-b876-dc843f8112f5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Espacio de nombres del SDK del visor{#viewer-sdk-namespace}

El visor está integrado por muchos componentes del SDK de visor. En la mayoría de los casos, la página web no necesita interactuar directamente con la API de componentes del SDK; todas las necesidades comunes se cubren en la propia API del visor.

Sin embargo, algunos casos de uso avanzados requieren que la página web obtenga una referencia a un componente SDK interno mediante la API del visor `getComponent()` y, a continuación, utilice toda la flexibilidad de las API del propio SDK.

El espacio de nombres que utiliza el visor para cargar e inicializar componentes del SDK depende del entorno en el que funcione el visor. Si el visor se está ejecutando en AEM (Adobe Experience Manager), el visor carga los componentes del SDK en el espacio de nombres `s7viewers.s7sdk`. Y el visor servido desde Dynamic Media Classic carga el SDK en `s7classic.s7sdk`.

En cualquier caso, el espacio de nombres utilizado por el SDK dentro del visor tiene el prefijo `s7viewers` o `s7classic`. Además, es diferente del espacio de nombres simple `s7sdk` utilizado en la guía del usuario del SDK o en la documentación de la API del SDK.

Por este motivo, es importante utilizar un espacio de nombres del SDK totalmente cualificado al escribir código de aplicación personalizado que se comunique con componentes del visor interno.

Por ejemplo, si planea escuchar el evento `StatusEvent.NOTF_VIEW_READY` y el visor se suministra desde Dynamic Media Classic, el tipo de evento completo es `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY` y el código del detector de eventos es similar al siguiente:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
