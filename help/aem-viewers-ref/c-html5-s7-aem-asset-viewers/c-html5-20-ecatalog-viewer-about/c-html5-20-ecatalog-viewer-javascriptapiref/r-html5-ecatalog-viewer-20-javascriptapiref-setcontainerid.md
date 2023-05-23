---
title: setContainerId
description: Referencia de la API de JavaScript para eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 32e75d36-cc9a-42df-95e8-5b48456296e9
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

Referencia de la API de JavaScript para eCatalog Viewer.

` setContainerId( *`containerId`*)`

Establece el ID del `DOM` contenedor (normalmente un `DIV`) en la que se inserta el visor. No es necesario tener el elemento contenedor creado para el momento en que se llama a este método. Sin embargo, el contenedor debe existir cuando `init()` se ejecuta. Debe llamarse antes de `init()`.

Este método es opcional si la información de configuración del visor se pasa con `config` Objeto JSON al constructor.

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
