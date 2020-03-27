---
description: nulo
seo-description: nulo
seo-title: Devoluciones de llamada de Evento
solution: Experience Manager
title: Devoluciones de llamada de Evento
topic: Dynamic media
uuid: 696838d2-11e4-4ef8-9cd3-136c5d5f6ed9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Devoluciones de llamada de Evento{#event-callbacks}

El visor admite llamadas de retorno de evento JavaScript que la página web utiliza para rastrear el proceso de inicialización del visor o el comportamiento en tiempo de ejecución.

Los controladores de llamada de retorno se asignan pasando nombres de evento y funciones de controlador correspondientes con la `handlers` propiedad al objeto `config` JSON en el constructor del visor. Como alternativa, es posible utilizar el método `setHandlers()` API.

Los eventos de visor admitidos son los siguientes:

* `initComplete` - se activa cuando se completa la inicialización del visor y se crean todos los componentes internos, de modo que es posible utilizar `getComponent()` API. El controlador de llamada de retorno no toma ningún argumento.

* `trackEvent` - se desencadena cada vez que se produce un evento en el visor que puede ser gestionado por un sistema de seguimiento de evento, como Adobe Analytics. El controlador callback toma los siguientes argumentos:

   * `objID {String}` no se está utilizando actualmente.
   * `compClass {String}` no se está utilizando actualmente.
   * `instName {String}` nombre de instancia del componente SDK de visor que activó el evento.
   * `timeStamp {Number}` Marca de hora de evento.
   * `eventInfo {String}` Carga útil de evento.

Consulte también [MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) y [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3).
