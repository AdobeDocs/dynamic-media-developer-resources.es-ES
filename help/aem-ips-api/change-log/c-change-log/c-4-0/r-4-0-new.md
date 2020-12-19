---
description: Describe los cambios nuevos e implementados para la API de IPS v4.0.
seo-description: Describe los cambios nuevos e implementados para la API de IPS v4.0.
seo-title: Nuevas adiciones y cambios
solution: Experience Manager
title: Nuevas adiciones y cambios
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 2%

---


# Nuevas adiciones y cambios{#new-additions-and-changes}

Describe los cambios nuevos e implementados para la API de IPS v4.0.

Se han implementado versiones de API paralelas con WSDL y Áreas de nombres de esquema independientes.

* Versiones de API anteriores: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versión de SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Campo añadido `PostScriptOptions/alpha`.

Propiedades `VideoRootUrl` y `SwfRootUrl` añadidas para la operación `getProperty`.

Se añadieron parámetros opcionales `appName` y `appVersion` a `authHeader` para rastrear la aplicación de llamada. Registro añadido en `ipsApiService.log`.

Se añadió un parámetro `serviceUrl` opcional al servlet de generación WSDL. Esto resulta especialmente útil para los proxies de depuración. Por ejemplo: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Se implementó la operación `getZipEntries`.

Se implementaron rangos de búsqueda y valores de comparación escritos para las condiciones de campo del sistema.

Constante de cadena de tipo de recurso `'Asset'` añadida, principalmente para permitir campos de metadatos entre recursos.

Se implementó el parámetro `trashState` para `searchAssets`.

Se implementó la operación `getAssetPublishHistory`.

Se añadió el encabezado opcional `faultHttpStatusCode` SOAP para habilitar la gestión de errores en Flex. Para Flex, utilice `<faultHttpStatusCode>200</faultHttpStatusCode>`. El código de estado predeterminado para las respuestas a errores es `500 (Internal Server Error)`.

Operaciones añadidas para restaurar recursos de la papelera y recursos vacíos de la papelera.

Se han implementado operaciones de CRUD.

Se ha añadido el indicador habilitado para el tipo `ImageMap` y la operación `saveImageMap`.

Se añadió la compatibilidad con los trabajos de Optimización de archivos restantes.

Se añadió `setAssetsPublishState` para actualizaciones de estado de publicación masiva.

Se añadieron `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Operación `saveMetadataField` desaprobada en favor de nuevas operaciones `createMetadataField` y `updateMetadataField`.

Se implementó la operación de eliminación por lotes `deleteAssetsParam`.

Se implementó la operación de movimiento por lotes `moveAssetsParam`.

Se implementó la operación `deleteMetadataField`.

Se implementaron operaciones `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat`.

Implementado `getAssetCounts`.

Se añadió la compatibilidad con `setImageSetMembers` para incluir `RenderSet` miembros en `ImageSet` recursos.

Operación `replaceImage` añadida.

Operación `copyImage` añadida.

Se añadieron los campos de operación `setUrlModifier` y `urlModifier/urlPostApplyModifier` para `LayerViewInfo`, `TemplateInfo` y `WatermarkInfo`.

Operación `createDerivedAsset` añadida. Actualmente, `ownerHandle` debe hacer referencia a un recurso de imagen y el tipo puede ser `AdjustedView` o `LayerView`.

Operación `createTemplate` añadida. Actualmente se puede llamar a esto para crear recursos de plantilla o marca de agua.

Configuración de compañía IPS, `CompanySettings`, portada a la API de servicios Web.

Se añadió el indicador de filtro `excludeByproducts` en la operación `searchAssets`. Al establecer este indicador en true, se ejecutan `PSDlayer` imágenes y se extraen imágenes en PDF.

Operación `getGenerationInfo` añadida.

Se añadió el nombre de la propiedad `SystemMessage` en la operación `getProperty`.

Se han modificado algunas constantes de cadena de tipo de recurso para que coincidan con los campos de información de recurso correspondientes.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Se ha modificado el formato de resultado de las operaciones por lotes para resumir los errores, las advertencias y el éxito.

Se implementó la operación de metadatos por lotes `batchSetAssetMetadata`.

Se ha implementado la compatibilidad con datos específicos de la aplicación.

Se implementó compatibilidad con marcas booleanas para `createTemplate`, `extendLayers` y `extractText` para trabajos de carga para controlar el proceso de procesamiento de Photoshop (similar a los cambios para agregar cargas de archivos).

Se implementaron operaciones `setImageMaps` y `setZoomTargets`.

Se implementaron operaciones `ViewerPreset`. Los tipos reconocidos son:

* `VideoPlayer` (El vídeo solo publica estos visores).
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Las apariencias de visor admiten dos parámetros: `skinFg` y `skinBg`. El código back-end realizará todo el procesamiento necesario para mantener la compatibilidad con versiones anteriores.

Se implementó la operación `getAssociatedAssets`.

Se añadió el tipo de trabajo `ReprocessAssets` para permitir el reprocesamiento de archivos de origen principales cargados anteriormente, incluida la recuperación de archivos PDF y la reoptimización de imágenes.

Se cambió el nombre del tipo de campo `PropertySetType` a `propertyType`. Esto afecta al parámetro `createPropertySetType` y a la respuesta `getPropertySetType/getPropertySetTypes`.

Se implementó la operación `batchSetImageFields` para admitir la configuración de datos de usuario de imagen y otros campos de imagen editables.

47 campo fileSize Añadido a varios tipos de información de recursos:

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

Se implementó la operación `getActivePublishContexts`. Esta operación devuelve una matriz de nombres de contexto de publicación con servidores de publicación activos para la compañía especificada. Los nombres de contexto de publicación actuales son:

* `ImageServing`
* `ImageRendering`
* `Video`

Se implementó la operación `getSearchStrings`. Devuelve una matriz de cadenas de búsqueda para el recurso dado.

Parámetros de configuración regional añadidos para trabajos y un mecanismo para establecer la configuración regional para las operaciones de API. La cadena de configuración regional debe tener el formato `<language_code>[-<country_code>]`. El código de idioma es un código de dos letras en minúsculas, tal como se especifica en ISO-639, y el código de país opcional es un código de dos letras en mayúscula, tal como se especifica en ISO-3166.

Se añadió el parámetro de configuración regional opcional en el encabezado `authHeader` SOAP para establecer la configuración regional de las operaciones de API. Si este parámetro no está presente, se utilizará el encabezado HTTP `Accept-Language`. Si este encabezado tampoco está presente, se utilizará la configuración regional predeterminada para el servidor IPS.

Compatibilidad añadida con get/set para campos de metadatos con establecimiento inflexible de tipos.

Se implementó la compatibilidad con encabezados SOAP y HTTP para el control de respuesta gzip.

Se añadió el indicador `gzipResponse` en `authHeader`. Si no está presente, la API también comprobará el encabezado HTTP `Accept-Encoding`.

Compatibilidad añadida con searchAssets para condiciones de campo de metadatos con establecimiento inflexible de tipos.

* Para todos los tipos de campo, el valor se puede pasar con un operador de comparación de cadenas ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Para los campos booleanos, `boolVal` puede pasarse con la operación `Equals`.
* Para los campos Int, `longVal` puede pasarse con un operador de comparación numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minLong/maxLong` puede pasarse con operaciones de rango numérico ( `Between, NotBetween`).
* Para los campos Float, `doubleVal` puede pasarse con un operador de comparación numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minDouble/maxDouble` puede pasarse con operaciones de rango numérico ( `Between, NotBetween`).
* Para los campos Fecha, puede pasar `dateVal` con un operador de comparación numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o puede pasar minDate/maxDate con operaciones de rango numérico ( `Between, NotBetween`).

Se añadieron los campos description, `jobSubType` y `originalJobName` al tipo `JobLog`.

* `originalJobName` es el nombre del trabajo enviado a  `submitJob` (sin sufijos de exclusividad ni nombres de trabajos posteriores).
* `jobSubType` actualmente solo lo utilizan  `ImageServingPublishJob` los trabajos (donde es uno de  `full`,  `increment, fullwithsearch,` o  `fulloverride`).
* `description` es una cadena vacía para todos los tipos de trabajos, pero finalmente contendrá información resumida del trabajo, como la ruta de carga.

Además, los siguientes campos no se incluyen con `getJobLogs` ni con `getJobLogDetails`. En versiones anteriores, solo estaban disponibles con `getJobLogDetails`.

* `endDate` (si se ha completado el trabajo).
* `fileDuplicateCount` (anteriormente siempre estaba  `0` con  `getJobLogs`)
* `fileUpdateCount` (anteriormente siempre estaba  `0` con  `getJobLogs` e incluido en  `fileSuccessCount`; ahora se divide en campos independientes).

Se añadió el campo assetHandle al tipo `JobLogDetail`.

Se añadió el parámetro de descripción opcional a `submitJob`. Esto se pasa a través de la recuperación en `getScheduledJobs`, `getActiveJobs` y `getJobLogs`.

Ya no se utiliza el campo del sistema SKU. El campo se omite si se pasa como `SystemFieldCondition` a `searchAssets`.

Se añadió el filtro `excludeAssetTypeArray` a `searchAssets`.

Se añadió el tipo `MaskInfo` a `Asset`.

Nuevos tipos de recursos añadidos para administración por IPS:

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
   <td colname="col2"> <p>Documento de Microsoft Word para los archivos que finalizan con .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento de Microsoft Excel para los archivos que finalizan con .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>Documento de Microsoft PowerPoint para archivos que terminan con .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>Archivo RTF para archivos cargados que finalizan con .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Se han añadido opciones adicionales a `UploadDirectoryJob` y `UploadUrlsJob` para controlar el procesamiento de archivos Postscript, Illustrator y PDF de forma independiente. Todos los trabajos existentes proporcionarán los parámetros necesarios a cada uno de los 3 gasoductos de procesamiento para que funcionen exactamente como se hace hoy. El bloque `PostScriptOptions` original se utiliza para definir el procesamiento de los archivos Illustrator y EPS/PS. Opcionalmente, se pueden suministrar bloques de opciones de archivo específicos para especificar el procesamiento. La lista de cambios incluye:

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
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Gestionar solo el activo y no crear ningún derivado al cargarlo. </p> </li> 
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
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Gestionar solo el activo y no crear ningún derivado al cargarlo. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Procese el archivo en una imagen con la resolución y el espacio de color establecidos. </p> </li> 
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
   <td colname="col4"> <p>Espacio de color del destinatario para la representación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha  </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Afecta al rasterizar el archivo en una imagen. Crea un fondo transparente si el archivo original está definido de esta manera para crear logotipos superpuestos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOoptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proceso </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Ninguno </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterizar  </span> (predeterminado) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Gestionar solo el activo y no crear ningún derivado al cargarlo. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Procese el archivo en una imagen con la resolución y el espacio de color establecidos. </p> </li> 
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
   <td colname="col4"> <p>Espacio de color del destinatario para la representación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define si se debe combinar un PDF de varias páginas en un catálogo electrónico después del procesamiento (el valor predeterminado es true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define si las palabras del PDF se extraen en la base de datos para luego suministrarlas a un servidor de búsqueda (el valor predeterminado es false). </p> </td> 
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
   <td colname="col2"> <p>No gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap </span> </p> </td> 
   <td colname="col2"> <p>La respuesta de Gzip solo se produce si authHeader/gzipResponse es true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aceptar </span> </p> </td> 
   <td colname="col2"> <p>Gzip si authHeader/gzipResponse es true o no hay ningún encabezado gzipResponse y el encabezado Accept-Encoding HTTP incluye gzip. (Predeterminado). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> siempre </span> </p> </td> 
   <td colname="col2"> <p>Siempre gzip, independientemente de los valores del encabezado. Utilice este valor solo para fines de depuración. </p> </td> 
  </tr> 
 </tbody> 
</table>

