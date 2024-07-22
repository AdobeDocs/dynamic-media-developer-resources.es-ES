---
description: Script de control del servicio de imágenes. Este script se utiliza para iniciar, detener o reiniciar el Supervisor del servidor de servicio de imágenes, que a su vez inicia, detiene o reinicia todos los demás componentes del servicio de imágenes.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%

---

# ImageServing{#imageserving}

Script de control del servicio de imágenes. Este script se utiliza para iniciar, detener o reiniciar el Supervisor del servidor de servicio de imágenes, que a su vez inicia, detiene o reinicia todos los demás componentes del servicio de imágenes.

## Uso {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`comando`*`

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
   <td colname="col1"> <p> <span class="codeph"> iniciar </span> </p> </td> 
   <td colname="col2"> <p> Inicie el Supervisor de servidor y todos los demás componentes del servicio de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> detener </span> </p> </td> 
   <td colname="col2"> <p> Detenga todos los componentes del servicio de imágenes, incluido el Supervisor de servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar </span> </p> </td> 
   <td colname="col2"> <p>Reinicie todos los componentes del servicio de imágenes, incluido el Supervisor de servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar { ps | es | svg } </span> </p> </td> 
   <td colname="col2"> <p> Reinicia Tomcat/[!DNL Platform Server], el servidor de imágenes o el SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> estado [ ps | es | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Devuelve la información de tiempo de actividad y uso de memoria actual para Image Server, Tomcat/[!DNL Platform Server] y SVGserver, o el estado solo del servidor especificado; en su lugar, se devuelve un mensaje informativo si el Supervisor del servidor no se está ejecutando. </p> </td> 
  </tr> 
 </tbody> 
</table>
