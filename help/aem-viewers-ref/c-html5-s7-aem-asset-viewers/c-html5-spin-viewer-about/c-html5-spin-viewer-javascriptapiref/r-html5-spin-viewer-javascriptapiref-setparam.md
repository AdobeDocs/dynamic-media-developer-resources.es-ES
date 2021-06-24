---
description: Referencia de la API de JavaScript para el visualizador de giros.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Developer,Business Practitioner
exl-id: 16d1d2cd-f58f-4ac3-b89f-f2f12fee231d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setParam{#setparam}

Referencia de la API de JavaScript para el visualizador de giros.

` setParam( *`nombre, valor`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> nombre del parámetro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> valor del parámetro. El valor no puede estar codificado por porcentajes. </p> </td> 
  </tr> 
 </tbody> 
</table>

Establece el parámetro del visor en un valor especificado. El parámetro es una opción de configuración específica del visor o un modificador del kit de desarrollo de software. Se llama a este parámetro antes de `init()`.

Este método es opcional si la información de configuración del visor se pasa con el objeto JSON `config` al constructor.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
