---
title: setHandlers
description: Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 37d14494-cdb2-45f7-96e2-d7a9e90edad3
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 3%

---

# setHandlers{#sethandlers}

Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente.

`setHandlers(handlers)`

Especifica cero o más controladores de devolución de llamada. Una llamada a este método sobrescribe completamente los controladores de eventos que se asignaron anteriormente a esa instancia de visor. Debe llamarse antes de `init()`.

## Parámetro {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> controladores </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> El objeto JSON con llamadas de retorno de eventos del visor, donde el nombre de la propiedad es el nombre del evento del visor admitido y el valor de la propiedad es una referencia de función JavaScript a una llamada de retorno adecuada. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> Llamadas de retorno de eventos </a> para obtener más información sobre los eventos del visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```
