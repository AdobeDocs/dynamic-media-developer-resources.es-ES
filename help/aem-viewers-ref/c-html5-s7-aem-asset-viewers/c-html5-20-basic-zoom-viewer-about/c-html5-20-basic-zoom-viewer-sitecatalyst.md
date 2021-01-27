---
description: El visor de zoom básico admite el seguimiento de Adobe Analytics de forma predeterminada.
seo-description: El visor de zoom básico admite el seguimiento de Adobe Analytics de forma predeterminada.
seo-title: Compatibilidad con el seguimiento de Adobe Analytics
solution: Experience Manager
title: Compatibilidad con el seguimiento de Adobe Analytics
topic: Dynamic Media
uuid: f48fde77-7e48-4d56-b5c5-079a484e6d9c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# Compatibilidad con el seguimiento de Adobe Analytics{#support-for-adobe-analytics-tracking}

El visor de zoom básico admite el seguimiento de Adobe Analytics de forma predeterminada.

## Seguimiento predeterminado {#section-ba994f079d0343c8ae48adffaa3195a3}

El visor de zoom básico admite el seguimiento [!DNL Adobe Analytics] listo para usar. Para habilitar el seguimiento, pase el nombre de ajuste preestablecido de compañía correcto como parámetro `config2`.

El visor también envía una única solicitud HTTP de seguimiento al servidor de imágenes configurado con el tipo de visor y la información de versión.

## Seguimiento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Para integrarse con sistemas de análisis de terceros, es necesario escuchar la rellamada del visor `trackEvent` y procesar el argumento `eventInfo` de la función de rellamada según sea necesario. El siguiente código es un ejemplo de dicha función de controlador:

```
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
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
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>un recurso se intercambia en el visor mediante la API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> se amplía una imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>una imagen está panorámica. </p> </td> 
  </tr> 
 </tbody> 
</table>

