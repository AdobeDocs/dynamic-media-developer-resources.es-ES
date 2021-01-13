---
description: Devoluciones de llamada de evento
solution: Experience Manager
title: Devoluciones de llamada de evento
topic: Dynamic media
uuid: 4a3dc8d7-2eb3-4244-849b-01d1314e43f2
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# Devoluciones de llamada de evento{#event-callbacks}

El visor admite llamadas de retorno de evento JavaScript que la página web utiliza para rastrear el proceso de inicialización del visor o el comportamiento en tiempo de ejecución.

Los controladores de llamada de retorno se asignan pasando nombres de evento y funciones de controlador correspondientes con la propiedad `handlers` al objeto JSON `config` en el constructor del visor. Como alternativa, es posible utilizar el método de API `setHandlers()`.

Los eventos de visor admitidos son los siguientes:

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evento de visor </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete  </span> </p> </td> 
   <td colname="col2"> <p>Déclencheur cuando se completa la inicialización del visor y se crean todos los componentes internos, de modo que es posible utilizar la API <span class="codeph"> getComponent() </span>. El controlador de llamada de retorno no toma ningún argumento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> Déclencheur cada vez que se produce un evento dentro del visor que puede ser gestionado por un sistema de seguimiento de evento, como Adobe Analytics. El controlador callback acepta los siguientes argumentos: </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String}  </span> - no se está utilizando. </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String}  </span> - no se utiliza actualmente. </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String}  </span> - nombre de instancia del componente SDK de visor que activó el evento. </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> timeStamp {Number}  </span> - Marca de hora de evento. </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String}  </span> - Carga útil de evento. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate  </span> </p> </td> 
   <td colname="col2"> <p> Déclencheur cuando el usuario activa un punto interactivo con los datos de Vista rápida asociados a él. El controlador callback toma el siguiente argumento: </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> data {Object}  </span> - un objeto JSON que contiene datos de la definición de zona interactiva. El campo <span class="codeph"> sku </span> es obligatorio, mientras que otros campos son opcionales y dependen de la definición del punto interactivo de origen. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte también [InteractiveImage](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-interactiveimage.md#reference-bd16cadc0c054fafb0db4994741d47cd) y [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
