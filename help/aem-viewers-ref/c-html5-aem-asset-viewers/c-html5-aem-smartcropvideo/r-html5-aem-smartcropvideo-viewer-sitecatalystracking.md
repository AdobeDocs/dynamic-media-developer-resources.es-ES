---
title: Compatibilidad con el seguimiento de Adobe Analytics
description: El Visor de recorte inteligente de vídeos admite el seguimiento de Adobe Analytics de forma predeterminada.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0d91ca94-79fc-40de-8095-0252688ebe76
TQID: 'https://experienceleague.adobe.com/qxJCNOQ6B6iYDi7JRepZfc9gMaF4Wn50DoPYWnTsq5Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%
---
# Compatibilidad con el seguimiento de Adobe Analytics{#support-for-adobe-analytics-tracking}

El Visor de recorte inteligente de vídeos admite el seguimiento de Adobe Analytics de forma predeterminada.

## Seguimiento listo para usar. {#section-3b101fe30be943c1b679fd5c273569ca}

El Visor de recorte inteligente de vídeos admite el seguimiento de Adobe Analytics de forma predeterminada.

Para habilitar el seguimiento, pase el nombre del ajuste preestablecido de empresa adecuado como parámetro `config2`.

El visor también envía una única solicitud HTTP de seguimiento al servidor de imágenes configurado con el tipo de visor y la información de versión.

## Seguimiento personalizado {#section-ab10bd7caf184721a366cf3953071934}

Para integrarse con sistemas de análisis de terceros, es necesario escuchar la llamada de retorno del visor `trackEvent` y procesar el argumento `eventInfo` de la función de llamada de retorno según sea necesario. El siguiente código es un ejemplo de esta función de controlador:

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

El visor realiza un seguimiento de los siguientes eventos de usuarios de SDK:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evento de usuario de SDK </p> </th> 
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
