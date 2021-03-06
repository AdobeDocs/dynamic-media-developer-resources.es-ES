---
title: Compatibilidad con el seguimiento de Adobe Analytics
description: El visor de vídeos de recorte inteligente es compatible con el seguimiento de Adobe Analytics listo para usar.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 0d91ca94-79fc-40de-8095-0252688ebe76
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# Compatibilidad con el seguimiento de Adobe Analytics{#support-for-adobe-analytics-tracking}

El visor de vídeos de recorte inteligente es compatible con el seguimiento de Adobe Analytics listo para usar.

## Seguimiento predeterminado {#section-3b101fe30be943c1b679fd5c273569ca}

El visor de vídeos de recorte inteligente es compatible con el seguimiento de Adobe Analytics listo para usar.

Para habilitar el seguimiento, pase el nombre de ajuste preestablecido de la empresa correspondiente como `config2` parámetro.

El visor también envía una única solicitud HTTP de seguimiento al servidor de imágenes configurado con el tipo de visor y la información de versión.

## Seguimiento personalizado {#section-ab10bd7caf184721a366cf3953071934}

Para integrarse con sistemas de análisis de terceros, es necesario escuchar `trackEvent` llamada de retorno y proceso del visor `eventInfo` de la función de llamada de retorno según sea necesario. El siguiente código es un ejemplo de dicha función de controlador:

```javascript {.line-numbers}
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>un recurso se intercambia en el visor mediante <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>se inicia la reproducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>la reproducción está en pausa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>se detiene la reproducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>la reproducción llega a uno de los siguientes molinos: 0 %, 25 %, 50 %, 75 % y 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>
