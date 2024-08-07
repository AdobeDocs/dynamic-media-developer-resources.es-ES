---
title: setAsset
description: Referencia de la API de JavaScript para el visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# setAsset{#setasset}

Referencia de la API de JavaScript para el visor de vídeo.

`setAsset(asset[, data])`

Establece el nuevo recurso y los datos de recurso adicionales opcionales. Puede llamar a este parámetro en cualquier momento, antes o después de `init()`. Si se llama después de `init()`, el visor intercambia el recurso durante la ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parámetros {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> recurso </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> cadena </span>} ID de recurso nuevo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> datos </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> JSON </span> objeto JSON con los siguientes campos opcionales (distingue mayúsculas de minúsculas): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage </span>: imagen que se mostrará en el primer fotograma antes de que comience la reproducción del vídeo. Ver <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> pie de ilustración </span> - ubicación del nuevo archivo de pie de ilustración cerrado. Si no se especifica el archivo, el botón de subtítulos opcionales no estará visible en la interfaz de usuario. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> navegación </span>: URL o ruta al contenido de navegación WebVTT. El archivo WebVTT debe servirlo el servicio de imágenes </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
