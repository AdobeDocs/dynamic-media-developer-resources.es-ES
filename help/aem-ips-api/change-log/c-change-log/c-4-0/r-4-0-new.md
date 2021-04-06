---
description: Describe los cambios nuevos e implementados para la API de IPS v4.0.
solution: Experience Manager
title: Nuevas adiciones y cambios
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '1227'
ht-degree: 2%

---

# Nuevas adiciones y cambios{#new-additions-and-changes}

Describe los cambios nuevos e implementados para la API de IPS v4.0.

Se han implementado versiones de API en paralelo con WSDL independientes y espacios de nombres de esquema.

* Versiones anteriores de la API: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versión de SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Se ha añadido el campo `PostScriptOptions/alpha`.

Se han agregado las propiedades `VideoRootUrl` y `SwfRootUrl` para la operación `getProperty`.

Se han agregado parámetros opcionales `appName` y `appVersion` a `authHeader` para rastrear la llamada a la aplicación. Se ha agregado el registro a `ipsApiService.log`.

Se ha añadido un parámetro opcional `serviceUrl` al servlet de generación WSDL. Esto resulta especialmente útil para depurar proxies. Por ejemplo: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Se ha implementado la operación `getZipEntries`.

Se han implementado intervalos de búsqueda y se han escrito valores de comparación para las condiciones de campo del sistema.

Se ha agregado la constante de cadena de tipo de recurso `'Asset'`, principalmente para permitir campos de metadatos entre recursos.

Se ha implementado el parámetro `trashState` para `searchAssets`.

Se ha implementado la operación `getAssetPublishHistory`.

Se ha añadido el encabezado SOAP opcional `faultHttpStatusCode` para habilitar la gestión de errores en Flex. Para Flex, utilice `<faultHttpStatusCode>200</faultHttpStatusCode>`. El código de estado predeterminado para las respuestas de error es `500 (Internal Server Error)`.

Se agregaron operaciones para restaurar recursos de la papelera y vaciar recursos de la papelera.

Se han implementado operaciones de CRUD.

Se ha añadido el indicador habilitado al tipo `ImageMap` y a la operación `saveImageMap` .

Se ha agregado compatibilidad con los trabajos Optimizar archivos restantes .

Se ha agregado `setAssetsPublishState` para las actualizaciones de estado de publicación masiva.

Se ha añadido `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Operación `saveMetadataField` obsoleta en favor de nuevas operaciones `createMetadataField` y `updateMetadataField`.

Se ha implementado la operación de eliminación por lotes `deleteAssetsParam`.

Se ha implementado la operación de movimiento por lotes `moveAssetsParam`.

Se ha implementado la operación `deleteMetadataField`.

Se han implementado operaciones `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat`.

Implementado `getAssetCounts`.

Se ha agregado compatibilidad con `setImageSetMembers` para incluir miembros `RenderSet` en activos `ImageSet`.

Se ha agregado la operación `replaceImage`.

Se ha agregado la operación `copyImage`.

Se agregaron los campos operación `setUrlModifier` y `urlModifier/urlPostApplyModifier` para `LayerViewInfo`, `TemplateInfo` y `WatermarkInfo`.

Se ha agregado la operación `createDerivedAsset`. Actualmente, `ownerHandle` debe hacer referencia a un recurso de imagen y el tipo puede ser `AdjustedView` o `LayerView`.

Se ha agregado la operación `createTemplate`. Actualmente se puede llamar a esto para crear recursos de plantilla o de marca de agua.

Configuración de empresa IPS, `CompanySettings`, portada a la API de servicios web.

Se ha agregado el indicador de filtro `excludeByproducts` a la operación `searchAssets`. Al establecer este indicador en verdadero, se ejecutan `PSDlayer` imágenes y se copian en PDF.

Se ha agregado la operación `getGenerationInfo`.

Se ha agregado el nombre de propiedad `SystemMessage` a la operación `getProperty`.

Se han modificado algunas constantes de cadena de tipo de recurso para que coincidan con los campos correspondientes de Información de recurso .

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Se ha modificado el formato de resultado de las operaciones por lotes para resumir los errores, las advertencias y el éxito.

Se ha implementado la operación de metadatos por lotes `batchSetAssetMetadata`.

Se ha implementado compatibilidad con datos específicos de la aplicación.

Se ha implementado compatibilidad con marcas booleanas para `createTemplate`, `extendLayers` y `extractText` para trabajos de carga para controlar el proceso de procesamiento de Photoshop (similar a los cambios para agregar cargas de archivos).

Se han implementado operaciones `setImageMaps` y `setZoomTargets`.

Se han implementado operaciones `ViewerPreset`. Los tipos reconocidos son:

* `VideoPlayer` (El vídeo solo publica estos visores).
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Las máscaras del visor admiten dos parámetros: `skinFg` y `skinBg`. El código back-end realiza todo el procesamiento necesario para mantener la compatibilidad con versiones anteriores.

Se ha implementado la operación `getAssociatedAssets`.

Se ha agregado el tipo de trabajo `ReprocessAssets` para permitir el reprocesamiento de archivos de origen primarios cargados anteriormente, incluida la recuperación de archivos PDF y la reoptimización de imágenes.

Se cambió el nombre del tipo de campo `PropertySetType` a `propertyType`. Esto afecta al parámetro `createPropertySetType` y a la respuesta `getPropertySetType/getPropertySetTypes`.

Se ha implementado la operación `batchSetImageFields` para admitir la configuración de datos de usuario de imagen y otros campos de imagen editables.

47 Se ha agregado el campo fileSize a varios tipos de información de recursos:

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

Se ha implementado la operación `getActivePublishContexts`. Esta operación devuelve una matriz de nombres de contexto de publicación con servidores de publicación activos para la empresa especificada. Los nombres de contexto de publicación actuales son:

* `ImageServing`
* `ImageRendering`
* `Video`

Se ha implementado la operación `getSearchStrings`. Devuelve una matriz de cadenas de búsqueda para el recurso dado.

Se han agregado parámetros de configuración regional para trabajos y un mecanismo para establecer la configuración regional para las operaciones de API. La cadena de configuración regional debe tener el formato `<language_code>[-<country_code>]`. El código de idioma es un código de dos letras en minúsculas, tal como se especifica en la norma ISO-639, y el código de país opcional es un código de dos letras en mayúscula, tal como se especifica en la norma ISO-3166.

Se ha agregado un parámetro de configuración regional opcional al encabezado SOAP `authHeader` para establecer la configuración regional de las operaciones de API. Si este parámetro no está presente, se utilizará el encabezado HTTP `Accept-Language`. Si este encabezado tampoco está presente, se utilizará la configuración regional predeterminada para el servidor IPS.

Se ha agregado compatibilidad con get/set para campos de metadatos con establecimiento inflexible de tipos.

Se ha implementado compatibilidad con encabezados SOAP y HTTP para el control de respuestas gzip.

Se ha agregado el indicador `gzipResponse` a `authHeader`. Si no está presente, la API también comprobará el encabezado HTTP `Accept-Encoding`.

Se agregó compatibilidad con searchAssets para condiciones de campo de metadatos con establecimiento inflexible de tipos.

* Para todos los tipos de campo, el valor se puede pasar con un operador de comparación de cadenas ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Para los campos booleanos, `boolVal` se puede pasar con la `Equals` op.
* Para los campos Int, `longVal` puede pasarse con un operador de comparación numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minLong/maxLong` puede pasarse con una operación de rango numérico ( `Between, NotBetween`).
* En los campos Float, `doubleVal` puede pasarse con un operador de comparación numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minDouble/maxDouble` puede pasarse con una operación de rango numérico ( `Between, NotBetween`).
* En los campos Fecha, puede pasar `dateVal` con un operador de comparación numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o minDate/maxDate con operaciones de rango numérico ( `Between, NotBetween`).

Se han añadido los campos descripción, `jobSubType` y `originalJobName` al tipo `JobLog` .

* `originalJobName` es el nombre del trabajo enviado a  `submitJob` (sin sufijos de exclusividad ni nombres de trabajo de seguimiento).
* `jobSubType` actualmente solo se utiliza en  `ImageServingPublishJob` trabajos (donde es de  `full`,  `increment, fullwithsearch,` o  `fulloverride`).
* `description` es actualmente una cadena vacía para todos los tipos de trabajo, pero finalmente contiene información resumida del trabajo, como la ruta de carga.

Además, los campos siguientes no se incluyen en `getJobLogs` ni en `getJobLogDetails`. En versiones anteriores solo estaban disponibles con `getJobLogDetails`.

* `endDate` (si el trabajo se ha completado).
* `fileDuplicateCount` (anteriormente siempre estaba  `0` con  `getJobLogs`)
* `fileUpdateCount` (anteriormente siempre se incluía  `0` en  `getJobLogs` y se incluía en  `fileSuccessCount`; ahora se divide en campos separados).

Se ha agregado el campo assetHandle al tipo `JobLogDetail`.

Se ha agregado un parámetro de descripción opcional a `submitJob`. Esto se transfiere para su recuperación en `getScheduledJobs`, `getActiveJobs` y `getJobLogs`.

Se ha desaprobado el campo del sistema de SKU. El campo se ignora si se pasa como `SystemFieldCondition` a `searchAssets`.

Se ha agregado el filtro `excludeAssetTypeArray` a `searchAssets`.

Se ha agregado el tipo `MaskInfo` a `Asset`.

Se agregaron nuevos tipos de activos para la administración mediante IPS:

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tipo de recurso </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Archivo Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>Archivos EPS y PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento de Microsoft Word para archivos que terminan con .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento de Microsoft Excel para archivos que terminan con .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento de Microsoft PowerPoint para archivos que terminan con .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>Archivo RTF para archivos cargados que terminan con .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Se han agregado opciones adicionales a `UploadDirectoryJob` y `UploadUrlsJob` para controlar el procesamiento de archivos Postscript, Illustrator y PDF de forma independiente. Todos los trabajos existentes proporcionarán los parámetros necesarios a cada una de las 3 canalizaciones de procesamiento para que funcionen exactamente como se hace hoy. El bloque `PostScriptOptions` original se utiliza para configurar el procesamiento de los archivos Illustrator y EPS/PS. Opcionalmente, se pueden proporcionar bloques de opciones de archivo específicos para especificar el procesamiento. La lista de cambios incluye:

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Campo </p> </th> 
   <th colname="col2" class="entry"> <p>Parámetro </p> </th> 
   <th colname="col3" class="entry"> <p>Valor </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proceso </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Ninguno </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterizar  </span>(predeterminado) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Administre solo el activo y no cree ningún derivado al cargarlo. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Procese el archivo EPS y PostScript en una imagen con la resolución y el espacio de color prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Tiene efecto al rasterizar el archivo en una imagen. Creará un fondo transparente si el archivo original está definido de esta manera para superponer logotipos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proceso </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Ninguno </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterizar  </span> (predeterminado) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Administre solo el activo y no cree ningún derivado al cargarlo. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Procese el archivo en una imagen con la resolución y el espacio de color prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entero&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterización de la resolución. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Espacio de color </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espacio de color de destino para la renderización. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa  </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Tiene efecto al rasterizar el archivo en una imagen. Crea un fondo transparente si el archivo original está definido de esta manera para crear logotipos superpuestos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proceso </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Ninguno </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterizar  </span> (predeterminado) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Administre solo el activo y no cree ningún derivado al cargarlo. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Procese el archivo en una imagen con la resolución y el espacio de color prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entero&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterización de la resolución. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Espacio de color </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espacio de color de destino para la renderización. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define si se desea combinar un PDF de varias páginas en un catálogo electrónico después de la representación (el valor predeterminado es true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define si las palabras del PDF se extraen en la base de datos para suministrarlas posteriormente a un servidor de búsqueda (el valor predeterminado es false). </p> </td> 
  </tr> 
 </tbody> 
</table>

También puede realizar consultas desde `getScheduledJobs`.

Se ha modificado la propiedad de configuración `webservice.gzip.response` para tomar uno de los siguientes valores:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nunca </span> </p> </td> 
   <td colname="col2"> <p>No escriba la respuesta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap </span> </p> </td> 
   <td colname="col2"> <p>La respuesta de Gzip solo es verdadera si authHeader/gzipResponse es verdadera. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aceptar </span> </p> </td> 
   <td colname="col2"> <p>Gzip si authHeader/gzipResponse es true, o si no hay ningún encabezado gzipResponse y el encabezado Accept-Encoding de HTTP incluye gzip. (Predeterminado). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> siempre </span> </p> </td> 
   <td colname="col2"> <p>Siempre gzip response, independientemente de los valores de encabezado. Utilice este valor solo para la depuración. </p> </td> 
  </tr> 
 </tbody> 
</table>
