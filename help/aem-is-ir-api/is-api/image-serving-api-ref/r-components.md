---
title: Componentes del servicio de imágenes
description: El servicio de imágenes de Dynamic Media consta de los siguientes componentes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
TQID: 'https://experienceleague.adobe.com/T6NzrpcCTHA4MgFfCDtOxUPxTrcUAmX1zMG9jia4Zb8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 1%

---

# Componentes del servicio de imágenes{#image-serving-components}

El servicio de imágenes de Dynamic Media consta de los siguientes componentes:

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Componente </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Supervisor del servidor </p> </td> 
   <td colname="col2"> <p>Un ejecutable independiente responsable de iniciar, detener y garantizar el estado de los demás componentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Proporciona el entorno para la mayoría de los componentes basados en Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servicio de monitorización/alertas </p> </td> 
   <td colname="col2"> <p>aplicación J2EE. Proporciona supervisión de servidor y alertas por correo electrónico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>aplicación J2EE. Administra conexiones de cliente, registros y comunicaciones con otros componentes. Acceso HTTP en <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servicio de almacenamiento en caché </p> </td> 
   <td colname="col2"> <p>aplicación J2EE. Administra las cachés de datos de [!DNL Platform Server]. Acceso HTTP en /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>Realiza todas las operaciones de E/S de procesamiento de imágenes y archivos de imagen. Los ejecutables de 32 y 64 bits están disponibles para Linux® (solo 32 bits para Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente de procesamiento de texto ATE </p> </td> 
   <td colname="col2"> <p>Una o más instancias del servicio de procesamiento de texto pueden estar activas cuando se ejecutan <span class="codeph"> operaciones textPs=</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente de procesamiento de SVG </p> </td> 
   <td colname="col2"> <p>Aplicación Java™ independiente (no alojada en Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Renderización de imágenes de Dynamic Media (también conocido como. Servidor de procesamiento) </p> </td> 
   <td colname="col2"> <p>Se necesita una licencia independiente para activarla. Acceso HTTP en <span class="filepath"> /ir/render</span>. Toda la funcionalidad de procesamiento de imágenes está integrada en [!DNL Platform Server] y el servidor de imágenes, sin componentes ejecutables independientes. </p> </td> 
  </tr> 
 </tbody> 
</table>

El catálogo predeterminado ([!DNL default.ini]) o catálogos de imágenes específicos proporcionan opciones de configuración adicionales (consulte [Catálogos de imágenes](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) para obtener detalles).
