---
description: Referencia de la API de JavaScript para el visor de imágenes de vídeo
seo-description: Referencia de la API de JavaScript para el visor de imágenes de vídeo
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 93db9c88-890e-4be8-b82f-d15978a0cfac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setHandlers{#sethandlers}

Referencia de la API de JavaScript para el visor de imágenes de vídeo

`setHandlers(handlers)`

Especifica cero o más controladores de llamada de retorno. Una llamada a este método sobrescribe por completo los controladores de evento asignados anteriormente para esa instancia de visor. Debe llamarse antes `init()`.

## Parámetro {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> controladores </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto JSON con rellamadas de evento de visor. El nombre de la propiedad es el nombre del evento del visor admitido. El valor de propiedad es una referencia de función JavaScript a una llamada de retorno adecuada. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Devoluciones de llamada de Evento </a> para obtener más información sobre los eventos del visor. </p> </td> 
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

