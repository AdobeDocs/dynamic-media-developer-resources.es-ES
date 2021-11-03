---
title: setVideo
description: Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: c89099f6-09f7-4d81-939e-90ffa2764c8c
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# setVideo{#setvideo}

Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente

`setVideo(videoUrl[, data])`

Establece el nuevo vídeo externo y los datos de vídeo adicionales opcionales. Se puede llamar en cualquier momento, tanto antes como después de `init()`. Si se llama después de `init()`, el visor intercambia el vídeo en tiempo de ejecución.

Consulte también [init]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parámetros {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Cadena </span>} una dirección URL absoluta del nuevo vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> data </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} Objeto JSON con los siguientes campos opcionales (con distinción de mayúsculas y minúsculas): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage </span> - Imagen que se mostrará en el primer fotograma antes de que el vídeo empiece a reproducirse. Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> caption </span> - Ubicación del nuevo archivo de rótulo. Si no se especifica ningún archivo de rótulo, el botón de rótulo no se muestra en la interfaz de usuario. </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> navegación </span> : URL o ruta al contenido de navegación de WebVTT. El archivo WebVTT debe ser servido por Image Serving. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```
