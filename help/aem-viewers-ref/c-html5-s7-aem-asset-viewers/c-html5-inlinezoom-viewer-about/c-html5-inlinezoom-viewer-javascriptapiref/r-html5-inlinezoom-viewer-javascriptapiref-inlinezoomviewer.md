---
description: Referencia de la API de JavaScript para el visor de zoom en línea.
solution: Experience Manager
title: Visor flotante
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 3%

---


# Visor flotante{#flyoutviewer}

Referencia de la API de JavaScript para el visor de zoom en línea.

`FlyoutViewer([config])`

Constructor; crea una nueva instancia de visor de zoom en línea.

## Parámetros {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} objeto de configuración JSON  </span> opcional, permite que todos los ajustes del visor pasen al constructor y evite llamar a métodos de establecimiento individuales. Contiene las siguientes propiedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID del contenedor DOM (normalmente un  <span class="codeph"> DIV  </span>) en el que se inserta el visor. No es necesario tener el elemento contenedor creado para cuando se llama a este método. Sin embargo, el contenedor debe existir cuando se ejecuta <span class="codeph"> init() </span>. Obligatorio. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params  </span> -  <span class="codeph"> {Object} objeto  </span> JSON con parámetros de configuración del visor en los que el nombre de propiedad es una opción de configuración específica del visor o un modificador SDK, y el valor de esa propiedad es un valor de configuración correspondiente. Obligatorio. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> controladores  </span> : objeto  <span class="codeph"> {Object}  </span> JSON con llamadas de retorno de eventos del visor, donde el nombre de la propiedad es el nombre del evento del visor admitido y el valor de la propiedad es una referencia de función JavaScript a una llamada de retorno adecuada. Opcional. <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> Llamadas de retorno de eventos </a> para obtener más información sobre los eventos del visor. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts  </span> - {  <span class="codeph"> Objeto  </span>} objeto JSON con datos de localización. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Localización de los elementos de la interfaz de usuario </a> para obtener más información. </p> <p>Consulte la <i>Guía del usuario del SDK de visor</i> y el ejemplo para obtener más información sobre el contenido del objeto. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
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

