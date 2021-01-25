---
description: Todos los archivos de configuración se encuentran en install_folder/conf y son editables con la mayoría de los editores de texto. Es posible que sea necesario reiniciar el servidor para que los cambios surtan efecto.
solution: Experience Manager
title: Archivos de configuración del servidor
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Archivos de configuración del servidor{#server-configuration-files}

Todos los archivos de configuración se encuentran en install_folder/conf y son editables con la mayoría de los editores de texto. Es posible que sea necesario reiniciar el servidor para que los cambios surtan efecto.

>[!NOTE]
>
>La mayoría de los archivos de configuración del servidor contienen propiedades y valores adicionales que no se describen en este documento. Estas propiedades son para uso interno del servidor y no deben modificarse a menos que se indique específicamente al servicio de asistencia técnica de Dynamic Media.

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
   <td> <p>Configuración de Platform Server. </p> </td> 
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

Los archivos de configuración se analizan más detalladamente más adelante en este documento.
