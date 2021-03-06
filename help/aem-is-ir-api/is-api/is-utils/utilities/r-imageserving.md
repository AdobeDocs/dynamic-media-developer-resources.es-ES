---
description: Secuencia de comandos de control de servicio de imágenes. Esta secuencia de comandos se utiliza para iniciar, detener o reiniciar el Supervisor del servidor de servicio de imágenes, que a su vez inicia, detiene o reinicia todos los demás componentes de servicio de imágenes.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---

# ImageServing{#imageserving}

Secuencia de comandos de control de servicio de imágenes. Esta secuencia de comandos se utiliza para iniciar, detener o reiniciar el Supervisor del servidor de servicio de imágenes, que a su vez inicia, detiene o reinicia todos los demás componentes de servicio de imágenes.

## Uso {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`command`*`

## Comandos {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Comando </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inicio </span> </p> </td> 
   <td colname="col2"> <p> Inicie el Supervisor del servidor y todos los demás componentes de servicio de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> Detenga todos los componentes de servicio de imágenes, incluido el Supervisor del servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar </span> </p> </td> 
   <td colname="col2"> <p>Reinicie todos los componentes de servicio de imágenes, incluido el Supervisor del servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar { ps | es | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Reinicia Tomcat/Platform Server, Image Server o SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | es | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Devuelve información de uso de memoria actual y de tiempo activo para Image Server, Tomcat/Platform Server y SVGserver, o solo el estado del servidor especificado; se devuelve un mensaje informativo en su lugar si el Supervisor del servidor no se está ejecutando. </p> </td> 
  </tr> 
 </tbody> 
</table>
