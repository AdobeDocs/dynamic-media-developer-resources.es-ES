---
description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-description: Referencia de la API de JavaScript para el visor de catálogos electrónicos.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 19149e38-b9d2-4ecd-a555-92e2960f7ee3
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---


# setContainerId{#setcontainerid}

Referencia de la API de JavaScript para el visor de catálogos electrónicos.

[!DNL ` setContainerId( *`containerId`*)`]

Define el ID del `DOM` contenedor (normalmente, un `DIV`) en el que se inserta el visor. No es necesario que el elemento contenedor se cree antes de que se llame a este método. Sin embargo, el contenedor debe existir cuando `init()` se ejecuta. Debe llamarse antes `init()`.

Este método es opcional si la información de configuración del visor se pasa con el objeto `config` JSON al constructor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ID de {string} </span> del contenedor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

