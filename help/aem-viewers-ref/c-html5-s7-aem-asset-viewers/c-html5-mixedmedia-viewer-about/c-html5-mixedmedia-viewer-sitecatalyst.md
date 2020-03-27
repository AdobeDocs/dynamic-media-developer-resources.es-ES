---
description: El visor de medios mixtos admite el seguimiento de Adobe Analytics de forma predeterminada.
seo-description: El visor de medios mixtos admite el seguimiento de Adobe Analytics de forma predeterminada.
seo-title: Compatibilidad con el seguimiento de Adobe Analytics
solution: Experience Manager
title: Compatibilidad con el seguimiento de Adobe Analytics
topic: Dynamic media
uuid: ad4dfed6-121f-4adb-bbdb-db6e6ee5672d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Compatibilidad con el seguimiento de Adobe Analytics{#support-for-adobe-analytics-tracking}

El visor de medios mixtos admite el seguimiento de Adobe Analytics de forma predeterminada.

## Seguimiento predeterminado {#section-ba994f079d0343c8ae48adffaa3195a3}

El visor de medios mixtos admite [!DNL Adobe Analytics] el seguimiento predeterminado. Para habilitar el seguimiento, pase el nombre de ajuste preestablecido de compañía correcto como `config2` parámetro.

El visor también envía una única solicitud HTTP de seguimiento al servidor de imágenes configurado con el tipo de visor y la información de versión.

## Seguimiento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Para integrarse con sistemas de análisis de terceros, es necesario escuchar la llamada de retorno del `trackEvent` visor y procesar el argumento `eventInfo` de la función de llamada de retorno según sea necesario. El siguiente código es un ejemplo de dicha función de controlador:

```
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
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

El visor realiza el seguimiento de los siguientes eventos de usuario del SDK:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>evento del usuario del SDK </p> </th> 
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
   <td colname="col2"> <p>un recurso se intercambia en el visor mediante la <span class="codeph"> API setAsset() </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>se amplía una imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>una imagen está panorámica. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> para cambiar una imagen, toque o haga clic en una muestra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>se ha iniciado la reproducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>la reproducción está en pausa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>la reproducción se detiene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>la reproducción llega a uno de los siguientes cálculos: 0 %, 25 %, 50 %, 75 % y 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPIN </span> </p> </td> 
   <td colname="col2"> <p>se realiza un giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

