---
description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cbd7987b-5e47-4ac0-8235-a217e5e6dee9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# setParams{#setparams}

Referencia de la API de JavaScript para el visor de catálogos electrónicos.

[!DNL ` setParams( *`parámetros`*)`]

Establece uno o varios parámetros en un valor determinado. La sintaxis del argumento de método es idéntica a una cadena de consulta de dirección URL. Es decir, representa pares nombre=valor separados con [!DNL `&`]. Al igual que en una cadena de consulta, los nombres y valores se codifican con porcentajes mediante UTF8. Antes de llamar a [!DNL `init()`], se debe llamar a este parámetro.

Este método es opcional si la información de configuración del visor se pasa con el objeto JSON [!DNL `config`] al constructor.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```
