---
title: setAsset
description: Referencia de la API de JavaScript para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 24d8d11d-4688-4ca0-92ae-824a5e984a10
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 1%

---

# setAsset{#setasset}

Referencia de la API de JavaScript para el visualizador de vídeo interactivo.

`setAsset(asset[, data])`

Establece el nuevo recurso y los datos de recurso adicionales opcionales. Puede llamar a este parámetro en cualquier momento, antes o después de `init()`. Si se llama después de `init()`, el visor intercambia el recurso durante la ejecución.

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> recurso </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> cadena </span>} ID de recurso nuevo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> datos </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> JSON </span> objeto JSON con los siguientes campos opcionales (distingue mayúsculas de minúsculas): </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> posterimage </span>: imagen que se mostrará en el primer fotograma antes de que comience la reproducción del vídeo. Ver <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> pie de ilustración </span> - ubicación del nuevo archivo de título. Si no se especifica, el botón de título no estará visible en la interfaz de usuario. </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> navegación </span>: URL o ruta al contenido de navegación WebVTT. El archivo WebVTT debe servirlo el servicio de imágenes. </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interactiveData </span>: URL o ruta al contenido de datos interactivo WebVTT. El archivo WebVTT debe servirlo el servicio de imágenes. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```
