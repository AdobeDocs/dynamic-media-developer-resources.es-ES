---
title: FlyoutViewer
description: Referencia de la API de JavaScript para el visor flotante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b64f16c8-03bf-4603-972f-845a4c1e2b02
source-git-commit: f970421ccc482b698343aa18e7dfde7bea4c2a89
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 3%

---

# FlyoutViewer{#flyoutviewer}

Referencia de la API de JavaScript para el visor flotante.

`FlyoutViewer([config])`

Constructor; crea una instancia de visor flotante.

## Parámetros {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configuración </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto de configuración JSON opcional, permite que toda la configuración del visor pase al constructor y evite llamar a métodos de establecedor individuales. Contiene las siguientes propiedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID del contenedor DOM (normalmente un DIV </span> de <span class="codeph">) en el que se inserta el visor. No es necesario tener el elemento contenedor creado para el momento en que se llama a este método. Sin embargo, el contenedor debe existir cuando se ejecute <span class="codeph"> init() </span>. Obligatorio. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> parámetros </span> - <span class="codeph"> {Object} </span> objeto JSON con parámetros de configuración del visor donde el nombre de propiedad es una opción de configuración específica del visor o un modificador del SDK, y el valor de esa propiedad es un valor de configuración correspondiente. Obligatorio. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> Controladores <span class="codeph"> </span> - <span class="codeph"> {Object} </span> objeto JSON con llamadas de retorno de evento del visor, donde el nombre de propiedad es el nombre de evento del visor admitido y el valor de propiedad es una referencia de función de JavaScript a una llamada de retorno adecuada. Opcional. <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> devoluciones de llamadas de evento </a> para obtener más información sobre los eventos de visor. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts </span> - objeto <span class="codeph"> </span> objeto JSON con datos de localización. Opcional. </p> <p>Consulte Localización de elementos de la interfaz de usuario </a> de <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> para obtener más información. </p> <p>Consulte la <i>Guía de usuario del SDK de visor</i> y el ejemplo para obtener más información sobre el contenido del objeto. Opcional. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
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
