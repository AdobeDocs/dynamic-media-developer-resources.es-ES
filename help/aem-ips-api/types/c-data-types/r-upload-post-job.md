---
description: Utiliza getActiveJobs para realizar un seguimiento de las cargas de escritorio.
solution: Experience Manager
title: UploadPostJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 10%

---

# [!DNL UploadPostJob]{#uploadpostjob}

Utiliza getActiveJobs para realizar un seguimiento de las cargas de escritorio.

Consulte también [Cargando recursos mediante HTTP POST en la carga...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Todas las solicitudes de POST para un trabajo de carga deben proceder de la misma dirección IP.

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
   <td colname="col4"> <p>Opciones para recortes automáticos de imágenes según el color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de scripts automáticos de generación de conjunto que se aplican a los archivos cargados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Elimina el espacio en blanco de los bordes de las imágenes en función de la transparencia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones que se pueden especificar durante una carga. El conjunto afecta a la forma en que se administra el color para la carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Sí</b> </p> </td> 
   <td colname="col4"> <p>Si se va a crear una máscara. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>Sí</b> </p> </td> 
   <td colname="col4"> <p>Opción de configuración de correo electrónico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:InDesignOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para cargar archivos de InDesign en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Opciones de Illustrator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:Opciones de Illustrator</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para cargar archivos de Illustrator en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:OpcionesFondoCobertura</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Enmascarar el fondo de las imágenes seleccionadas. Esto permite superponerlas en otras capas con una transparencia fuera de la imagen del sujeto. Opcional. </p> <p>Consulte<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para recortes manuales de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:OpcionesMedios</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones que permiten establecer una imagen en miniatura del vídeo. </p> <p>Consulte <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> OpcionesDeMedios</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sobrescribir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Sí</p> </td> 
   <td colname="col4"> <p>Indica si se sobrescribirán los archivos al cargarlos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PDFOptions</span> </td> 
   <td colname="col3"> <p>No</p> </td> 
   <td colname="col4"> <p>Opciones para cargar archivos del PDF en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para cargar archivos de Photoshop en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Dirección URL donde se cargan los archivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:OpcionesPostScript</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones para cargar archivos Post Script en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Controla la conservación de cualquier definición de recorte existente. El valor predeterminado es true.</p> <p>Si proporciona el parámetro manualCropOptions y los valores correspondientes, los nuevos valores (excluyendo 0,0,0,0) se aplicarán al recurso independientemente del valor preserveCrop.</p><p>Si lo hace <i>no</i> Si se proporciona el parámetro manualCropOptions, se mantiene el valor de preserveCrop. Y, en caso de true, se conservan los valores preserveCrop existentes; en caso de false, se eliminan los valores preserveCrop.</p><p>Ejemplo:</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Sí</b> </p> </td> 
   <td colname="col4"> <p>Controla si el estado de publicación de un recurso existente se conserva al sobrescribirlo. Si no se configura, se utiliza la configuración predeterminada de la empresa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de identificadores de proyecto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Sí</b> </p> </td> 
   <td colname="col4"> <p>Indica si los archivos están marcados como listos para publicar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uncompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:NoComprimirOpciones</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Extraiga y procese el contenido de los archivos TAR/ZIP cargados con esta configuración opcional. </p> <p>Consulte <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> DescomprimirOpciones</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:OpcionesMáscaraDeEnfoque</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Opciones que permiten controlar los ajustes de máscara de enfoque al crear un archivo TIF piramidal optimizado. Utilice esta configuración para mejorar la nitidez de la imagen. </p> <p>Consulte <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Una opción de metadatos adicional para todo el trabajo de carga. </p> </td> 
  </tr> 
 </tbody> 
</table>
