---
title: Llamadas de retorno de eventos
description: Llamadas de retorno de eventos
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 14b317ab-82fb-4f55-babe-72c24e6afc2c
source-git-commit: d5f1f05c36c1cb8a57b5a4bb8a9d066c20e32e75
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Llamadas de retorno de eventos{#event-callbacks}

El visor admite las llamadas de retorno de eventos de JavaScript que la página web utiliza para rastrear el proceso de inicialización del visor o el comportamiento en tiempo de ejecución.

Los controladores de devolución de llamada se asignan pasando nombres de evento y funciones de controlador correspondientes con la variable `handlers` propiedad a `config` objeto JSON en el constructor del visualizador. Alternativamente, es posible utilizar `setHandlers()` método de API.

Los eventos de visor admitidos son los siguientes:

* `initComplete` : déclencheur cuando se completa la inicialización del visor y se crean todos los componentes internos, de modo que sea posible utilizar `getComponent()` API. El controlador de llamada de retorno no toma ningún argumento.

* `trackEvent` : déclencheur cada vez que se produce un evento dentro del visualizador que puede ser gestionado por un sistema de seguimiento de eventos, como Adobe Analytics. El controlador de llamada de retorno toma los siguientes argumentos:

   * `objID {String}` no se usa actualmente.
   * `compClass {String}` no se usa actualmente.
   * `instName {String}` nombre de instancia del componente SDK del visor que activó el evento.
   * `timeStamp {Number}` marca de hora del evento.
   * `eventInfo {String}` carga útil de evento.

Consulte también [Visor de zoom básico](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) y [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9).
