---
title: setParam
description: Referencia de la API de JavaScript para el visor de carrusel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 0829933f-a90b-4066-9904-748f2a727169
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 3%

---

# setParam{#setparam}

Referencia de la API de JavaScript para el visor de carrusel.

` setParam( *`nombre, valor`*)`

Establece el parámetro del visor en un valor especificado. El parámetro es una opción de configuración específica del visor o un modificador del kit de desarrollo de software. Se llama a este parámetro antes de `init()`.

Este método es opcional si la información de configuración del visor se pasó con el objeto JSON `config` al constructor.

Consulte también [xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md).

## Parámetros {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

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

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```
