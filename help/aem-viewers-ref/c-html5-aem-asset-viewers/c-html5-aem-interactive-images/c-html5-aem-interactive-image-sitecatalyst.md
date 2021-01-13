---
description: Compatibilidad con el seguimiento de análisis
solution: Experience Manager
title: Compatibilidad con el seguimiento de análisis
topic: Dynamic media
uuid: ae870d2e-2a09-4551-935a-916d0e657653
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---


# Compatibilidad con el seguimiento de análisis{#support-for-analytics-tracking}

## Seguimiento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

De forma predeterminada, el visor envía una única solicitud HTTP de seguimiento al servidor de imágenes configurado con el tipo de visor y la información de versión.

Para integrarse con sistemas de análisis de terceros, es necesario escuchar la llamada de retorno del visor `trackEvent` y procesar el argumento `eventInfo` de la función de llamada de retorno según sea necesario. El siguiente código es un ejemplo de dicha función de controlador:

```
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

El visor realiza el seguimiento de los siguientes eventos de usuario del SDK:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>EVENTO del usuario del SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Enviado cuando... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>primero se carga el visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>el usuario activa la zona interactiva. </p> </td> 
  </tr> 
 </tbody> 
</table>

