---
description: Las alertas estándar se envían con un mensaje de correo electrónico consolidado al final del intervalo de promedio configurado.
seo-description: Las alertas estándar se envían con un mensaje de correo electrónico consolidado al final del intervalo de promedio configurado.
seo-title: Alertas estándar
solution: Experience Manager
title: Alertas estándar
topic: Scene7 Image Serving - Image Rendering API
uuid: d3294434-a44b-4742-9d77-a6945760d33c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Alertas estándar{#standard-alerts}

Las alertas estándar se envían con un mensaje de correo electrónico consolidado al final del intervalo de promedio configurado.

La siguiente tabla describe cada tipo de alerta estándar.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Tipo de alerta</b> </th> 
   <th class="entry"> <b>Id. de título</b> </th> 
   <th class="entry"> <b>Descripción</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Solicitud bloqueada </p> </td> 
   <td> <p>Bloquear </p> </td> 
   <td> <p>Se envía cuando una solicitud no devuelve una respuesta al cliente dentro del umbral especificado. Puede ser indicativo de solicitudes de bloqueo, lo que puede causar el agotamiento del grupo de subprocesos de Java. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Alta concurrencia </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Se envía cuando el número de solicitudes que se procesan simultáneamente (la <i>superposición</i>) supera el umbral especificado. Puede indicar una condición de sobrecarga de servidor. </td> 
  </tr> 
  <tr> 
   <td> <p>Tráfico mínimo </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Se genera cuando la tasa de solicitud global cae por debajo del umbral especificado. Generalmente indica un problema de comunicación con el servidor (por ejemplo, cuando un servidor se desconecta de la línea). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tasa de error </p> </td> 
   <td> <p>Error </p> </td> 
   <td> <p>Se envía cuando la tasa media de respuestas de error HTTP durante el intervalo de muestra supera el umbral especificado. Puede ser indicativo de problemas de configuración, imágenes que faltan, programación de sitios web o errores de base de datos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tiempo de respuesta </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Se envía cuando el tiempo medio de procesamiento de la solicitud durante el intervalo de muestreo supera el umbral especificado. Generalmente indica una condición de sobrecarga temporal o persistente del servidor o del sistema de almacenamiento de imágenes back-end. </p> <p>Las respuestas a errores no se tienen en cuenta al calcular el tiempo de respuesta promedio. </p> </td> 
  </tr> 
 </tbody> 
</table>

