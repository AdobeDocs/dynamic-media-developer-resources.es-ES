---
description: 'El servicio de imágenes de Scene7 consta de los siguientes componentes '
solution: Experience Manager
title: Componentes de servicio de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# Componentes de servicio de imágenes{#image-serving-components}

El servicio de imágenes de Scene7 consta de los siguientes componentes:

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
   <td colname="col2"> <p>Ejecutable independiente responsable de iniciar, detener y garantizar el estado de los demás componentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Proporciona el entorno para la mayoría de los componentes basados en Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servicio de monitoreo/alertas </p> </td> 
   <td colname="col2"> <p>aplicación J2EE. Proporciona supervisión del servidor y alertas por correo electrónico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servidor de plataforma </p> </td> 
   <td colname="col2"> <p>aplicación J2EE. Gestiona las conexiones de cliente, el registro y las comunicaciones con otros componentes. Acceso HTTP en <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servicio de almacenamiento en caché </p> </td> 
   <td colname="col2"> <p>aplicación J2EE. Gestiona las cachés de datos de Platform Server. Acceso HTTP en /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Image Server </p> </td> 
   <td colname="col2"> <p>Realiza todas las operaciones de I/O de archivos de imagen y procesamiento de imágenes. Tanto los ejecutables de 32 bits como los de 64 bits están disponibles para Linux (solo de 32 bits para Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente de procesamiento de texto ATE </p> </td> 
   <td colname="col2"> <p>Una o más instancias del servicio de renderización de texto pueden estar activas cuando se ejecutan operaciones <span class="codeph"> textPs=</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente de renderización SVG </p> </td> 
   <td colname="col2"> <p>Aplicación Java independiente (no alojada por Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Representación de imágenes de Dynamic Media (también conocida como Render Server) </p> </td> 
   <td colname="col2"> <p>Requiere una licencia independiente para activarla. Acceso HTTP en <span class="filepath"> /ir/render</span>. Toda la funcionalidad de renderización de imágenes está integrada en Platform Server y Image Server, sin componentes ejecutables independientes. </p> </td> 
  </tr> 
 </tbody> 
</table>

El catálogo predeterminado ( [!DNL default.ini]) o catálogos de imágenes específicos proporcionan configuraciones adicionales (consulte [Catálogos de imágenes](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) para obtener más información).
