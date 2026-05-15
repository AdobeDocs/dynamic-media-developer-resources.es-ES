---
title: setParams
description: Referencia de la API de JavaScript para el visor de Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
TQID: 'https://experienceleague.adobe.com/dzJWfzwEhkx3964O0SYqStA7ZmcMISt--W72OKNTpbE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 3%

---

# setParams{#setparams}

Referencia de la API de JavaScript para el visor de Video360.

` setParams( *`parámetros`*)`

Establece uno o varios parámetros en un valor determinado. La sintaxis del argumento de método es idéntica a una cadena de consulta de dirección URL. Es decir, representa pares nombre=valor separados con `&`. Al igual que en una cadena de consulta, los nombres y valores se codifican con porcentajes mediante UTF8. Antes de llamar a `init()`, se debe llamar a este parámetro.

Este método es opcional si la información de configuración del visor se pasó con el objeto JSON `config` al constructor.

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Parámetro {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> parámetros</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> pares de parámetro name=value separados con <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
