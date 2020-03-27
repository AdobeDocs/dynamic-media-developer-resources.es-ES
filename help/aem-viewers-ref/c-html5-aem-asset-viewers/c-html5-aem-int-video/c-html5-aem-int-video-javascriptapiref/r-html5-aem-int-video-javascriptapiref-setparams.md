---
description: Referencia de la API de JavaScript para el visor de vídeo interactivo.
seo-description: Referencia de la API de JavaScript para el visor de vídeo interactivo.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 0a5b9798-0e3f-4310-9b6e-0214a420951b
translation-type: tm+mt
source-git-commit: 94b8dde58cda2670f3e2f22f217599c23601e450

---


# setParams{#setparams}

Referencia de la API de JavaScript para el visor de vídeo interactivo.

` setParams( *`params`*)`

Establece uno o más parámetros en un valor determinado. La sintaxis del argumento de método es idéntica a una cadena de consulta URL. Es decir, representa pares nombre=valor separados por `&`. Al igual que en una cadena de consulta, los nombres y los valores están codificados en porcentaje con UTF8. Antes de llamar `init()`, se debe llamar a este parámetro.

Este método es opcional si la información de configuración del visor se pasó con el objeto `config` JSON al constructor.

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).


## Parámetro {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Los pares de parámetros {string}</span> name=value separados por <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
