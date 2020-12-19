---
description: Envía un trabajo al sistema.
seo-description: Envía un trabajo al sistema.
seo-title: submitJob
solution: Experience Manager
title: submitJob
topic: Scene7 Image Production System API
uuid: d3a83b59-bcd7-4ae9-b1ee-e515fc3c9261
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 12%

---


# submitJob{#submitjob}

Envía un trabajo al sistema.

Sintaxis

## Tipos de usuarios autorizados {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-31a07dbccf964850883e817384499459}

**Entrada (submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> <p>Identificador de compañía. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Gestionar al usuario que envió el trabajo. </p> <p> <p>Nota: El sistema envía un correo electrónico al usuario especificado por <span class="codeph"> userHandle</span>. Si no se proporciona <span class="codeph"> userHandle</span>, la persona que envió el trabajo recibe los correos electrónicos. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> <p>Nombre de trabajo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>La configuración regional utilizada para los detalles del registro de trabajos y la localización por correo electrónico. </p> <p>Las configuraciones regionales se especifican como <span class="codeph"> &lt;language_code&gt;</span> y <span class="codeph"> [&lt;country_code&gt;]</span>, donde el código de idioma es un código de dos letras en minúscula, según lo especificado por ISO-639, y el código de país opcional es un código de dos letras en mayúsculas según lo especificado por ISO-3166. Por ejemplo, la cadena de configuración regional para inglés (Estados Unidos) sería: en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Fecha y hora de ejecución del trabajo. </p> <p>Nota:  Proporcione el huso horario con la solicitud. Los husos horarios se ajustan a la zona horaria del servidor IPS de destinatario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Determina cuándo ejecutar el trabajo. </p> <p> Puede ser una cadena <span class="codeph"> cron</span> que ejecute el trabajo de forma recurrente. </p> <p>La programación siempre es relativa al huso horario local del servidor. Consulte la documentación de IPS para obtener el formato de programación personalizado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Descripción del trabajo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ExportJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Exportar archivos cargados anteriormente. </p> <p>Consulte <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageServingPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Detalles de un trabajo de publicación de servicio de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Detalles de un trabajo de publicación de procesamiento de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:VideoPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Detalles de un trabajo de publicación de vídeo. </p> <p>Consulte <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Detalles de un trabajo de publicación de directorio de servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UploadDirectoryJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Detalles de un trabajo de directorio de carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UploadUrlsJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Detalles de un trabajo de URL de carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizedImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:OptimizeImagesJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:RipPdfsJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> AutomatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Procesar una lista de recursos en conjuntos mediante las secuencias de comandos de conjuntos automatizados. </p> <p>Consulte <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (submitJobReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`jobHandle`*` | `xsd:string` | Sí | Identificador de trabajo. |

## Ejemplos {#section-40ac77d14adf4588ba2575be6879b2d2}

Este ejemplo de código envía un trabajo de publicación de servicio de imágenes a IPS y devuelve un identificador de trabajo. Elija un solo tipo de trabajo en la solicitud. Debido a que `userHandle` se omitió, se envían notificaciones por correo electrónico al usuario que envió el trabajo. Este trabajo de ejemplo se ejecuta inmediatamente porque se omitieron `execTime` y `execSchedule`.

**Solicitar**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**Respuesta**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## Notas {#section-0f3078e503a249aeb6f3d662a51f036a}

Puede especificar como máximo uno de `execTime` y `execSchedule`. Si no se aprueba ninguna de estas opciones, el trabajo se ejecuta inmediatamente. Puede utilizar solo una de las siguientes opciones:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`

