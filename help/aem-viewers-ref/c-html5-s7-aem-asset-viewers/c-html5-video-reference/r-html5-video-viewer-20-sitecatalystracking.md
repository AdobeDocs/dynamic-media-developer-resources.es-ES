---
description: El visor de vídeo es compatible con el seguimiento de Adobe Analytics de serie.
solution: Experience Manager
title: Compatibilidad con el seguimiento de Adobe Analytics
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial, ingeniero de datos, arquitecto de datos
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 3%

---


# Compatibilidad con el seguimiento de Adobe Analytics{#support-for-adobe-analytics-tracking}

El visor de vídeo es compatible con el seguimiento de Adobe Analytics de serie.

## Seguimiento predeterminado {#section-3b101fe30be943c1b679fd5c273569ca}

El visor de vídeo es compatible con el seguimiento de Adobe Analytics de serie.

Para habilitar el seguimiento, pase el nombre de ajuste preestablecido de empresa adecuado como parámetro `config2`.

El visor también envía una única solicitud HTTP de seguimiento al servidor de imágenes configurado con el tipo de visor y la información de versión.

## Seguimiento personalizado {#section-ab10bd7caf184721a366cf3953071934}

Para integrarse con sistemas de análisis de terceros, es necesario escuchar la llamada de retorno del visor `trackEvent` y procesar el argumento `eventInfo` de la función de llamada de retorno según sea necesario. El siguiente código es un ejemplo de dicha función de controlador:

```
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
   <td colname="col2"> <p>un recurso se intercambia en el visor mediante la API <span class="codeph"> setAsset() </span>. </p> </td> 
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

