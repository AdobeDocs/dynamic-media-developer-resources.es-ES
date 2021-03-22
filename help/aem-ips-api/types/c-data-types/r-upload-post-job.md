---
description: Utiliza getActiveJobs para rastrear las cargas de escritorio.
seo-description: Utiliza getActiveJobs para rastrear las cargas de escritorio.
seo-title: UploadPostJob
solution: Experience Manager
title: UploadPostJob
uuid: 172f47c7-685a-4014-9c30-dacd78733655
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 10%

---


# UploadPostJob{#uploadpostjob}

Utiliza getActiveJobs para rastrear las cargas de escritorio.

Consulte también [Carga de recursos mediante HTTP POST a la carga...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Todas las solicitudes de POST de un trabajo de carga deben proceder de la misma dirección IP.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatorio? </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para cultivos automáticos de imágenes basadas en el color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de secuencias de comandos de generación de conjuntos automáticas para aplicar a archivos cargados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Elimina el espacio en blanco de los bordes de las imágenes, en función de la transparencia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones que se pueden especificar durante una carga. El conjunto afecta a cómo se administra el color para la carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Sí</b> </p> </td> 
   <td colname="col4"> <p>Si se crea una máscara. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>Sí</b> </p> </td> 
   <td colname="col4"> <p>Elección de la configuración del correo electrónico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:InDesignOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para cargar archivos de InDesign en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para cargar archivos Illustrator en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Enmascara el fondo de las imágenes seleccionadas. Esto permite superponerlos en otras capas con una transparencia fuera de la imagen del sujeto. Opcional. </p> <p>Consulte<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para cultivos manuales de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MediaOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones que permiten establecer una imagen en miniatura del vídeo. </p> <p>Consulte <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sobrescribir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Sí</p> </td> 
   <td colname="col4"> <p>Si se sobrescriben los archivos al cargarlos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PDFOptions</span> </td> 
   <td colname="col3"> <p>No</p> </td> 
   <td colname="col4"> <p>Opciones para cargar archivos PDF en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para cargar archivos Photoshop en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Dirección URL donde se cargan los archivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para cargar archivos de Post Script al servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Controla la preservación de cualquier definición de recorte existente. El valor predeterminado es true.</p> <p>Si proporciona el parámetro manualCropOptions y los valores correspondientes, los nuevos valores (excepto 0,0,0,0) se aplican al recurso independientemente del valor preserveCrop.</p><p>Si <i>not</i> proporciona el parámetro manualCropOptions, se mantiene el valor de preserveCrop. Y, en el caso de true, se conservan los valores preserveCrop existentes; en el caso de false, se eliminan los valores preserveCrop .</p><p>Ejemplo:</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt;190&lt;/left&gt;<br />    &lt;right&gt;310&lt;/right&gt;<br />    &lt;top&gt;160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Sí</b> </p> </td> 
   <td colname="col4"> <p>Controla si se conserva el estado de publicación de un recurso existente al sobrescribirlo. Si no se establece, se utiliza la configuración predeterminada de la empresa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de controladores de proyecto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Sí</b> </p> </td> 
   <td colname="col4"> <p>Indica si los archivos están marcados como listos para publicarse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UncompressOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Extraiga y procese el contenido de los archivos TAR/ZIP cargados con esta configuración opcional. </p> <p>Consulte <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> DescompresiónOpciones</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unSharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:Opciones de máscara de enfoque</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones que permiten controlar la configuración de máscara de enfoque al crear un archivo TIF piramidal optimizado. Utilice estos ajustes para mejorar el nitidez de la imagen. </p> <p>Consulte <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnSharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Una opción de metadatos adicional para todo el trabajo de carga. </p> </td> 
  </tr> 
 </tbody> 
</table>

