---
description: Llamadas de retorno de eventos
solution: Experience Manager
title: Llamadas de retorno de eventos
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Developer,Business Practitioner
exl-id: 1a7b51c1-baa7-4ae3-b6b7-17478055a605
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
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

Consulte también [MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) y [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3).
