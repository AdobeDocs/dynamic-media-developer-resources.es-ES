---
description: Trabajo que se ejecuta en un servidor. Además, es una instancia de un trabajo programado.
seo-description: Trabajo que se ejecuta en un servidor. Además, es una instancia de un trabajo programado.
seo-title: ActiveJob
solution: Experience Manager
title: ActiveJob
topic: Scene7 Image Production System API
uuid: d7120a88-6f3e-4844-aafa-83d419470fad
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ActiveJob{#activejob}

Trabajo que se ejecuta en un servidor. Además, es una instancia de un trabajo programado.

Los trabajos existen en 3 estados:

* Programado para ejecutarse.
* Actualmente en ejecución.
* Se completó la ejecución (y ya se ha escrito información en un registro de trabajos).

Especifique un valor de tipo de trabajo para devolver el tipo de trabajo. Puede devolver los siguientes trabajos:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## Parámetros {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Manejar a la compañía. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gestionar el trabajo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nombre exclusivo del trabajo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Nombre original del tipo de <span class="codeph"> ActiveJob</span> enviado con el trabajo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Elección de tipos de trabajo devueltos por el sistema. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Elección de los estados de trabajo activos devueltos por el sistema. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> dirección de correo electrónico del usuario que programó el trabajo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">La configuración regional para los detalles del registro de trabajos y la localización por correo electrónico. <p>Especifique las configuraciones regionales como <span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>, donde el código de idioma es un código de dos letras en minúscula según lo especificado por ISO-639, y el código de país opcional es un código de dos letras en mayúsculas según lo especificado por ISO-3166. Por ejemplo, la cadena de configuración regional para inglés (Estados Unidos) sería: <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Descripción del trabajo especificada originalmente en <span class="codeph"> submitJob</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nombre del servidor que ejecuta el trabajo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Fecha, hora y zona horaria del trabajo activo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Tamaño total del trabajo activo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progreso</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Progreso del trabajo (es decir, cuánto está cerca de la finalización del trabajo). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Mensaje de texto que describe el progreso del trabajo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Fecha, hora y zona horaria de la última actualización de progreso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:TaskProgressArray</span> </td> 
   <td colname="col3"> Información sobre el progreso de la tarea asincrónica. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Detalles del trabajo de un trabajo de publicación de servicio de imágenes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageServingRenderJob</span> </td> 
   <td colname="col3"> Detalles del trabajo de un trabajo de procesamiento de imágenes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:VideoPublishJob</span> </td> 
   <td colname="col3"> Detalles del trabajo de un trabajo de publicación de vídeo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Detalles del trabajo de un trabajo de publicación de directorio de servidor. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UploadUrlsJob</span> </td> 
   <td colname="col3"> Detalles del trabajo de un trabajo de URL de carga. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizedImagesJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UploadPostJob</span> </td> 
   <td colname="col3"> Seguimiento detallado del trabajo de la carga de escritorio. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ExportJob</span> </td> 
   <td colname="col3">Permitir la exportación autorizada de archivos cargados anteriormente. Consulte <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exportjob.html" format="http" scope="external"> Trabajo</a>de exportación. </td> 
  </tr> 
 </tbody> 
</table>

