---
description: Compatibilidad con el seguimiento de análisis
solution: Experience Manager
title: Compatibilidad con el seguimiento de análisis
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Developer,User,Data Engineer,Data Architect
exl-id: 17e8937f-e328-46a4-b7d9-1fd39ab2e8bd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
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

El visor realiza el seguimiento de los siguientes eventos de usuario de SDK:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evento de usuario del SDK </p> </th> 
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
