---
description: Detalles de una entrada de registro de trabajos asociada a un recurso en particular. Datos devueltos por getAssetJobLogs.
seo-description: Detalles de una entrada de registro de trabajos asociada a un recurso en particular. Datos devueltos por getAssetJobLogs.
seo-title: AssetJobLog
solution: Experience Manager
title: AssetJobLog
topic: Scene7 Image Production System API
uuid: 0dd65da1-f358-4d9a-98a2-abfb036347e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetJobLog{#assetjoblog}

Detalles de una entrada de registro de trabajos asociada a un recurso en particular. Datos devueltos por getAssetJobLogs.

Sintaxis

## Parámetros {#section-5da4d6156b7f4ca88a67202fbf736104}

<table id="table_7BC785BC95EA43D582D1B2289FF3130D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Identificador de trabajo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nombre de trabajo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Mensaje en el registro de trabajos. <p><span class="codeph"> El campo de respuesta logMessage</span> se localiza en función del campo de configuración regional <span class="codeph"> authHeader</span> . </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Tipo de trabajo en la entrada de registro. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> correo electrónico del usuario que envió el trabajo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Fecha del trabajo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> auxArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:JobLogDetailArray</span> </td> 
   <td colname="col3"> Matriz de mensajes auxiliares de registro de trabajos para cada registro de trabajos. </td> 
  </tr> 
 </tbody> 
</table>

