---
description: Referencia de la API de JavaScript para el visor de carrusel.
seo-description: Referencia de la API de JavaScript para el visor de carrusel.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 87f16ea9-0267-4114-9aeb-a68fdb616a88
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParam{#setparam}

Referencia de la API de JavaScript para el visor de carrusel.

` setParam( *`nombre, valor`*)`

Establece el parámetro del visor en un valor especificado. El parámetro es una opción de configuración específica del visor o un modificador del kit de desarrollo de software. Este parámetro se llama antes `init()`.

Este método es opcional si la información de configuración del visor se pasó con el objeto `config` JSON al constructor.

Consulte también [xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md).

## Parámetros {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> nombre del parámetro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> valor </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Valor {string} </span> del parámetro. El valor no puede estar codificado en porcentaje. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```

