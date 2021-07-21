---
description: Las alertas estándar se envían con un mensaje de correo electrónico consolidado al final del intervalo de promedio configurado.
solution: Experience Manager
title: Alertas estándar
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# Alertas estándar{#standard-alerts}

Las alertas estándar se envían con un mensaje de correo electrónico consolidado al final del intervalo de promedio configurado.

La siguiente tabla describe cada tipo de alerta estándar.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Tipo de alerta</b> </th> 
   <th class="entry"> <b>ID de título</b> </th> 
   <th class="entry"> <b>Descripción</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Solicitud bloqueada </p> </td> 
   <td> <p>Bloquear </p> </td> 
   <td> <p>Se envía cuando una solicitud no devuelve una respuesta al cliente dentro del umbral especificado. Puede ser indicativo de solicitudes colgadas, lo que puede causar el agotamiento del grupo de subprocesos de Java. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Alta concurrencia </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Se envía cuando el número de solicitudes que se procesan simultáneamente (<i>superposición</i>) supera el umbral especificado. Puede indicar una condición de sobrecarga del servidor. </td> 
  </tr> 
  <tr> 
   <td> <p>Tráfico mínimo </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Generado cuando la tasa de solicitud global se encuentra por debajo del umbral especificado. Normalmente indica un problema de comunicación con el servidor (por ejemplo, cuando un servidor está fuera de línea). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tasa de error </p> </td> 
   <td> <p>Error </p> </td> 
   <td> <p>Se envía cuando la tasa media de respuestas de error HTTP durante el intervalo de muestreo supera el umbral especificado. Puede indicar problemas de configuración, imágenes faltantes, programación de sitios web o errores de bases de datos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tiempo de respuesta </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Se envía cuando el tiempo medio de procesamiento de la solicitud durante el intervalo de muestreo aumenta por encima del umbral especificado. Normalmente indica una condición de sobrecarga temporal o persistente del servidor o del sistema de almacenamiento de imágenes back-end. </p> <p>Las respuestas de error no se tienen en cuenta al calcular el tiempo de respuesta promedio. </p> </td> 
  </tr> 
 </tbody> 
</table>
