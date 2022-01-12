---
title: Nuevas adiciones y cambios
description: Describe los cambios nuevos e implementados para la API de IPS v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 2%

---

# Nuevas adiciones y cambios{#new-additions-and-changes}

Describe los cambios nuevos e implementados para la API de IPS v4.0.

Se han implementado versiones de API en paralelo con WSDL independientes y espacios de nombres de esquema.

* Versiones anteriores de la API: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* Versión de SPS 4.0: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Se ha añadido `PostScriptOptions/alpha` campo .

Se ha añadido `VideoRootUrl` y `SwfRootUrl` propiedades para `getProperty` operación.

Se ha añadido opcional `appName` y `appVersion` parámetros a `authHeader` para rastrear la aplicación de llamada. Se ha añadido el registro a `ipsApiService.log`.

Se ha añadido la opción `serviceUrl` parámetro al servlet de generación WSDL. Este parámetro es útil para depurar proxies. Por ejemplo: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Implementado `getZipEntries` operación.

Se han implementado intervalos de búsqueda y se han escrito valores de comparación para las condiciones de campo del sistema.

Se ha añadido `'Asset'` constante de cadena de tipo de recurso, principalmente para permitir campos de metadatos entre recursos.

Implementado `trashState` param para `searchAssets`.

Implementado `getAssetPublishHistory` operación.

Se ha añadido opcional `faultHttpStatusCode` Encabezado SOAP para habilitar la gestión de errores en Flex. Para Flex, use `<faultHttpStatusCode>200</faultHttpStatusCode>`. El código de estado predeterminado para las respuestas a errores es `500 (Internal Server Error)`.

Se agregaron operaciones para restaurar recursos de la papelera y vaciar recursos de la papelera.

Se han implementado operaciones de CRUD.

Se ha añadido el indicador habilitado a `ImageMap` tipo y `saveImageMap` operación.

Se ha agregado compatibilidad con los trabajos Optimizar archivos restantes .

Se ha añadido `setAssetsPublishState` para actualizaciones de estado de publicación masiva.

Se ha añadido `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Obsoleto `saveMetadataField` operación en favor de una nueva `createMetadataField` y `updateMetadataField` operaciones.

Implementado `deleteAssetsParam` operación de eliminación por lotes.

Implementado `moveAssetsParam` operación de movimiento por lotes.

Implementado `deleteMetadataField` operación.

Implementado `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` operaciones.

Implementado `getAssetCounts`.

Se ha agregado compatibilidad con `setImageSetMembers` para `RenderSet` miembros de `ImageSet` activos.

Se ha añadido `replaceImage` operación.

Se ha añadido `copyImage` operación.

Se ha añadido `setUrlModifier` operación y `urlModifier/urlPostApplyModifier` campos para `LayerViewInfo`, `TemplateInfo`y `WatermarkInfo`.

Se ha añadido `createDerivedAsset` operación. Actualmente, la variable `ownerHandle` debe hacer referencia a un recurso de imagen y el tipo puede ser `AdjustedView` o `LayerView`.

Se ha añadido `createTemplate` operación. Llame a para crear recursos de plantilla o marca de agua.

Configuración de empresa IPS, `CompanySettings`, portado a la API de servicios web.

Se ha añadido `excludeByproducts` indicador de filtro a `searchAssets` operación. Establecer este indicador como verdadero se ejecuta `PSDlayer` imágenes y PDF.

Se ha añadido `getGenerationInfo` operación.

Se ha añadido `SystemMessage` nombre de propiedad a `getProperty` operación.

Se han modificado algunas constantes de cadena de tipo de recurso para que coincidan con los campos correspondientes de Información de recurso .

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Se ha modificado el formato de resultado de las operaciones por lotes para resumir los errores, las advertencias y el éxito.

Implementado `batchSetAssetMetadata` operación de metadatos por lotes.

Se ha implementado compatibilidad con datos específicos de la aplicación.

Se ha implementado compatibilidad con marcas booleanas para `createTemplate`, `extendLayers`y `extractText` para los trabajos de carga para controlar el proceso de procesamiento de Photoshop (similar a los cambios para agregar cargas de archivos).

Implementado `setImageMaps` y `setZoomTargets` operaciones.

Implementado `ViewerPreset` operaciones. Los tipos reconocidos son:

* `VideoPlayer` (El vídeo solo publica estos visores).
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Las máscaras del visor admiten dos parámetros: `skinFg` y `skinBg`. El código back-end realiza todo el procesamiento necesario para mantener la compatibilidad con versiones anteriores.

Implementado `getAssociatedAssets` operación.

Se ha añadido `ReprocessAssets` tipo de trabajo para permitir el reprocesamiento de archivos de origen primarios cargados anteriormente, incluida la recuperación de PDF y la reoptimización de imágenes.

Nuevo nombre `PropertySetType` tipo de campo a `propertyType`. Este cambio de nombre afecta a la variable `createPropertySetType` y `getPropertySetType/getPropertySetTypes` respuesta.

Implementado `batchSetImageFields` para admitir la configuración de datos de usuario de imagen y otros campos de imagen editables.

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

Implementado `getActivePublishContexts` operación. Esta operación devuelve una matriz de nombres de contexto de publicación con servidores de publicación activos para la empresa especificada. Los nombres de contexto de publicación actuales son:

* `ImageServing`
* `ImageRendering`
* `Video`

Implementado `getSearchStrings` operación. Devuelve una matriz de cadenas de búsqueda para el recurso dado.

Se han agregado parámetros de configuración regional para trabajos y un mecanismo para establecer la configuración regional para las operaciones de API. La cadena de configuración regional debe tener el formato `<language_code>[-<country_code>]`. El código de idioma es un código de dos letras en minúsculas, tal como se especifica en la norma ISO-639, y el código de país opcional es un código de dos letras en mayúscula, tal como se especifica en la norma ISO-3166.

Se ha agregado un parámetro de configuración regional opcional al `authHeader` Encabezado SOAP para establecer la configuración regional para operaciones de API. Si este parámetro no está presente, el encabezado HTTP `Accept-Language` se utiliza. Si este encabezado tampoco está presente, se utiliza la configuración regional predeterminada para el servidor IPS.

Se ha agregado compatibilidad con get/set para campos de metadatos con establecimiento inflexible de tipos.

Se ha implementado compatibilidad con encabezados SOAP y HTTP para el control de respuestas gzip.

Se ha añadido `gzipResponse` marcar como `authHeader`. Si no está presente, la API comprueba el `Accept-Encoding` encabezado.

Se agregó compatibilidad con searchAssets para condiciones de campo de metadatos con establecimiento inflexible de tipos.

* Para todos los tipos de campo, el valor se puede pasar con un operador de comparación de cadenas ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Para campos booleanos, `boolVal` puede pasarse con la variable `Equals` op.
* Para los campos Int, `longVal` se puede pasar con un operador de comparación numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minLong/maxLong` puede pasarse con operaciones de rango numérico ( `Between, NotBetween`).
* Para campos flotantes, `doubleVal` se puede pasar con un operador de comparación numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o `minDouble/maxDouble` puede pasarse con operaciones de rango numérico ( `Between, NotBetween`).
* Para los campos Fecha, puede pasar `dateVal` con un operador de comparación numérico ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) o puede pasar minDate/maxDate con operaciones de rango numérico ( `Between, NotBetween`).

Se ha añadido una descripción, `jobSubType`y `originalJobName` campos a `JobLog` tipo .

* `originalJobName` es el nombre del trabajo enviado a `submitJob` (sin sufijos de exclusividad ni nombres de trabajo de seguimiento).
* `jobSubType` solo usa `ImageServingPublishJob` trabajos (donde es uno de `full`, `increment, fullwithsearch,` o `fulloverride`).
* `description` es una cadena vacía para todos los tipos de trabajo, pero finalmente contiene información resumida del trabajo, como la ruta de carga.

Además, los campos siguientes no se incluyen en ambos `getJobLogs` y `getJobLogDetails`. En versiones anteriores, solo estaban disponibles con `getJobLogDetails`.

* `endDate` (si el trabajo se ha completado).
* `fileDuplicateCount` (anteriormente siempre era `0` con `getJobLogs`)
* `fileUpdateCount` (anteriormente siempre era `0` con `getJobLogs` y se incluyen en `fileSuccessCount`; ahora se divide en campos separados).

Se ha agregado el campo assetHandle a `JobLogDetail` tipo .

Se ha añadido un parámetro de descripción opcional a `submitJob`. Este parámetro se transfiere para recuperarse en `getScheduledJobs`, `getActiveJobs`y `getJobLogs`.

Se ha desaprobado el campo del sistema de SKU. El campo se omite si se transfiere como `SystemFieldCondition` a `searchAssets`.

Se ha añadido `excludeAssetTypeArray` filtrar a `searchAssets`.

Se ha añadido `MaskInfo` escriba a `Asset`.

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

Se han añadido opciones adicionales a `UploadDirectoryJob` y `UploadUrlsJob` para controlar el procesamiento de archivos Postscript, Illustrator y PDF de forma independiente. Todos los trabajos existentes proporcionan los parámetros necesarios a cada una de las tres canalizaciones de procesamiento para que funcionen exactamente como se hace hoy. El original `PostScriptOptions` se utiliza para configurar el procesamiento de los archivos Illustrator y EPS/PS. Opcionalmente, se pueden proporcionar bloques de opciones de archivo específicos para especificar el procesamiento. La lista de cambios incluye:

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proceso </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Ninguno </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterizar </span>(predeterminado) </p> </li> 
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
   <td colname="col4"> <p>Tiene efecto al rasterizar el archivo en una imagen. Crea un fondo transparente si el archivo original está definido de esta manera para superponer logotipos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> proceso </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Ninguno </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterizar </span> (predeterminado) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Administre solo el activo y no cree ningún derivado al cargarlo. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Procese el archivo en una imagen con la resolución y el espacio de color prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entero&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterización de la resolución. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Espacio de color </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espacio de color de destino para la renderización. </p> </td> 
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
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Administre solo el activo y no cree ningún derivado al cargarlo. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Procese el archivo en una imagen con la resolución y el espacio de color prescritos. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;entero&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rasterización de la resolución. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Espacio de color </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Espacio de color de destino para la renderización. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define si se debe combinar un PDF de página múltiple en un catálogo electrónico después de la renderización (el valor predeterminado es true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;booleano&gt; </span> </p> </td> 
   <td colname="col4"> <p>Define si las palabras del PDF se extraen en la base de datos para suministrarlas posteriormente a un servidor de búsqueda (el valor predeterminado es false). </p> </td> 
  </tr> 
 </tbody> 
</table>

También puede consultar desde `getScheduledJobs`.

Se ha modificado la variable `webservice.gzip.response` propiedad configuration para tomar uno de los siguientes valores:

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
