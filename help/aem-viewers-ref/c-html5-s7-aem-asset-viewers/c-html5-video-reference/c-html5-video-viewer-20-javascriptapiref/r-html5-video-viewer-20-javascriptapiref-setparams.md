---
title: setParams
description: Referencia de la API de JavaScript para el visualizador de vídeos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 76bad894-bfb8-4d79-b3ff-c2497c68e5e8
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# setParams{#setparams}

Referencia de la API de JavaScript para el visualizador de vídeos.

` setParams( *`parámetros`*)`

Establece uno o varios parámetros en un valor determinado. La sintaxis del argumento de método es idéntica a una cadena de consulta de dirección URL. Es decir, representa pares nombre=valor separados con `&`. Al igual que en una cadena de consulta, los nombres y valores se codifican con porcentajes mediante UTF8. Antes de llamar a `init()`, este parámetro debe llamarse.

Este método es opcional si la información de configuración del visor se pasa con `config` Objeto JSON al constructor.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> parámetros</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> pares de parámetros nombre=valor separados con <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```css{.line-numbers}
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
