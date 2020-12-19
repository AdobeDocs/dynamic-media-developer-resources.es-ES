---
description: Referencia de la API de JavaScript para el visor de imágenes de vídeo.
seo-description: Referencia de la API de JavaScript para el visor de imágenes de vídeo.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: f1486f82-28dd-4321-a0e5-9e5696f6bbf7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---


# setContainerId{#setcontainerid}

Referencia de la API de JavaScript para el visor de imágenes de vídeo.

` setContainerId( *`containerId`*)`

Establece el ID del contenedor DOM (normalmente DIV) en el que se inserta el visor. No es necesario que el elemento contenedor se cree antes de que se llame a este método. Sin embargo, el contenedor debe existir cuando se ejecuta `init()`. Debe llamarse antes de `init()`.

Este método es opcional si la información de configuración del visor se pasa con el objeto JSON `config` al constructor.

## Parámetro {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> ID del contenedor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

