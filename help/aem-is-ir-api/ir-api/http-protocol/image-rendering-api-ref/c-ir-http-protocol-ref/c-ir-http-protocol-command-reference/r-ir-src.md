---
description: Archivo de material. Especifica datos de material, ya sea en forma de una única referencia de catálogo de material, o como uno o dos archivos de datos de imagen o material, separados por coma.
seo-description: Archivo de material. Especifica datos de material, ya sea en forma de una única referencia de catálogo de material, o como uno o dos archivos de datos de imagen o material, separados por coma.
seo-title: src
solution: Experience Manager
title: src
uuid: 52751bcc-a65d-4441-a3b5-802d27b54b54
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 2%

---


# src{#src}

Archivo de material. Especifica datos de material, ya sea en forma de una única referencia de catálogo de material, o como uno o dos archivos de datos de imagen o material, separados por coma.

`src = *``*|{{ *``*| *``*}[, *`catalogEntrymaterialFileEmbeddedRequestFile`*]`

`srcE= *`name`*`

`srcN= *`índice`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> EmbeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;brace;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;rbrace;'|&amp;lbrace;'&amp;lbrace;'<span class="varname"> ForeignReq</span>'&amp;rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>ID del catálogo de materiales (<span class="codeph"> atributo::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Registro del catálogo de materiales (<span class="codeph"> catálogo::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>Archivo de estilo de material (<span class="filepath"> .vnc</span> o <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>Archivo de datos de imagen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Solicitud al servicio de imágenes. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Solicitud de representación de imágenes. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ForeignReq</span> </p></td> 
  <td class="stentry"> <p>Solicitud a un servidor externo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>Nombre de un material incrustado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> índice</span> </p></td> 
  <td class="stentry"> <p>Número de índice basado en 0 para un material incrustado. </p></td> 
 </tr> 
</table>

Los materiales de textura, calco y papel tapiz repetibles requieren una sola imagen, que puede especificarse como archivo o como solicitud incrustada.

Los materiales del gabinete requieren un archivo de estilo de archivador ( [!DNL .vnc]), que no se puede especificar como una solicitud anidada. Un archivo de imagen de textura es opcional para los archivadores y, si se especifica, puede ser un archivo o una solicitud incrustada.

Los materiales de las cubiertas de ventanas requieren un archivo de estilo de las coberturas de ventana ( [!DNL .vnw]), que no se puede especificar como una solicitud anidada. Un archivo de textura es opcional y, si se especifica, puede ser un archivo o una solicitud incrustada.

El procesamiento de imágenes utiliza las mismas reglas que el servicio de imágenes para buscar catálogos de material, entradas de catálogo y archivos de datos. Consulte la descripción del *`object`* Tipo de datos en la documentación del servicio de imágenes para obtener más información.

*`materialFile`* es una ruta relativa a  `attribute::RootPath`.

*`foreignReq`* puede ser una dirección URL relativa a  `attribute::RootUrl`, o una dirección URL absoluta si  `attribute::AllowDirectUrls` se configura.

Si no se especifica *`catId`*, se utiliza el catálogo de sesiones.

`srcE=` y  `srcN=` proporcionan acceso a los materiales incrustados en la viñeta.

## Formatos de archivo compatibles {#section-f2186d3eef834fc8bbecb2bc68daacad}

La representación de imágenes admite los mismos formatos de imagen de origen que Dynamic Media Image Serving.

Las aplicaciones que requieran datos de imagen en varias resoluciones diferentes tendrán un mejor rendimiento al usar el formato de varias resoluciones TIFF (PTIFF) piramidal de Scene7. Image Serving incluye la utilidad Image Converter (IC) que crea imágenes PTIFF a partir de cualquier formato admitido.

Consulte la descripción de la utilidad IC en la documentación de Image Serving para obtener una lista completa de los formatos de archivo admitidos.

## Propiedades {#section-e68d03788d534e2184147987d51dfd0f}

Atributo de material. Necesario para todos los materiales excepto el color sólido (no permitido para materiales de color sólido). Todas las cadenas distinguen entre mayúsculas y minúsculas. *`index`* debe ser 0 o mayor.

## Predeterminado {#section-dde549c1917540dc8f9555962202da3c}

Ninguno.

## Ejemplo {#section-675865444f8a4d35b9fc6e58b36e3438}

Un MSS para un gabinete coloreado con una textura repetible independiente:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

El mismo material podría encontrarse en un catálogo de materiales `'cat`&#39; en el registro &#39; `12-3-2`&#39;:

`…&obj=cabinets&src=cat/12-3-2&…`

Solicitud anidada al servicio de imágenes para obtener una imagen de textura:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Véase también {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Catálogos](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2) de materiales,  [atributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402),  [atributo::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
