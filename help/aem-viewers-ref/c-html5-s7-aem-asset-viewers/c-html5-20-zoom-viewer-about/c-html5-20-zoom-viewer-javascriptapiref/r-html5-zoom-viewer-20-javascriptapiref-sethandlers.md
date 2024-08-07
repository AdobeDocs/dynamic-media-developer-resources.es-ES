---
title: setHandlers
description: Referencia de la API de JavaScript para el visor de vídeo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: cff331a9-bca1-4360-88fa-96812aa8ba62
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 3%

---

# setHandlers{#sethandlers}

Referencia de la API de JavaScript para el visor de vídeo

`setHandlers(handlers)`

Especifica cero o más controladores de devolución de llamada. Una llamada a este método sobrescribe completamente los controladores de eventos asignados anteriormente para esa instancia de visor. Se debe llamar antes de `init()`.

## Parámetro {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> controladores </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto JSON con llamadas de retorno de evento del visor, donde el nombre de propiedad es el nombre del evento del visor admitido y el valor de propiedad es una referencia de función de JavaScript a una llamada de retorno adecuada. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> devoluciones de llamadas de evento </a> para obtener más información sobre los eventos de visor. </p> </td> 
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
