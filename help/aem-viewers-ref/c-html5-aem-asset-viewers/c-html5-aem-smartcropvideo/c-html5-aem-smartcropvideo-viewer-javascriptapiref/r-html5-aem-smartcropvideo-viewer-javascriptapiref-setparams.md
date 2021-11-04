---
title: setParams
description: Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---

# setParams{#setparams}

Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente.

` setParams( *`params`*)`

Establece uno o más parámetros en un valor determinado. La sintaxis del argumento de método es idéntica a una cadena de consulta de URL. Es decir, representa pares de nombre=valor separados por `&`. Los mismos que en una cadena de consulta, los nombres y los valores se codifican por porcentajes utilizando UTF8. Antes de llamar a `init()`, se debe llamar a este parámetro.

Este método es opcional si se pasa la información de configuración del visor con `config` objeto JSON al constructor.

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> pares de parámetros name=value separados por <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&SmartCropVideoPlayer.playback=progressive")
```
