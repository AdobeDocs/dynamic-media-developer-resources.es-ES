---
title: setParams
description: Referencia de la API de JavaScript para el visor flotante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: bd26292d-f9c6-4e67-8cc1-c74336d50860
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setParams{#setparams}

Referencia de la API de JavaScript para el visor flotante.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> pares de parámetros name=value separados por <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Establece uno o más parámetros en un valor determinado. La sintaxis del argumento de método es idéntica a una cadena de consulta de URL. Es decir, representa pares de nombre=valor separados por `&`. Los mismos que en una cadena de consulta, los nombres y los valores se codifican por porcentajes utilizando UTF8. Antes de llamar a `init()`, se debe llamar a este parámetro. Este método es opcional si se pasa la información de configuración del visor con `config` objeto JSON al constructor.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```
