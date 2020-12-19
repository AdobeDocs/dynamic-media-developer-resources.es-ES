---
description: Referencia de la API de JavaScript para el visor de medios mixtos.
seo-description: Referencia de la API de JavaScript para el visor de medios mixtos.
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 2477ec80-f627-48da-a66d-a86f17d7cc7d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---


# setHandlers{#sethandlers}

Referencia de la API de JavaScript para el visor de medios mixtos.

`setHandlers(handlers)`

Especifica cero o más controladores de llamada de retorno. Una llamada a este método sobrescribe por completo los controladores de evento asignados anteriormente para esa instancia de visor. Debe llamarse antes de `init()`.

## Parámetro {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> controladores  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Objeto {Object}  </span> JSON con rellamadas de evento de visor, donde el nombre de la propiedad es el nombre del evento del visor admitido y el valor de la propiedad es una referencia de función JavaScript a una rellamada adecuada. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> rellamadas de Evento </a> para obtener más información sobre los eventos del visor. </p> </td> 
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

