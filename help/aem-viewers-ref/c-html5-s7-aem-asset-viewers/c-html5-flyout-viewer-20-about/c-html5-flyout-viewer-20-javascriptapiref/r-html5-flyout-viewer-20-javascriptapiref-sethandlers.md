---
title: setHandlers
description: Referencia de la API de JavaScript para el visor flotante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 3a7b2aeb-2de5-4d4c-8974-47b6418140e6
TQID: 'https://experienceleague.adobe.com/8c3rfrLYrPTG5CdAjFod6lnUDRnMq6zzXsDSXztwirQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 3%

---

# setHandlers{#sethandlers}

Referencia de la API de JavaScript para el visor flotante.

`setHandlers(handlers)`

Especifica cero o más controladores de devolución de llamada. Una llamada a este método sobrescribe completamente los controladores de eventos asignados anteriormente para esa instancia de visor. Se debe llamar antes de `init()`.

## Parámetro {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> controladores </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto JSON con llamadas de retorno de evento del visor, donde el nombre de propiedad es el nombre del evento del visor admitido y el valor de propiedad es una referencia de función de JavaScript a una llamada de retorno adecuada. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> devoluciones de llamadas de evento </a> para obtener más información sobre los eventos de visor. </p> </td> 
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
