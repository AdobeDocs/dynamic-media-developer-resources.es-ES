---
title: Llamadas de retorno de eventos
description: Llamadas de retorno de eventos
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 24ea35c0-a0b1-4768-9336-94eb5e2d4fb2
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Llamadas de retorno de eventos{#event-callbacks}

El visor admite llamadas de retorno de eventos de JavaScript que la página web utiliza para rastrear el proceso de inicialización del visor o el comportamiento en tiempo de ejecución.

Los controladores de devolución de llamada se asignan pasando nombres de evento y funciones de controlador correspondientes con la propiedad `handlers` al objeto JSON `config` en el constructor del visor. Como alternativa, es posible utilizar el método de API `setHandlers()`.

Los eventos de visor admitidos son los siguientes:

* `initComplete`: déclencheur cuando se completa la inicialización del visor y se crean todos los componentes internos, de modo que sea posible utilizar la API `getComponent()`. El controlador de devolución de llamada no toma ningún argumento.
* `trackEvent`: déclencheur cada vez que se produce un evento dentro del visor que puede administrar un sistema de seguimiento de eventos, como Adobe Analytics. El controlador de devolución de llamada toma los siguientes argumentos:

   * `objID {String}` no se usa actualmente.
   * `compClass {String}` no se usa actualmente.
   * `instName {String}` un nombre de instancia del componente SDK del visor de HTML5 que activó el evento.
   * `timeStamp {Number}` marca de tiempo del evento.
   * `eventInfo {String}` carga útil de evento.

Consulte también [Video360Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-video360viewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) y [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
