---
title: setParam
description: Referencia de la API de JavaScript para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 820379e5-04ef-4840-85ca-bbfd9b42cf17
TQID: 'https://experienceleague.adobe.com/21qvI-g8-lSvtdkZ0sgGjoq2rTeJLpsDmaKL8XUW2ow'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 3%

---

# setParam{#setparam}

Referencia de la API de JavaScript para el visualizador de vídeo interactivo.

` setParam( *`nombre, valor`*)`

Establece el parámetro del visor en un valor especificado. El parámetro es una opción de configuración específica del visor o un modificador del kit de desarrollo de software. Se llama a este parámetro antes de `init()`.

Este método es opcional si la información de configuración del visor se pasó con el objeto JSON `config` al constructor.

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Parámetros {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> nombre </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> nombre del parámetro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> valor del parámetro. El valor no puede tener codificación porcentual. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
