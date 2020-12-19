---
description: Referencia de la API de JavaScript para el visor de vídeos.
seo-description: Referencia de la API de JavaScript para el visor de vídeos.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 0497ae9c-e94a-458d-a4c7-5915add17f60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# setParams{#setparams}

Referencia de la API de JavaScript para el visor de vídeos.

` setParams( *`params`*)`

Establece uno o más parámetros en un valor determinado. La sintaxis del argumento de método es idéntica a una cadena de consulta URL. Es decir, representa pares nombre=valor separados por `&`. Al igual que en una cadena de consulta, los nombres y los valores se codifican en porcentaje con UTF8. Antes de llamar a `init()`, se debe llamar a este parámetro.

Este método es opcional si la información de configuración del visor se pasa con el objeto JSON `config` al constructor.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Los pares de parámetro {string}</span> name=value separados por  <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```

