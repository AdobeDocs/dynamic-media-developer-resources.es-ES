---
description: Llamadas de retorno de eventos
solution: Experience Manager
title: Llamadas de retorno de eventos
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Developer,Business Practitioner
exl-id: 7bd2e167-d04c-43e2-a71c-e2b3dddb13a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Llamadas de retorno de eventos{#event-callbacks}

El visor admite las llamadas de retorno de eventos de JavaScript que la página web utiliza para rastrear el proceso de inicialización del visor o el comportamiento en tiempo de ejecución.

Los controladores de devolución de llamada se asignan pasando nombres de evento y funciones de controlador correspondientes con la propiedad `handlers` al objeto JSON `config` en el constructor del visor. Como alternativa, es posible utilizar el método de API `setHandlers()`.

Los eventos de visor admitidos son los siguientes:

* `initComplete` : déclencheur cuando se completa la inicialización del visor y se crean todos los componentes internos, de modo que sea posible utilizar la  `getComponent()` API. El controlador de llamada de retorno no toma ningún argumento.

* `trackEvent` : déclencheur cada vez que se produce un evento dentro del visualizador que puede ser gestionado por un sistema de seguimiento de eventos, como Adobe Analytics. El controlador de llamada de retorno toma los siguientes argumentos:

   * `objID {String}` no se usa actualmente.
   * `compClass {String}` no se usa actualmente.
   * `instName {String}` nombre de instancia del componente SDK del visor que activó el evento.
   * `timeStamp {Number}` marca de hora del evento.
   * `eventInfo {String}` carga útil de evento.

Consulte también [eCatalogViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-ecatalogviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) y [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856).
