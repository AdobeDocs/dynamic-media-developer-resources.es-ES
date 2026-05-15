---
title: Llamadas de retorno de eventos
description: Llamadas de retorno de eventos
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
TQID: 'https://experienceleague.adobe.com/pAXI43BvGyX7rM3--kuoLsAsexeM993-WKoLPCU9Zzg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 210
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
   * `instName {String}` un nombre de instancia del componente de visor de SDK que activó el evento.
   * `timeStamp {Number}` marca de tiempo del evento.
   * `eventInfo {String}` carga útil de evento.

* `quickViewActivate`: déclencheur cuando un usuario pulsa o hace clic en una muestra interactiva dentro del componente de muestras interactivas o en la pantalla &quot;call to action&quot; que se muestra al final de la reproducción de vídeo. El controlador de devolución de llamada toma el único argumento que es un objeto JSON con los siguientes campos:

   * Valor de SKU de `sku` { `String` asociado a la muestra interactiva.
   * `<additionalVariable>` { `String`} cero o más variables adicionales asociadas con la muestra interactiva.

Consulte también [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) y [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
