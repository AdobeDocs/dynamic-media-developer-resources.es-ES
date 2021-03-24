---
description: Llamadas de retorno de eventos
solution: Experience Manager
title: Llamadas de retorno de eventos
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '160'
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
   * `instName {String}` nombre de instancia del componente SDK del visor HTML5 que activó el evento.
   * `timeStamp {Number}` marca de hora del evento.
   * `eventInfo {String}` carga útil de evento.

Consulte también [Video360Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-video360viewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) y [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
