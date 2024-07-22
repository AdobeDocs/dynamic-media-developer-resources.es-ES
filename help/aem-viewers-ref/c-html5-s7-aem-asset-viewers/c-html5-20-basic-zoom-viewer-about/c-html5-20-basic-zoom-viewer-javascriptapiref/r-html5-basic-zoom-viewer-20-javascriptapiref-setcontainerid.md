---
title: setContainerId
description: Referencia de la API de JavaScript para el visor de zoom básico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: dae07170-24bb-4e8c-86d6-5313db33736f
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

Referencia de la API de JavaScript para el visor de zoom básico.

` setContainerId( *`containerId`*)`

Establece el ID del contenedor DOM (normalmente un DIV) en el que se inserta el visor. No es necesario tener el elemento contenedor creado para el momento en que se llama a este método. Sin embargo, el contenedor debe existir cuando se ejecute `init()`. Se debe llamar antes de `init()`.

Este método es opcional si la información de configuración del visor se pasó con el objeto JSON `config` al constructor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID del contenedor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
