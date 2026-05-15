---
title: Compatibilidad con el seguimiento de Adobe Analytics
description: El visor de giros es compatible con el seguimiento de Adobe Analytics de forma predeterminada.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 30762700-6d69-4299-9492-57893232abe1
TQID: 'https://experienceleague.adobe.com/a9Ab9GwdXqTOrBLuKj49d5Jl01V2-iGH5xb1khFGH7g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# Compatibilidad con el seguimiento de Adobe Analytics{#support-for-adobe-analytics-tracking}

El visor de giros es compatible con el seguimiento de Adobe Analytics de forma predeterminada.

## Seguimiento listo para usar. {#section-d06145cfa2b9491bb485b599368d466e}

El visor de giros es compatible con el seguimiento de Adobe Analytics de forma predeterminada.

Para habilitar el seguimiento, pase el nombre del ajuste preestablecido de empresa adecuado como parámetro `config2`.

El visor también envía una única solicitud HTTP de seguimiento al servidor de imágenes configurado con el tipo de visor y la información de versión.

## Seguimiento personalizado {#section-47512156a1d64b338b50cfa39c84f4aa}

Para integrarse con sistemas de análisis de terceros, es necesario escuchar la llamada de retorno del visor `trackEvent` y procesar el argumento `eventInfo` de la función de llamada de retorno, según sea necesario. El siguiente código es un ejemplo de esta función de controlador:

```javascript {.line-numbers}
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
   <td colname="col2"> <p>se intercambia un recurso en el visor mediante la API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> se amplía una imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PANORÁMICA </span> </p> </td> 
   <td colname="col2"> <p>se panorámica una imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> GIRO </span> </p> </td> 
   <td colname="col2"> <p> se realiza un giro. </p> </td> 
  </tr> 
 </tbody> 
</table>
