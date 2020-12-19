---
description: Referencia de la API de JavaScript para el visor de zoom en línea.
seo-description: Referencia de la API de JavaScript para el visor de zoom en línea.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 50fde4b0-2fd8-4341-bb2f-b1785f82ebc1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 1%

---


# setParams{#setparams}

Referencia de la API de JavaScript para el visor de zoom en línea.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Los pares de parámetro {string}</span> name=value separados por  <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Establece uno o más parámetros en un valor determinado. La sintaxis del argumento de método es idéntica a una cadena de consulta URL. Es decir, representa pares nombre=valor separados por `&`. Al igual que en una cadena de consulta, los nombres y los valores se codifican en porcentaje con UTF8. Antes de llamar a `init()`, se debe llamar a este parámetro. Este método es opcional si la información de configuración del visor se pasa con el objeto JSON `config` al constructor.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```

