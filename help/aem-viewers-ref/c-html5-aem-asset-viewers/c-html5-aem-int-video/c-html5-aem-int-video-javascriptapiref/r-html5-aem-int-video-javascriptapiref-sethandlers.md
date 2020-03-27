---
description: Referencia de la API de JavaScript para el visor de vídeo interactivo
seo-description: Referencia de la API de JavaScript para el visor de vídeo interactivo
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: f33df5a9-e323-4dff-b792-88d778332c75
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setHandlers{#sethandlers}

Referencia de la API de JavaScript para el visor de vídeo interactivo

`setHandlers(handlers)`

Especifica cero o más controladores de llamada de retorno. Una llamada a este método sobrescribe por completo los controladores de evento asignados anteriormente para esa instancia de visor. Debe llamarse antes `init()`.

## Parámetro {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> controladores </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto JSON con rellamadas de retorno de evento de visor, donde el nombre de propiedad es el nombre del evento de visor admitido y el valor de propiedad es una referencia de función JavaScript a una rellamada adecuada. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Devoluciones de llamada de Evento </a> para obtener más información sobre los eventos del visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

