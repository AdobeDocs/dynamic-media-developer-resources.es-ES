---
description: Referencia de la API de JavaScript para el visualizador de vídeo.
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 2%

---


# setContainerId{#setcontainerid}

Referencia de la API de JavaScript para el visualizador de vídeo.

` setContainerId( *`containerId`*)`

Establece el ID del contenedor DOM (normalmente un `DIV`) en el que se inserta el visor. No es necesario tener el elemento contenedor creado para cuando se llama a este método. Sin embargo, el contenedor debe existir cuando se ejecuta `init()`. Se llama a este parámetro antes de `init()`. Este método es opcional si la información de configuración del visor se pasa con el objeto JSON `config` al constructor.

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

