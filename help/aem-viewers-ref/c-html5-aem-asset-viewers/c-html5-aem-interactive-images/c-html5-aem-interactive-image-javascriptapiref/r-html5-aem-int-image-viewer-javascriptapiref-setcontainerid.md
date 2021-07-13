---
description: Referencia de la API de JavaScript para el visualizador de imágenes de vídeo.
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Developer,User
exl-id: 2b9b89e6-50ea-458f-9da2-6fda1884935c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

Referencia de la API de JavaScript para el visualizador de imágenes de vídeo.

` setContainerId( *`containerId`*)`

Establece el ID del contenedor DOM (normalmente un DIV) en el que se inserta el visor. No es necesario tener el elemento contenedor creado para cuando se llama a este método. Sin embargo, el contenedor debe existir cuando se ejecuta `init()`. Debe llamarse antes de `init()`.

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
