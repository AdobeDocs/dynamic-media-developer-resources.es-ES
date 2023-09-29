---
title: Archivos de configuración del servidor
description: Todos los archivos de configuración se encuentran en la carpeta install_folder/conf y se pueden editar con la mayoría de los editores de texto. Reinicie el servidor para que los cambios surtan efecto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---

# Archivos de configuración del servidor{#server-configuration-files}

Todos los archivos de configuración se encuentran en `install_folder/conf` y son editables con la mayoría de los editores de texto. Reinicie el servidor para que los cambios surtan efecto.

>[!NOTE]
>
>La mayoría de los archivos de configuración del servidor contienen propiedades y valores adicionales que no se describen en este documento. Estas propiedades son para uso interno del servidor y no se deben modificar a menos que así lo indique el servicio de asistencia técnica de Dynamic Media.

Este documento analiza la configuración de los siguientes archivos de configuración:

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Archivo de configuración</b> </th> 
   <th class="entry"> <b>Descripción</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>Configuración del Supervisor del servidor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Configuración de Tomcat. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] configuración. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>Configuración del servicio de catálogo. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>Configuración de supervisión del servidor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>Configuración del servidor de imágenes. </p> </td> 
  </tr> 
 </tbody> 
</table>

Los archivos de configuración se analizan con más detalle más adelante en este documento.
