---
title: Llamadas de retorno de eventos
description: Llamadas de retorno de eventos
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '210'
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

* `quickViewActivate` : déclencheur cuando un usuario hace clic o pulsa una muestra interactiva dentro del componente de muestras interactivas o en la pantalla &quot;llamada a la acción&quot; que se muestra al final de la reproducción de vídeo. El controlador de devolución de llamada toma el único argumento que es un objeto JSON con los siguientes campos:

   * `sku` { `String`} valor de SKU que está asociado con la muestra interactiva.
   * `<additionalVariable>` { `String`} cero o más variables adicionales asociadas con la muestra interactiva.

Consulte también [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) y [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
