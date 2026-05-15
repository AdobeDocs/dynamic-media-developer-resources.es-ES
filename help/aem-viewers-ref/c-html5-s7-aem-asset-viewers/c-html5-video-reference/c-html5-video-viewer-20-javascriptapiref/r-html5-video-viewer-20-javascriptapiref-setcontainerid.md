---
title: setContainerId
description: Referencia de la API de JavaScript para el visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 9f2857a4-108d-4689-9c39-cb2635405d0d
TQID: 'https://experienceleague.adobe.com/Scvi0NLsspUOCki7LP2G1rX0g9iKNXkLwIQIvk8eVVw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 2%

---

# setContainerId{#setcontainerid}

Referencia de la API de JavaScript para el visor de vídeo.

` setContainerId( *`containerId`*)`

Establece el identificador del contenedor DOM (normalmente un `DIV`) en el que se inserta el visor. No es necesario tener el elemento contenedor creado para el momento en que se llama a este método. Sin embargo, el contenedor debe existir cuando se ejecute `init()`. Se llama a este parámetro antes de `init()`. Este método es opcional si la información de configuración del visor se pasa con el objeto JSON `config` al constructor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID de contenedor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
