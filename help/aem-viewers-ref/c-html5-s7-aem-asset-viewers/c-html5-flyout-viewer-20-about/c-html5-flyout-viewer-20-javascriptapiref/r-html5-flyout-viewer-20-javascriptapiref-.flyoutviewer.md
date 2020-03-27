---
description: Referencia de la API de JavaScript para el visor flotante.
seo-description: Referencia de la API de JavaScript para el visor flotante.
seo-title: Visor flotante
solution: Experience Manager
title: Visor flotante
topic: Dynamic media
uuid: 070ae248-34fd-40fb-9d40-2c7fff388592
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Visor flotante{#flyoutviewer}

Referencia de la API de JavaScript para el visor flotante.

`FlyoutViewer([config])`

Constructor; crea una nueva instancia de visor flotante.

## Parámetros {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> El objeto de configuración JSON opcional {Object} </span> permite que todos los ajustes del visor pasen al constructor y evite llamar a métodos de establecedor individuales. Contiene las siguientes propiedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> : <span class="codeph"> {String} </span> ID del contenedor DOM (normalmente, un <span class="codeph"> DIV </span>) en el que se inserta el visor. No es necesario que el elemento contenedor se cree antes de que se llame a este método. Sin embargo, el contenedor debe existir cuando se <span class="codeph"> ejecuta init() </span> . Obligatorio. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> : <span class="codeph"> objeto {Object} </span> JSON con parámetros de configuración del visor en los que el nombre de propiedad es una opción de configuración específica del visor o un modificador SDK, y el valor de esa propiedad es un valor de configuración correspondiente. Obligatorio. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> controladores </span> : <span class="codeph"> objeto JSON {Object} </span> con rellamadas de evento del visor, donde el nombre de la propiedad es el nombre del evento del visor admitido y el valor de propiedad es una referencia de función JavaScript a una rellamada adecuada. Opcional. <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> Devoluciones de llamada de Evento </a> para obtener más información sobre los eventos del visor. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Objeto </span>} objeto JSON con datos de localización. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Localización de los elementos de la interfaz de usuario </a> para obtener más información. </p> <p>Consulte la Guía <i>del usuario del SDK del</i> visor y el ejemplo para obtener más información sobre el contenido del objeto. Opcional. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```

