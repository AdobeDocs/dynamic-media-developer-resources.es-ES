---
description: Responder formato de imagen. Especifica el formato de codificación de imagen para los datos de imagen enviados al cliente y el tipo MIME de respuesta correspondiente para el encabezado de respuesta HTTP.
seo-description: Responder formato de imagen. Especifica el formato de codificación de imagen para los datos de imagen enviados al cliente y el tipo MIME de respuesta correspondiente para el encabezado de respuesta HTTP.
seo-title: fmt
solution: Experience Manager
title: fmt
uuid: 7c589119-d1b3-460f-acbd-5e8d10d0d976
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 4%

---


# fmt{#fmt}

Responder formato de imagen. Especifica el formato de codificación de imagen para los datos de imagen enviados al cliente y el tipo MIME de respuesta correspondiente para el encabezado de respuesta HTTP.

` fmt= *``*[,[ *``*][, *`formatpixelTypetiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> formato </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG con pérdida. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>JPG perdedor. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>PNG sin pérdidas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>PNG sin pérdida con canal alfa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alfa </p> </td> 
  <td class="stentry"> <p>TIFF con canal alfa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>JPEG con pérdida incrustada en un archivo swf de Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alfa </p> </td> 
  <td class="stentry"> <p>JPEG con pérdida y Máscara comprimida en deflación incrustada en un archivo swf de Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>Imagen incrustada en PDF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>Pasos </p> </td> 
  <td class="stentry"> <p>PostScript encapsulado binario sin comprimir. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>GIF con 256 colores. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>GIF con 255 colores más transparencia de color clave. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType  </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>Devuelve datos de imagen RGB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gris </p> </td> 
  <td class="stentry"> <p>Devuelve datos de imagen en escala gris. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>Devolver datos de imagen CMYK. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression  </span> </td> 
  <td class="stentry"> <p>ninguno </p> </td> 
  <td class="stentry"> <p>Sin comprimir. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>Compresión LZW (Lempel-Ziv-Welch) (sin pérdidas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>Compresión "Deflate" (sin pérdidas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>Compresión JPEG (pérdida). </p> </td> 
 </tr> 
</table>

*`pixelType`* afecta a la conversión del espacio de color de salida cuando no  `icc=` se especifica; se  *`pixelType`* aplica el perfil de color predeterminado correspondiente a . Si la administración de color está deshabilitada, se aplica la conversión ingenua. *`pixelType`* se ignora cuando  `icc=` se especifica , lo que determina el tipo de píxel de salida.

*`compression`* solo está permitido si tif, tif-alfa o PDF se especifican como  *`format`*. Consulte la siguiente tabla para ver las opciones de compresión compatibles con estos formatos de imagen.

`qlt-` establece las opciones de codificación JPEG para estos formatos: JPEG, TIFF con compresión JPEG, PDF con compresión JPEG y archivo SWF. Utilice `quantize=` si `fmt=gif` o `fmt=gif-alpha`. Consulte las descripciones de los comandos para obtener más información. Los demás formatos no tienen opciones configurables.

Se devuelven 8 bits por componente de píxel para todos los formatos y tipos de píxeles.

En la tabla siguiente se enumeran las combinaciones válidas de *`format`* y *`pixelType`*, los tipos MIME de respuesta HTTP correspondientes, si se pueden incrustar perfiles ICC (consulte [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)) y qué comandos de opción específicos de formato se pueden aplicar.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> formato </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType  </span> </p> </th> 
   <th colname="col3" class="entry"> <p>Tipo MIME de respuesta </p> </th> 
   <th colname="col4" class="entry"> <p>Incrustar perfil ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Opciones </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt=  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alfa </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alfa </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>sí </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> (ninguno|lzw|zip|jpeg), pathEmbed=, qlt  </span> </p> <p>( <span class="codeph"> qlt= </span> se ignora a menos que <span class="varname"> tiffCompression </span> esté configurado como 'jpeg'). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> <p>(El Flash Player ignora los perfiles ICC incrustados). </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> atributo::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> (none|zip|jpeg),qlt=  </span> </p> <p> ( <span class="codeph"> qlt= </span> se ignora a menos que <span class="varname"> tiffCompression </span> esté configurado como 'jpeg'). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pasos </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> <p>(Los datos se convierten en paletas después de la conversión a gris o gb). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Especifica el formato de codificación para los datos de imagen de respuesta enviados al cliente y el tipo MIME de respuesta correspondiente para el encabezado de respuesta HTTP.

`png-alpha` devuelve alfa no asociado (es decir, alfa no multiplica previamente los valores de píxeles), mientras que  `tif-alpha` y  `swf-alpha` devuelve alfa asociado (es decir, los valores alfa se multiplican previamente con los valores alfa). El canal alfa corresponde a la inversa de la máscara de fondo de la viñeta para `req=img` y a la máscara de grupo u objeto en el caso de `req=object`. Para aplicar alfa cuando se utiliza una solicitud IR anidada, añada `fmt=` con el formato de archivo alfa apropiado a la solicitud IR incrustada y a la solicitud principal. No se devuelven datos alfa si se especifica un perfil CMYK o escala de grises ICC con `icc=`.

## Propiedades {#section-eb12a82c69d84622bcea153dd84d95b3}

Puede ocurrir en cualquier parte de la solicitud.

## Predeterminado {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* el valor predeterminado es  `attribute::Format`y  *`tiffCompression`* el predeterminado es  `attribute::TiffEncoding`. *`pixelType`* el valor predeterminado es  `rgb` si no  `icc=` se especifica, de lo contrario corresponde al tipo de píxel del perfil ICC especificado.

## Véase también {#section-c55efc881fc94c70bff91b870e026a7b}

[atributo::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) ,  [atributo::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50),  [atributo::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e),  [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb),  [cuantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
