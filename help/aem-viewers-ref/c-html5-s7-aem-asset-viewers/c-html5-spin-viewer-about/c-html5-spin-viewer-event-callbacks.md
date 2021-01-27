---
description: Devoluciones de llamada de evento
solution: Experience Manager
title: Devoluciones de llamada de evento
topic: Dynamic Media
uuid: 512f5c08-cf6a-4721-a169-11977cd4c248
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Devoluciones de llamada de evento{#event-callbacks}

El visor admite llamadas de retorno de evento JavaScript que la página web utiliza para rastrear el proceso de inicialización del visor o el comportamiento en tiempo de ejecución.

Los controladores de llamada de retorno se asignan pasando nombres de evento y funciones de controlador correspondientes con la propiedad `handlers` al objeto JSON `config` en el constructor del visor. Como alternativa, es posible utilizar el método de API `setHandlers()`.

Los eventos de visor admitidos son los siguientes:

* `initComplete` - déclencheur cuando se completa la inicialización del visor y se crean todos los componentes internos, para que sea posible utilizar  `getComponent()` API. El controlador de llamada de retorno no toma ningún argumento.

* `trackEvent` - déclencheur cada vez que se produce un evento dentro del visor que puede ser gestionado por un sistema de seguimiento de evento, como Adobe Analytics. El controlador callback toma los siguientes argumentos:

   * `objID {String}` no se está utilizando actualmente.
   * `compClass {String}` no se está utilizando actualmente.
   * `instName {String}` nombre de instancia del componente SDK de visor que activó el evento.
   * `timeStamp {Number}` Marca de hora de evento.
   * `eventInfo {String}` Carga útil de evento.

Consulte también [SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) y [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef).
