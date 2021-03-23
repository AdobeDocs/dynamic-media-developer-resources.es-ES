---
description: Llamadas de retorno de eventos
solution: Experience Manager
title: Llamadas de retorno de eventos
uuid: 08756e93-2c6c-4c63-9dd0-c64531561d6f
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '157'
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

Consulte también [VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) y [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
