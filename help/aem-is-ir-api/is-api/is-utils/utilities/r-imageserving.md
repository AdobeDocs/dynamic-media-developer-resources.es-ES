---
description: Secuencia de comandos de control del servicio de imágenes. Esta secuencia de comandos se utiliza para inicio, detención o reinicio del Supervisor del servidor de servicio de imágenes, que a su vez inicio, detiene o reinicia todos los demás componentes del servicio de imágenes.
seo-description: Secuencia de comandos de control del servicio de imágenes. Esta secuencia de comandos se utiliza para inicio, detención o reinicio del Supervisor del servidor de servicio de imágenes, que a su vez inicio, detiene o reinicia todos los demás componentes del servicio de imágenes.
seo-title: ImageServing
solution: Experience Manager
title: ImageServing
topic: Scene7 Image Serving - Image Rendering API
uuid: 2975b957-e06f-42c6-8c0a-0d2757a0025a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# ImageServing{#imageserving}

Secuencia de comandos de control del servicio de imágenes. Esta secuencia de comandos se utiliza para inicio, detención o reinicio del Supervisor del servidor de servicio de imágenes, que a su vez inicio, detiene o reinicia todos los demás componentes del servicio de imágenes.

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
   <td colname="col2"> <p> Inicio el Supervisor del servidor y todos los demás componentes del servicio de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> Detenga todos los componentes del servicio de imágenes, incluido el Supervisor del servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar </span> </p> </td> 
   <td colname="col2"> <p>Reinicie todos los componentes del servicio de imágenes, incluido el Supervisor del servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar { ps | is | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Reinicia Tomcat/Platform Server, Image Server o SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | is | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Devuelve información de tiempo activo y de uso de memoria actual para el servidor de imágenes, Tomcat/Platform Server y SVGserver, o solo el estado del servidor especificado; se devuelve un mensaje informativo si el Supervisor del servidor no se está ejecutando. </p> </td> 
  </tr> 
 </tbody> 
</table>

