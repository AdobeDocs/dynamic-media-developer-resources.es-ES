---
description: Referencia de la API de JavaScript para el visor de zoom básico.
seo-description: Referencia de la API de JavaScript para el visor de zoom básico.
seo-title: BasicZoomViewer
solution: Experience Manager
title: BasicZoomViewer
topic: Dynamic media
uuid: 727e38af-636a-4eb3-b373-6940169d006b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# BasicZoomViewer{#basiczoomviewer}

Referencia de la API de JavaScript para el visor de zoom básico.

`BasicZoomViewer([config])`

Constructor, crea una nueva instancia de visor de zoom básico.

## Parámetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> El objeto de configuración JSON  </span> opcional {object} permite que toda la configuración del visor se pase al constructor para evitar llamar a métodos de establecedor individuales. Contiene las siguientes propiedades: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID del contenedor DOM (normalmente un  <span class="codeph"> DIV  </span>) en el que se inserta el visor. Cuando se llama a este método, no es necesario tener creado el elemento contenedor. Sin embargo, el contenedor debe existir cuando se ejecuta <span class="codeph"> init() </span>. Obligatorio. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> -  <span class="codeph"> {Object} objeto  </span> JSON con parámetros de configuración del visor en el que el nombre de propiedad es una opción de configuración específica del visor o un modificador SDK, y el valor de esa propiedad es un valor de configuración correspondiente. Obligatorio. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> controladores  </span> -  <span class="codeph"> {Object} objeto  </span> JSON con rellamadas de evento de visor, donde el nombre de propiedad es el nombre del evento de visor admitido y el valor de propiedad es una referencia de función JavaScript a la rellamada adecuada. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local"> rellamadas de Evento </a> para obtener más información sobre los eventos del visor. </p> </li> 
      <li id="li_528FE03845F847E08F964E38D6AB6E86"> <p> <span class="codeph"> localizedTexts  </span> -  <span class="codeph"> {Object} objeto  </span> JSON con datos de localización. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localización de los elementos de la interfaz de usuario </a> para obtener más información. </p> <p> Consulte también la <i>Guía del usuario del SDK del visor</i> y el ejemplo para obtener más información sobre el contenido del objeto. Opcional </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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

