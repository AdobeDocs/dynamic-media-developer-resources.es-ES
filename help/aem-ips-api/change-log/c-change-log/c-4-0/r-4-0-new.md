---
title: Nuevas adiciones y cambios
description: Describe cambios nuevos e implementados para la API IPS 4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# Nuevas adiciones y cambios{#new-additions-and-changes}

Describe cambios nuevos e implementados para la API IPS 4.0.

Se han implementado versiones de API en paralelo con WSDL y áreas de nombres de esquema independientes.

* Versiones de API anteriores: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versión de SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Se agregó el campo `PostScriptOptions/alpha`.

Se agregaron las propiedades `VideoRootUrl` y `SwfRootUrl` para la operación `getProperty`.

Se agregaron `appName` y `appVersion` parámetros opcionales a `authHeader` para realizar el seguimiento de la aplicación que realiza la llamada. Se agregó el registro a `ipsApiService.log`.

Se ha agregado un parámetro `serviceUrl` opcional al servlet de generación de WSDL. Este parámetro es útil para depurar proxies. Por ejemplo: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Se implementó la operación `getZipEntries`.

Se implementaron rangos de búsqueda y valores de comparación ingresados para las condiciones de campo del sistema.

Se agregó `'Asset'` constante de cadena de tipo de recurso, principalmente para permitir campos de metadatos entre recursos.

Se implementó el parámetro `trashState` para `searchAssets`.

Se implementó la operación `getAssetPublishHistory`.

Se agregó el encabezado opcional de SOAP `faultHttpStatusCode` para habilitar la administración de errores en Flex. Para Flex, use `<faultHttpStatusCode>200</faultHttpStatusCode>`. El código de estado predeterminado para las respuestas de errores es `500 (Internal Server Error)`.

Se han añadido operaciones para restaurar recursos de la papelera y vaciar recursos de la papelera.

Implementó operaciones de CRUD.

Se agregó la marca habilitada al tipo `ImageMap` y a la operación `saveImageMap`.

Se ha agregado compatibilidad con los trabajos de Optimizar archivos restantes.

Se agregó `setAssetsPublishState` para actualizaciones de estado de publicación en lotes.

Se agregó `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Operación `saveMetadataField` obsoleta en favor de nuevas operaciones `createMetadataField` y `updateMetadataField`.

Se implementó `deleteAssetsParam` operación de eliminación por lotes.

Se implementó la operación de movimiento por lotes de `moveAssetsParam`.

Se implementó la operación `deleteMetadataField`.

Se implementaron `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` operaciones.

Se implementó `getAssetCounts`.

Se agregó compatibilidad con `setImageSetMembers` para incluir `RenderSet` miembros en `ImageSet` recursos.

Se agregó la operación `replaceImage`.

Se agregó la operación `copyImage`.

Se agregaron la operación `setUrlModifier` y `urlModifier/urlPostApplyModifier` campos para `LayerViewInfo`, `TemplateInfo` y `WatermarkInfo`.

Se agregó la operación `createDerivedAsset`. Actualmente, `ownerHandle` debe hacer referencia a un recurso de imagen y el tipo puede ser `AdjustedView` o `LayerView`.

Se agregó la operación `createTemplate`. Llame a para crear recursos de plantilla o marca de agua.

Configuración de empresa de IPS, `CompanySettings`, transferida a la API de servicios web.

Se agregó el indicador de filtro `excludeByproducts` a la operación `searchAssets`. Si se establece este indicador como verdadero, se ejecutan `PSDlayer` imágenes e imágenes copiadas desde PDF.

Se agregó la operación `getGenerationInfo`.

Se agregó el nombre de propiedad `SystemMessage` a la operación `getProperty`.

Se han modificado algunas constantes de cadena de tipo de recurso para que coincidan con los campos de información de recurso correspondientes.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Se ha modificado el formato de resultado de las operaciones por lotes para resumir el éxito, las advertencias y los errores.

Se implementó la operación de metadatos por lotes `batchSetAssetMetadata`.

Se ha implementado compatibilidad con datos específicos de la aplicación.

Se ha implementado compatibilidad con indicadores booleanos para `createTemplate`, `extendLayers` y `extractText` para trabajos de carga para controlar el proceso de procesamiento de Photoshop (similar a los cambios para agregar cargas de archivos).

Se implementaron `setImageMaps` y `setZoomTargets` operaciones.

Se implementaron `ViewerPreset` operaciones. Los tipos reconocidos son:

* `VideoPlayer` (el vídeo solo publica estos visores).
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Las máscaras del visor admiten dos parámetros: `skinFg` y `skinBg`. El código back-end realiza todo el procesamiento necesario para mantener la compatibilidad con versiones anteriores.

Se implementó la operación `getAssociatedAssets`.

Se ha agregado el tipo de trabajo `ReprocessAssets` para permitir el reprocesamiento de archivos de origen principales cargados anteriormente, incluida la copia de archivos PDF y la reoptimización de imágenes.

Se cambió el nombre del tipo de campo `PropertySetType` a `propertyType`. Este cambio de nombre afecta al parámetro `createPropertySetType` y a la respuesta `getPropertySetType/getPropertySetTypes`.

Se implementó la operación `batchSetImageFields` para admitir la configuración de datos de usuario de imagen y otros campos de imagen editables.

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

Se implementó la operación `getActivePublishContexts`. Esta operación devuelve una matriz de nombres de contexto de publicación con servidores de publicación activos para la empresa especificada. Los nombres de contexto de publicación actuales son:

* `ImageServing`
* `ImageRendering`
* `Video`

Se implementó la operación `getSearchStrings`. Devuelve una matriz de cadenas de búsqueda para el recurso determinado.

Se han agregado parámetros de configuración regional para trabajos y un mecanismo para establecer la configuración regional de operaciones de API. La cadena de configuración regional debe tener el formato `<language_code>[-<country_code>]`. El código de idioma es un código en minúsculas de dos letras como se especifica en la norma ISO-639, y el código de país opcional es un código en mayúsculas de dos letras como se especifica en la norma ISO-3166.

Se ha agregado un parámetro de configuración regional opcional al encabezado de SOAP `authHeader` para establecer la configuración regional de las operaciones de API. Si este parámetro no está presente, se utiliza el encabezado HTTP `Accept-Language`. Si este encabezado tampoco está presente, se utilizará la configuración regional predeterminada del servidor IPS.

Se ha agregado la compatibilidad de obtener/establecer para campos de metadatos con establecimiento inflexible de tipos.

Se ha implementado compatibilidad con encabezados HTTP y SOAP para el control de respuesta gzip.

Se agregó la marca `gzipResponse` a `authHeader`. Si no está presente, la API comprueba el encabezado HTTP `Accept-Encoding`.

Se ha agregado compatibilidad para buscar recursos en condiciones de campo de metadatos con establecimiento inflexible de tipos.

* Para todos los tipos de campo, el valor se puede pasar con un operador de comparación de cadenas ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Para los campos booleanos, `boolVal` se puede pasar con la operación `Equals`.
* Para los campos Ent, `longVal` se puede pasar con un operador de comparación numérica (`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minLong/maxLong` con operaciones de intervalo numérico (`Between, NotBetween`).
* Para los campos Flotante, `doubleVal` se puede pasar con un operador de comparación numérica (`Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minDouble/maxDouble` con operaciones de intervalo numérico (`Between, NotBetween`).
* Para los campos Fecha, puede pasar `dateVal` con un operador de comparación numérica ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o minDate/maxDate con operaciones de intervalo numérico ( `Between, NotBetween`).

Se agregaron los campos de descripción `jobSubType` y `originalJobName` al tipo `JobLog`.

* `originalJobName` es el nombre de trabajo enviado a `submitJob` (sin sufijos de exclusividad ni nombres de trabajo de seguimiento).
* `jobSubType` solo lo usan `ImageServingPublishJob` trabajos (donde es uno de `full`, `increment, fullwithsearch,` o `fulloverride`).
* `description` es una cadena vacía para todos los tipos de trabajos, pero finalmente contiene información de trabajo de resumen, como la ruta de carga.

Además, los campos siguientes no se incluyen con `getJobLogs` y `getJobLogDetails`. En versiones anteriores, solo estaban disponibles con `getJobLogDetails`.

* `endDate` (si el trabajo se ha completado).
* `fileDuplicateCount` (anteriormente siempre era `0` con `getJobLogs`)
* `fileUpdateCount` (anteriormente era siempre `0` con `getJobLogs` e incluido en `fileSuccessCount`; ahora se divide en campos separados).

Se agregó el campo assetHandle al tipo `JobLogDetail`.

Se agregó un parámetro de descripción opcional a `submitJob`. Este parámetro se pasó para su recuperación en `getScheduledJobs`, `getActiveJobs` y `getJobLogs`.

Obsoleto en el campo del sistema SKU. El campo se omitirá si se pasa como `SystemFieldCondition` a `searchAssets`.

Se agregó el filtro `excludeAssetTypeArray` a `searchAssets`.

Se agregó el tipo `MaskInfo` a `Asset`.

Se agregaron nuevos tipos de recursos para la administración por IPS:

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
   <td colname="col2"> <p>Archivo de Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>Archivos de EPS y PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Documento de Microsoft® Word para archivos que terminan con .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Documento de Microsoft® Excel para archivos que terminan con .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Documento de Microsoft® PowerPoint para archivos que terminan con .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>Archivo RTF para archivos cargados que terminan con .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Se agregaron opciones adicionales a `UploadDirectoryJob` y `UploadUrlsJob` para controlar el procesamiento de archivos Postscript, Illustrator y PDF de forma independiente. Todos los trabajos existentes proporcionan los parámetros necesarios a cada una de las tres canalizaciones de procesamiento para que funcionen exactamente como se hacen hoy. El bloque `PostScriptOptions` original se usa para establecer el procesamiento de los archivos de Illustrator y EPS/PS. De forma opcional, se pueden proporcionar bloques de opciones de archivo específicas para especificar el procesamiento. La lista de cambios incluye:

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Ninguno </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterizar </span> (predeterminado) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Administre únicamente el recurso y no cree ningún derivado al cargar. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Procese el archivo EPS y PostScript en una imagen con la resolución y el espacio de color prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Tiene efecto al rasterizar el archivo en una imagen. Crea un fondo transparente si el archivo original se define de esta manera para superponer logotipos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proceso </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Ninguno </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterizar </span> (predeterminado) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Administre únicamente el recurso y no cree ningún derivado al cargar. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Procese el archivo en una imagen con la resolución y el espacio de color prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entero&gt; </span> </p> </td> 
   <td colname="col4"> <p>Resolución de rasterización. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espacio de color de destino para procesamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Opcional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Tiene efecto al rasterizar el archivo en una imagen. Crea un fondo transparente si el archivo original está definido de esta manera para crear logotipos superpuestos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proceso </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Ninguno </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterizar </span> (predeterminado) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Administre únicamente el recurso y no cree ningún derivado al cargar. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Procese el archivo en una imagen con la resolución y el espacio de color prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entero&gt; </span> </p> </td> 
   <td colname="col4"> <p>Resolución de rasterización. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espacio de color de destino para procesamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> catálogo PDF </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define si se debe combinar un PDF de varias páginas en un catálogo electrónico después de procesarlo (el valor predeterminado es verdadero). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define si las palabras de PDF se extraen en la base de datos para su posterior suministro a un servidor de búsqueda (el valor predeterminado es falso). </p> </td> 
  </tr> 
 </tbody> 
</table>

También puede realizar consultas desde `getScheduledJobs`.

Se ha modificado la propiedad de configuración `webservice.gzip.response` para que tome uno de los siguientes valores:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>No realice una respuesta gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>La respuesta Gzip solo si authHeader/gzipResponse es true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip si authHeader/gzipResponse es true o no hay ningún encabezado gzipResponse presente y el encabezado HTTP Accept-Encoding incluye gzip. (Predeterminado). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>Siempre hay una respuesta gzip, independientemente de los valores del encabezado. Utilice este valor únicamente con fines de depuración. </p> </td> 
  </tr> 
 </tbody> 
</table>
