---
description: Referencia de la API de JavaScript para el visualizador de Video360
seo-description: Referencia de la API de JavaScript para el visualizador de Video360
seo-title: setVideo
solution: Experience Manager
title: setVideo
uuid: 749aa32c-c27f-476c-954b-d4524528bccc
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---


# setVideo{#setvideo}

Referencia de la API de JavaScript para el visualizador de Video360

`setVideo(videoUrl)`

Establece el nuevo vídeo externo. Se puede llamar en cualquier momento, tanto antes como después de `init()`. Si se llama después de `init()`, el visor intercambia el vídeo en tiempo de ejecución.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parámetros {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} es una dirección URL absoluta del nuevo vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```

