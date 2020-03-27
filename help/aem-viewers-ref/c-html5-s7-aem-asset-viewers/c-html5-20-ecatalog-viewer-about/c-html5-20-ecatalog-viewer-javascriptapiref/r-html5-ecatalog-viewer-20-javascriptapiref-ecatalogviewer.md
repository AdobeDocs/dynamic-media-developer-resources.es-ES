---
description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-title: eCatalogViewer
solution: Experience Manager
title: eCatalogViewer
topic: Dynamic media
uuid: b87b6f6b-3e83-47b3-b867-30eca5eae56b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# eCatalogViewer{#ecatalogviewer}

Referencia de la API de JavaScript para el visor de catálogos electrónicos.

`eCatalogViewer([config])`

Constructor, crea una nueva instancia de visor de catálogos electrónicos.

## Parámetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> El objeto de configuración JSON opcional {Object} </span> permite que todos los ajustes del visor pasen al constructor y evite llamar a métodos de establecedor individuales. Contiene las siguientes propiedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> : <span class="codeph"> {String} </span> ID del contenedor DOM (normalmente, un <span class="codeph"> DIV </span>) en el que se inserta el visor. No es necesario que el elemento contenedor se cree antes de que se llame a este método. Sin embargo, el contenedor debe existir cuando se <span class="codeph"> ejecuta init() </span> . Obligatorio. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params </span> : <span class="codeph"> objeto {Object} </span> JSON con parámetros de configuración del visor en los que el nombre de propiedad es una opción de configuración específica del visor o un modificador SDK, y el valor de esa propiedad es un valor de configuración correspondiente. Obligatorio. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> controladores </span> : <span class="codeph"> objeto JSON {Object} </span> con rellamadas de evento del visor, donde el nombre de la propiedad es el nombre del evento del visor admitido y el valor de propiedad es una referencia de función JavaScript a una rellamada adecuada. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> Devoluciones de llamada de Evento </a> para obtener más información sobre los eventos del visor. </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Objeto </span>} objeto JSON con datos de localización. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localización de los elementos de la interfaz de usuario </a> para obtener más información. </p> <p>Consulte también la Guía <i>del usuario del SDK del</i> visor y el ejemplo para obtener más información sobre el contenido del objeto. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```

