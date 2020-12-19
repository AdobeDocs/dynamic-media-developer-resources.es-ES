---
description: nulo
seo-description: nulo
seo-title: Devoluciones de llamada de evento
solution: Experience Manager
title: Devoluciones de llamada de evento
topic: Dynamic media
uuid: b9252d4b-cff1-42eb-9e56-553091f854b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Devoluciones de llamada de evento{#event-callbacks}

El visor admite llamadas de retorno de evento JavaScript que la página web utiliza para rastrear el proceso de inicialización del visor o el comportamiento en tiempo de ejecución.

Los controladores de llamada de retorno se asignan pasando nombres de evento y funciones de controlador correspondientes con la propiedad `handlers` al objeto JSON `config` en el constructor del visor. Como alternativa, es posible utilizar el método de API `setHandlers()`.

Los eventos de visor admitidos son los siguientes:

* `initComplete` - se activa cuando se completa la inicialización del visor y se crean todos los componentes internos, de modo que es posible utilizar  `getComponent()` API. El controlador de llamada de retorno no toma ningún argumento.
* `trackEvent` - se desencadena cada vez que se produce un evento dentro del visor que puede ser gestionado por un sistema de seguimiento de evento, como Adobe Analytics. El controlador callback toma los siguientes argumentos:

   * `objID {String}` no se está utilizando actualmente.
   * `compClass {String}` no se está utilizando actualmente.
   * `instName {String}` nombre de instancia del componente SDK de visor que activó el evento.
   * `timeStamp {Number}` Marca de hora de evento.
   * `eventInfo {String}` Carga útil de evento.

* `quickViewActivate` - se activa cuando un usuario hace clic o toca una muestra interactiva dentro del componente de muestras interactivas o en la pantalla de llamada a la acción que se muestra al final de la reproducción de vídeo. El controlador de llamada de retorno toma el único argumento que es un objeto JSON con los siguientes campos:

   * `sku` { `String`} valor de SKU asociado a la muestra interactiva.
   * `<additionalVariable>` { `String`} cero o más variables adicionales asociadas con la muestra interactiva.

Consulte también [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) y [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
