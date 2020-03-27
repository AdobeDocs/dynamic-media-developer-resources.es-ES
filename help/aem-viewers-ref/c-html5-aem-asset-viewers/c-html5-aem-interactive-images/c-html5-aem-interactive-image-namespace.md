---
description: nulo
seo-description: nulo
seo-title: Área de nombres del SDK del visor
solution: Experience Manager
title: Área de nombres del SDK del visor
topic: Dynamic media
uuid: e1639806-3052-4913-aae0-ca9a79100d0f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Área de nombres del SDK del visor{#viewer-sdk-namespace}

El visor está integrado por varios componentes del SDK de visor. En la mayoría de los casos, la página web no necesita interactuar directamente con la API de componentes del SDK; todas las necesidades comunes se cubren en la propia API del visor.

Sin embargo, algunos casos de uso avanzados requieren que la página web obtenga una referencia a un componente del SDK interno mediante la API del `getComponent()` visor y, a continuación, utilice toda la flexibilidad de las propias API del SDK.

La Área de nombres que el visor utiliza para cargar e inicializar los componentes del SDK depende del entorno en el que funciona el visor. Si el visor se está ejecutando en AEM (Adobe Experience Manager), el visor carga los componentes del SDK en la `s7viewers.s7sdk` Área de nombres. Y el visor que se proporciona desde Scene7 Publishing System carga el SDK en `s7classic.s7sdk`.

En cualquier caso, la Área de nombres utilizada por el SDK dentro del visor tiene `s7viewers` o `s7classic` el prefijo . Además, es diferente de la `s7sdk` Área de nombres simple utilizada en la Guía del usuario del SDK o en la documentación de la API del SDK.

Por este motivo, es importante utilizar una Área de nombres de SDK totalmente cualificada al escribir código de aplicación personalizado que se comunique con los componentes del visor interno.

Por ejemplo, si planea escuchar `StatusEvent.NOTF_VIEW_READY` evento y el visor se suministra desde AEM, el tipo de evento completo es `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`y el código de escucha de evento es similar al siguiente:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

