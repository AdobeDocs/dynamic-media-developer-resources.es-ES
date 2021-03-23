---
description: Formato de imagen de respuesta.
seo-description: Formato de imagen de respuesta.
seo-title: fmt
solution: Experience Manager
title: fmt
uuid: 29151740-3bbc-4c5e-bbc7-4afe9064ff5f
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 5%

---


# fmt{#fmt}

Formato de imagen de respuesta.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* — jpeg | jpg | pjpeg | png | png8 | png-alfa | png8-alfa | tif | tif-alfa | swf | swf-alpha | swf3 | swf3-alpha | Pasos | gif | gif-alfa | m3u8 | f4m | web | webp-alpha | jpeg2000 | jpeg2000-alfa | jpegxr | jpegxr-alpha

| *`format`* | Descripción |
|---|---| 
| `jpeg` | JPEG perdedor |
| `jpg` | JPG perdedor |
| `pjpeg` | JPEG progresivo |
| `png` | PNG sin pérdida de 24 bits |
| `png8` | PNG sin pérdida de 8 bits |
| `png-alpha` | PNG sin pérdida de 24 bits con canal alfa |
| `png8-alpha` | PNG sin pérdida de 8 bits con canal alfa |
| `tif` | TIFF |
| `tif-alpha` | TIFF con canal alfa |
| `pdf` | Imagen incrustada en PDF |
| `eps` | PostScript encapsulado binario sin comprimir |
| `gif` | GIF con entre 2 y 256 colores |
| `gif-alpha` | GIF con entre 2 y 255 colores más transparencia de color clave |
| `swf` | JPEG perdido incrustado en un archivo swf AS2 de Adobe |
| `swf-alpha` | JPEG perdedor y una máscara comprimida deflada incrustada en un archivo swf AS2 de Adobe |
| `swf3` | JPEG perdido incrustado en un archivo swf AS3 de Adobe |
| `swf3-alpha` | JPEG perdedor y una máscara comprimida deflate incrustada en un archivo swf AS3 de Adobe. **Nota**: los formatos swf y swf-alpha se utilizan mejor para las aplicaciones de ActionScript 2 (Flash Player 8 y anteriores). se recomienda el uso de swf3 y swf3-alpha para aplicaciones de ActionScript3 (Flash Player 9 y posteriores) |
| `m3u8` | Formato de manifiesto del servidor de transmisión de Apple |
| `f4m` | Formato del manifiesto del servidor de transmisión por Flash |
| `webp` | WebP con pérdida y pérdida |
| `webp-alpha` | WebP perdedora y sin pérdidas con canal alfa |
| `jpeg2000` | JPEG 2000 con pérdida y sin pérdida |
| `jpeg2000-alpha` | JPEG 2000 con canal alfa, con pérdida y pérdida |
| `jpegxr` | JPEG XR con pérdida y sin pérdida |
| `jpegxr-alpha` | JPEG XR con pérdida y sin pérdida con canal alfa |


| *`pixelType`* — rgb | gris | cmyk |
| *`pixelType`* | Descripción |
|---|---|
| `rgb` | Devuelve datos de imagen RGB. |
| `gray` | Devuelve datos de imagen en escala gris. |
| `cmyk` | Devolver datos de imagen CMYK. |

| *`compression`* — none | lzw | zip | jpeg | pérdida | sin pérdidas |
| *`compression`* | Descripción |
|---|---|
| `none` | Sin comprimir |
| `lzw` | Compresión LZW (Lempel-Ziv-Welch) (sin pérdidas) |
| `zip` | Compresión &quot;Deflate&quot; (sin pérdidas) |
| `jpeg` | Compresión JPEG (pérdida) |
| `lossy` | Compresión WebP, JPEG 2000 y JPEG XR (con pérdida) |
| `lossless` | Compresión WebP, JPEG 2000 y JPEG XR (sin pérdidas) |

* *`format`* especifica el formato de codificación de imagen para los datos de imagen enviados al cliente y el tipo MIME de respuesta correspondiente para el encabezado de respuesta HTTP.
* *`pixelType`* se puede utilizar para realizar la conversión del espacio de color de salida cuando no  `icc=` se especifique.

   Se aplica el perfil de color predeterminado correspondiente a *`pixelType`*. Si la administración de color está deshabilitada, se aplica la conversión ingenua. *`pixelType`* se ignora cuando  `icc=` se especifica , lo que determina el tipo de píxel de salida.

* *`compression`* solo está permitido si  `tif`,  `tif-alpha`,  `pdf`,  `webp`,  `webp-alpha`,  `jpeg2000`,  `jpeg2000-alpha`,  `jpegxr` o  `jpegxr-alpha` se especifican como  *`format`*. Consulte la siguiente tabla para ver las opciones de compresión compatibles con estos formatos de imagen.

Puede utilizar `qlt=` para establecer las opciones de codificación JPEG para estos formatos: JPEG, TIFF con compresión JPEG, PDF con compresión JPEG y SWF. WebP, JPEG 2000 y JPEG XR también utilizan `qlt=` pero los valores dan como resultado diferentes cualidades para los diferentes formatos. Utilice `quantize=` si `fmt=gif` o `fmt=gif-alpha`. Consulte las descripciones de los comandos para obtener más información. Los demás formatos no tienen opciones configurables.

Se devuelven 8 bits por componente de píxel para todos los *`formats`* y *`pixelTypes`* (8 bits por píxel para GIF).

En la tabla siguiente se enumeran las combinaciones válidas de *`format`*y *`pixelType`*, los tipos de MIME de respuesta HTTP correspondientes, si se pueden incrustar perfiles ICC (consulte [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) y qué opciones específicas de formato se pueden aplicar.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> Tipo MIME de respuesta</b> </th> 
   <th class="entry"> <b>Incrustar perfil ICC</b> </th> 
   <th class="entry"> <b> Opciones</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span>,  <span class="codeph"> pscan=  </span>,  <span class="codeph"> qlt=  </span>,  <span class="codeph"> xmpEmbed=  </span> </p> <p>El parámetro <span class="codeph"> pscan= </span> solo se aplica al formato pjpeg. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alfa </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alfa </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compresión  </span> </span> <p> ( <span class="codeph"> ninguno|lzw|zip|jpeg </span>) </p> <p>solo "tiff"; 'tiff-alpha' no admite compresión jpeg. </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> qlt=  </span> se ignora a menos que la  <span class="varname"> compresión  </span> se establezca en  <span class="codeph"> jpeg  </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> <p> <p>Nota:  El Flash Player de Adobe ignora los perfiles ICC incrustados. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> atributo::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compresión  </span> </span> <p> ( <span class="codeph"> ninguno|zip|jpeg </span>), <span class="codeph"> qlt= </span>) </p> <p> <span class="codeph"> qlt=  </span> se ignora a menos que la  <span class="codeph"> <span class="varname"> compresión  </span> </span> se establezca en  <span class="codeph"> jpeg  </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> Pasos </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> <p>Los datos se convierten a paletas después de la conversión a gris o rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> cuantizar=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>web, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compresión  </span> </span> (  <span class="codeph"> con pérdidas  </span>,  <span class="codeph"> sin pérdidas  </span>) </p> <p> <span class="codeph"> qlt=  </span> se ignora para  <span class="codeph"> sin pérdidas  </span>. </p> <p>Como no hay concepto de disminución de resolución de crominancia con el formato WebP, si utiliza un segundo valor con <span class="codeph"> qlt </span> (por ejemplo, <span class="codeph"> qlt=80,1 </span>), el segundo valor ( <span class="codeph"> 1 </span>) se ignora. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, gris </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p>Igual que arriba. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p>Igual que arriba. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual si `req=img` (predeterminado) o `req=mask`; ignorado en caso contrario.

*`type`* se ignora si  `iccProfile=` se especifica .

## Predeterminado {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, donde el  *`defaultType`* se gestiona de la siguiente manera: Si  `icc=` se especifica,  *`defaultType`* corresponde al tipo de píxel del perfil ICC especificado. Si no se especifica `icc=`, *`defaultType`* es `gray` si `req=mask`, de lo contrario es `rgb`.

## Ejemplos {#section-b93222e652df404a84c69025247f07df}

**Solicite una imagen de vista previa pequeña y de baja calidad en formato JPEG (predeterminado):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Solicite la misma imagen convertida a escala de grises:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Solicite la misma imagen en un formato sin pérdida con canal alfa y con alta resolución:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Solicite el canal alfa para la misma imagen que una imagen TIFF de escala gris:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Convierta la misma imagen a cmyk con los perfiles ICC predeterminados:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Convierta la misma imagen a cmyk usando un perfil ICC diferente e incruste el perfil en la imagen TIFF:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Proporcione esta imagen como archivo TIF con compresión JPEG sin conversión de tipo de píxel:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Convierta la imagen en un GIF bitonal con transparencia de color clave y fuerza los colores a blanco y negro:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Pérdida con un marco de calidad de 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Sin pérdidas con alfa:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Pérdida con un marco de calidad de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Sin pérdidas con alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Pérdida con un marco de calidad de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Sin pérdidas con alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Véase también {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [cuantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38),  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301),  [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
