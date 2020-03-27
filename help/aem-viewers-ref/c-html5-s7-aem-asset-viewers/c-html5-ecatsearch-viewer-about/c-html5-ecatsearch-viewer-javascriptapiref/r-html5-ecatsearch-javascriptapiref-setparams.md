---
description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 4929884e-b072-4177-83c3-1f9b4e5df569
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setParams{#setparams}

Referencia de la API de JavaScript para el visor de catálogos electrónicos.

[!DNL ` setParams( *`params`*)`]

Establece uno o más parámetros en un valor determinado. La sintaxis del argumento de método es idéntica a una cadena de consulta URL. Es decir, representa pares nombre=valor separados por [!DNL `&`]. Al igual que en una cadena de consulta, los nombres y los valores están codificados en porcentaje con UTF8. Antes de llamar [!DNL `init()`], se debe llamar a este parámetro.

Este método es opcional si la información de configuración del visor se pasa con el objeto [!DNL `config`] JSON al constructor.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```

