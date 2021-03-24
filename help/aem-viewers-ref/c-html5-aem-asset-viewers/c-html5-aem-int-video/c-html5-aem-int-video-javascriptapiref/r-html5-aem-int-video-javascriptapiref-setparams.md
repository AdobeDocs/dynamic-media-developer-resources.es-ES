---
description: Referencia de la API de JavaScript para el visualizador de vídeo interactivo.
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---


# setParams{#setparams}

Referencia de la API de JavaScript para el visualizador de vídeo interactivo.

` setParams( *`params`*)`

Establece uno o más parámetros en un valor determinado. La sintaxis del argumento de método es idéntica a una cadena de consulta de URL. Es decir, representa pares nombre=valor separados por `&`. Al igual que en una cadena de consulta, los nombres y valores están codificados por porcentajes utilizando UTF8. Antes de llamar a `init()`, se debe llamar a este parámetro.

Este método es opcional si la información de configuración del visor se pasó con el objeto JSON `config` al constructor.

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).


## Parámetro {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value pares de parámetros separados por  <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
