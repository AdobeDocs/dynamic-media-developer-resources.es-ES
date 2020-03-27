---
description: Tipo de trabajo para permitir el reprocesamiento de archivos principales cargados anteriormente, incluida la recuperación de archivos PDF y la reoptimización de imágenes.
seo-description: Tipo de trabajo para permitir el reprocesamiento de archivos principales cargados anteriormente, incluida la recuperación de archivos PDF y la reoptimización de imágenes.
seo-title: ReprocessAssetsJob
solution: Experience Manager
title: ReprocessAssetsJob
topic: Scene7 Image Production System API
uuid: 5b4aa838-0fb4-4ae8-be5a-8ce1e1487127
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ReprocessAssetsJob{#reprocessassetsjob}

Tipo de trabajo para permitir el reprocesamiento de archivos principales cargados anteriormente, incluida la recuperación de archivos PDF y la reoptimización de imágenes.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Identificador de recurso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Indica si los archivos están marcados para publicación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Controla si se conserva el estado de publicación de un recurso existente al sobrescribir. Si no se establece, se utiliza la configuración predeterminada de compañía. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Si se va a crear una máscara. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3">Controla la preservación de cualquier definición de cultivo existente. El valor predeterminado es <span class="codeph"> true</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones de recorte manual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para recortes automáticos de imágenes en función del color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Elimina el espacio en blanco de los bordes de las imágenes, en función de la transparencia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cargar archivos de Photoshop en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cargar archivos PostScript en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:PDFOoptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cargar archivos PDF al servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones de archivo multimedia A/V. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> IllustratorOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cargar archivos de Illustrator en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones que puede especificar durante una carga. El conjunto afecta a la forma en que se administra el color para la carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>Matriz de secuencias de comandos de generación automática de conjuntos para aplicar a archivos cargados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Matriz de controladores de proyecto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Opciones de configuración de correo electrónico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Indica si se cargarán solo archivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Dirección URL de la ubicación de carga de archivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Los detalles del trabajo de un trabajo de publicación de servicio de imágenes se ejecutarán una vez finalizada la carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Los detalles del trabajo de un trabajo de publicación de procesamiento de imágenes se ejecutarán una vez finalizada la carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Los detalles del trabajo de un trabajo de publicación de vídeo se ejecutarán una vez finalizada la carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cargar archivos de InDesign en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Máscara el fondo de las imágenes seleccionadas. Esto permite superponerlos en otras capas con una transparencia fuera de la imagen del sujeto. </p> <p>Opcional. </p> <p>Consulte<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones que permiten controlar la configuración de la máscara de enfoque al crear un archivo TIF piramidal optimizado. Utilice esta configuración para mejorar el enfoque de la imagen. </p> <p>Consulte <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Notas**

Las opciones para `*CropOptions` incluir son:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Las opciones para `*PublishJob` incluir son:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

