---
title: Llamadas de retorno de eventos
description: Llamadas de retorno de eventos
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c54c54ae-f98f-4cd4-8c36-c7e2a9f3c6df
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Llamadas de retorno de eventos{#event-callbacks}

El visor admite llamadas de retorno de eventos JavaScript que la página web utiliza para rastrear el proceso de inicialización del visor o el comportamiento del tiempo de ejecución.

Los controladores de llamada de retorno se asignan pasando nombres de evento y funciones de controlador correspondientes con el `handlers` propiedad a `config` Objeto JSON en el constructor del visor. Alternativamente, es posible utilizar `setHandlers()` Método de API.

Los eventos de visor admitidos son los siguientes:

* `initComplete` : déclencheur cuando se completa la inicialización del visor y se crean todos los componentes internos, de modo que es posible utilizar `getComponent()` API. El controlador de devolución de llamada no toma ningún argumento.

* `trackEvent` : déclencheur cada vez que se produce un evento dentro del visor, que puede gestionar un sistema de seguimiento de eventos, como Adobe Analytics. El controlador de devolución de llamada toma los siguientes argumentos:

   * `objID {String}` no se utiliza actualmente.
   * `compClass {String}` no se utiliza actualmente.
   * `instName {String}` un nombre de instancia del componente SDK de visor que activó el evento.
   * `timeStamp {Number}` marca de tiempo del evento.
   * `eventInfo {String}` carga útil de evento.

Consulte también [FlyoutViewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-.flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) y [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692).
