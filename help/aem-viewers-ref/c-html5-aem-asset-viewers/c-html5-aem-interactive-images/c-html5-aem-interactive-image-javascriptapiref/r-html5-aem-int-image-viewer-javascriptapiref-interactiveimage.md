---
title: InteractiveImage
description: Referencia de la API de JavaScript para el visualizador de imágenes de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 165de14f-0031-4969-9671-5da310d44c28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 3%

---

# InteractiveImage{#interactiveimage}

Referencia de la API de JavaScript para el visualizador de imágenes de vídeo.

`InteractiveImage([config])`

, crea una instancia del Visor de imágenes de vídeo.

## Parámetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configuración </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> objeto de configuración JSON opcional, permite que toda la configuración del visor pase al constructor para evitar llamar a métodos de establecedor individuales. Contiene las siguientes propiedades: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID del contenedor DOM (normalmente un DIV <span class="codeph"> de </span>) en el que se inserta el visor. Para el momento en que se llama a este método, no es necesario tener creado el elemento contenedor. Sin embargo, el contenedor debe existir cuando se ejecute <span class="codeph"> init() </span>. </p> <p>Obligatorio. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> parámetros </span> - <span class="codeph"> {Object} </span> objeto JSON con parámetros de configuración del visor donde el nombre de propiedad es una opción de configuración específica del visor o un modificador de SDK, y el valor de esa propiedad es un valor de configuración correspondiente. </p> <p>Obligatorio. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> Controladores <span class="codeph"> </span> - <span class="codeph"> {Object} </span> objeto JSON con llamadas de retorno de evento del visor, donde el nombre de propiedad es el nombre del evento del visor admitido y el valor de propiedad es una referencia de función de JavaScript a la llamada de retorno adecuada. </p> <p>Opcional. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> devoluciones de llamadas de evento </a> para obtener más información sobre los eventos de visor. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
} 
});
```
