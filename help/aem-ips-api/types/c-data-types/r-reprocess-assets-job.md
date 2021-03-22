---
description: Tipo de trabajo para permitir el reprocesamiento de archivos principales cargados anteriormente, incluida la recuperación de archivos PDF y la reoptimización de imágenes.
seo-description: Tipo de trabajo para permitir el reprocesamiento de archivos principales cargados anteriormente, incluida la recuperación de archivos PDF y la reoptimización de imágenes.
seo-title: ReprocessAssetsJob
solution: Experience Manager
title: ReprocessAssetsJob
uuid: 5b4aa838-0fb4-4ae8-be5a-8ce1e1487127
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 5%

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Identificador de recurso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Indica si los archivos están marcados como listos para publicarse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Controla si se conserva el estado de publicación de un recurso existente al sobrescribirlo. Si no se establece, se utiliza la configuración predeterminada de la empresa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Si se crea una máscara. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Controla la preservación de cualquier definición de recorte existente. El valor predeterminado es true.</p> <p>Si proporciona el parámetro manualCropOptions y los valores correspondientes, los nuevos valores (excepto 0,0,0,0) se aplican al recurso independientemente del valor preserveCrop.</p><p>Si <i>not</i> proporciona el parámetro manualCropOptions, se mantiene el valor de preserveCrop. Y, en el caso de true, se conservan los valores preserveCrop existentes; en el caso de false, se eliminan los valores preserveCrop .</p><p>Ejemplo:</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt;190&lt;/left&gt;<br />    &lt;right&gt;310&lt;/right&gt;<br />    &lt;top&gt;160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones de recorte manual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cultivos automáticos de imágenes basadas en el color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Elimina el espacio en blanco de los bordes de las imágenes, en función de la transparencia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cargar archivos Photoshop en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cargar archivos PostScript al servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cargar archivos PDF en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones del archivo multimedia A/V. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cargar archivos Illustrator en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones que se pueden especificar durante una carga. El conjunto afecta a cómo se administra el color para la carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>Matriz de secuencias de comandos de generación de conjuntos automáticas para aplicar a archivos cargados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Matriz de controladores de proyecto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Opciones de configuración de correo electrónico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Indica si cargar solo archivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Dirección URL de la ubicación de carga de archivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Los detalles del trabajo de un trabajo de publicación de servicio de imágenes se ejecutarán una vez finalizada la carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Los detalles del trabajo de un trabajo de publicación de renderización de imágenes se ejecutarán una vez finalizada la carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Los detalles del trabajo de un trabajo de publicación de vídeo se ejecutarán una vez finalizada la carga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Opciones para cargar archivos de InDesign en el servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Enmascara el fondo de las imágenes seleccionadas. Esto permite superponerlos en otras capas con una transparencia fuera de la imagen del sujeto. </p> <p>Opcional. </p> <p>Consulte<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unSharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:Opciones de máscara de enfoque</span> </p> </td> 
   <td colname="col3"> <p>Opciones que permiten controlar la configuración de máscara de enfoque al crear un archivo TIF piramidal optimizado. Utilice estos ajustes para mejorar el nitidez de la imagen. </p> <p>Consulte <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnSharpMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Notas**

Las opciones para `*CropOptions` incluyen:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Las opciones para `*PublishJob` incluyen:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

