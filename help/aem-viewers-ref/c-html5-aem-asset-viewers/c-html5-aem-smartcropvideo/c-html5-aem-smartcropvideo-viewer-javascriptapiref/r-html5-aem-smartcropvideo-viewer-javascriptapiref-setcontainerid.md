---
title: setContainerId
description: Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

Referencia de la API de JavaScript para el visor de vídeos de recorte inteligente.

` setContainerId( *`containerId`*)`

Establece el ID del contenedor DOM (normalmente, un `DIV`) en la que se inserta el visor. No es necesario tener el elemento contenedor creado para cuando se llama a este método. Sin embargo, el contenedor debe existir cuando `init()` se ejecuta. Este parámetro se invoca antes de que `init()`. Este método es opcional si se pasa la información de configuración del visor con `config` objeto JSON al constructor.

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
