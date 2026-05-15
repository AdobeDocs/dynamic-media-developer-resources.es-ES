---
title: SpinViewer
description: Referencia de la API de JavaScript para el visor de giros.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 0cfde665-c578-41a0-a428-0db3cbdac6ae
TQID: 'https://experienceleague.adobe.com/-aZhpoZiLqC8B77Ajt8wPTLBC3Z7zwcTiF9bPjndglg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 205
ht-degree: 3%

---

# SpinViewer{#spinviewer}

Referencia de la API de JavaScript para el visor de giros.

`SpinViewer([config])`

Constructor, crea una nueva instancia del visualizador de giros.

## Parámetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configuración </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto de configuración JSON opcional, permite que toda la configuración del visor pase al constructor y evite llamar a métodos de establecedor individuales. Contiene las siguientes propiedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID del contenedor DOM (normalmente un DIV <span class="codeph"> </span>) en el que se inserta el visor. No es necesario tener el elemento contenedor creado para el momento en que se llama a este método. Sin embargo, el contenedor debe existir cuando se ejecute <span class="codeph"> init() </span>. Obligatorio. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> parámetros </span> - <span class="codeph"> {Object} </span> objeto JSON con parámetros de configuración del visor donde el nombre de propiedad es una opción de configuración específica del visor o un modificador SDK, y el valor de esa propiedad es un valor de configuración correspondiente. Obligatorio. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> controladores </span> - <span class="codeph"> {Object} </span> objeto JSON con llamadas de retorno de evento del visor, donde el nombre de la propiedad es el nombre del evento del visor admitido y el valor de la propiedad es una referencia de función de JavaScript a una llamada de retorno adecuada. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> devoluciones de llamadas de evento </a> para obtener más información sobre los eventos de visor. </p> </li> 
      <li id="li_643787FB4A424D0AB6B8E12F44C3A9AC"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> objeto JSON con datos de localización. Opcional. </p> <p>Consulte Localización de elementos de la interfaz de usuario </a> de <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> para obtener más información. </p> <p>Consulte también la <i>Guía del usuario de Viewer SDK</i> y el ejemplo para obtener más información sobre el contenido del objeto. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
