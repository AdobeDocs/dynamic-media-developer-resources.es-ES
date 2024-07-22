---
title: Compatibilidad con el seguimiento de Adobe Analytics
description: El Visor de vídeo admite el seguimiento de Adobe Analytics de forma predeterminada.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Compatibilidad con el seguimiento de Adobe Analytics{#support-for-adobe-analytics-tracking}

El Visor de vídeo admite el seguimiento de Adobe Analytics de forma predeterminada.

## Seguimiento listo para usar. {#section-3b101fe30be943c1b679fd5c273569ca}

El Visor de vídeo admite el seguimiento de Adobe Analytics de forma predeterminada.

Para habilitar el seguimiento, pase el nombre del ajuste preestablecido de empresa adecuado como parámetro `config2`.

El visor también envía una única solicitud HTTP de seguimiento al servidor de imágenes configurado con el tipo de visor y la información de versión.

## Seguimiento personalizado {#section-ab10bd7caf184721a366cf3953071934}

Para integrarse con sistemas de análisis de terceros, es necesario escuchar la llamada de retorno del visor `trackEvent` y procesar el argumento `eventInfo` de la función de llamada de retorno según sea necesario. El siguiente código es un ejemplo de esta función de controlador:

```javascript {.line-numbers}
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
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

El visor realiza un seguimiento de los siguientes eventos de usuarios del SDK:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evento de usuario del SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Se envía cuando... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CARGAR </span> </p> </td> 
   <td colname="col2"> <p>El visor se carga primero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> INTERCAMBIAR </span> </p> </td> 
   <td colname="col2"> <p>se intercambia un recurso en el visor mediante la API setAsset() </span> de <span class="codeph">. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> REPRODUCIR </span> </p> </td> 
   <td colname="col2"> <p>Se inicia la reproducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSAR </span> </p> </td> 
   <td colname="col2"> <p>la reproducción se detiene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DETENER </span> </p> </td> 
   <td colname="col2"> <p>la reproducción se ha detenido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HITO </span> </p> </td> 
   <td colname="col2"> <p>La reproducción de alcanza uno de los siguientes hitos: 0 %, 25 %, 50 %, 75 % y 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>
