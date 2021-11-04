---
title: SmartCropVideoViewer
description: Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 3%

---

# SmartCropVideoViewer{#smartcropvideoviewer}

Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente.

`SmartCropVideoViewer([config])`

Constructor; crea una instancia de visor de vídeo de recorte inteligente.

## Parámetros {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto de configuración JSON opcional, permite que todos los ajustes del visor pasen al constructor y evite llamar a métodos de ajuste individuales. Contiene las siguientes propiedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {Cadena} </span> ID del contenedor DOM (normalmente, un <span class="codeph"> DIV </span>) en la que se inserta el visor. No es necesario tener el elemento contenedor creado para cuando se llama a este método. Sin embargo, el contenedor debe existir cuando <span class="codeph"> init() </span> se ejecuta. Obligatorio. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> El objeto JSON con parámetros de configuración del visor en los que el nombre de la propiedad es una opción de configuración específica del visor o un modificador del SDK, y el valor de esa propiedad es un valor de configuración correspondiente. Obligatorio. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> controladores </span> - <span class="codeph"> {Object} </span> El objeto JSON con llamadas de retorno de eventos del visor, donde el nombre de la propiedad es el nombre del evento del visor admitido, y el valor de la propiedad es una referencia de función JavaScript a una llamada de retorno adecuada. Opcional. <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> Llamadas de retorno de eventos </a> para obtener más información sobre los eventos del visor. </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Objeto </span>} objeto JSON con datos de localización. Opcional. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> Espacio de nombres del SDK del visor </a> para obtener más información. </p> <p>Consulte la <i>Guía del usuario del SDK del visor</i> y el ejemplo para obtener más información sobre el contenido del objeto. Opcional. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"SmartCropVideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"SmartCropVideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
