---
description: nulo
seo-description: nulo
seo-title: Devoluciones de llamada de Evento
solution: Experience Manager
title: Devoluciones de llamada de Evento
topic: Dynamic media
uuid: d98074f1-7dd9-4a7f-9ef8-ebd47b698869
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

Consulte también [Visor flotante](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-.flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) y [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692).
