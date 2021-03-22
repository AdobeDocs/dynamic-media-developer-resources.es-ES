---
description: Referencia de la API de JavaScript para el visualizador de giros
seo-description: Referencia de la API de JavaScript para el visualizador de giros
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
uuid: 50db47ee-c1bb-4e45-bfcf-fae0fff6e0e8
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---


# setHandlers{#sethandlers}

Referencia de la API de JavaScript para el visualizador de giros

`setHandlers(handlers)`

Especifica cero o más controladores de devolución de llamada. Una llamada a este método sobrescribe completamente los controladores de eventos que se asignaron anteriormente a esa instancia de visor. Debe llamarse antes de `init()`.

## Parámetro {#section-51f820ded5e842bebd123e37a35176c7}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> controladores  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} objeto  </span> JSON con llamadas de retorno de eventos del visor, donde el nombre de la propiedad es el nombre del evento del visor admitido y el valor de la propiedad es una referencia de función JavaScript a una llamada de retorno adecuada. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> Llamadas de retorno de eventos </a> para obtener más información sobre los eventos del visor. </p> </td> 
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

