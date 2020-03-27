---
description: Formato de imagen de respuesta.
seo-description: Formato de imagen de respuesta.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Scene7 Image Serving - Image Rendering API
uuid: 29151740-3bbc-4c5e-bbc7-4afe9064ff5f
translation-type: tm+mt
source-git-commit: f490c0b927679917d5fbf3553e60aa90952735c3

---


# fmt{#fmt}

Formato de imagen de respuesta.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*]]

*`format`* — jpeg| jpg| pjpeg| png| png8| png-alpha| png8-alpha| tif| tif-alpha| swf| swf-alpha| swf3| swf3-alpha| Pasos| gif| gif-alpha| m3u8| f4m| web| webp-alpha| jpeg2000| jpeg2000-alpha| jpegxr| jpegxr-alpha

| *`format`* | Descripción |
|---|---| 
| `jpeg` | JPEG con pérdida |
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
| `swf` | JPEG con pérdida incrustado en un archivo swf de Adobe AS2 |
| `swf-alpha` | JPEG con pérdida y una máscara deflate comprimida incrustadas en un archivo swf de Adobe AS2 |
| `swf3` | JPEG con pérdida incrustado en un archivo swf de Adobe AS3 |
| `swf3-alpha` | JPEG con pérdida y una máscara con compresión de desinflado incrustadas en un archivo swf Adobe AS3. **Nota**: los formatos swf y swf-alpha se utilizan mejor para las aplicaciones ActionScript 2 (Flash Player 8 y versiones anteriores). se recomienda utilizar swf3 y swf3-alpha para aplicaciones ActionScript3 (Flash Player 9 y posterior) |
| `m3u8` | Formato de manifiesto de Apple Streaming Server |
| `f4m` | Formato de manifiesto de Flash Streaming Server |
| `webp` | WebP sin pérdida y con pérdida |
| `webp-alpha` | WebP con pérdida y pérdida con canal alfa |
| `jpeg2000` | JPEG 2000 con pérdida y pérdida |
| `jpeg2000-alpha` | JPEG 2000 con pérdida y sin pérdida con canal alfa |
| `jpegxr` | JPEG XR con pérdida y pérdida |
| `jpegxr-alpha` | JPEG XR con pérdida y pérdida con canal alfa |


| *`pixelType`* — rgb | gris | cmyk |
| *`pixelType`* | Descripción |
|---|---|
| `rgb` | Devuelve datos de imagen RGB. |
| `gray` | Devuelve datos de imagen en escala de grises. |
| `cmyk` | Devolver datos de imagen CMYK. |

| *`compression`* — none | lzw | zip | jpeg | pérdida | sin pérdida |
| *`compression`* | Descripción |
|---|---|
| `none` | Sin comprimir |
| `lzw` | Compresión LZW (Lempel-Ziv-Welch) (sin pérdida) |
| `zip` | Compresión &quot;Deflate&quot; (sin pérdida) |
| `jpeg` | Compresión JPEG (pérdida) |
| `lossy` | Compresión WebP, JPEG 2000 y JPEG XR (con pérdida) |
| `lossless` | Compresión WebP, JPEG 2000 y JPEG XR (sin pérdida) |

* *`format`* especifica el formato de codificación de imagen para los datos de imagen enviados al cliente y el tipo MIME de respuesta correspondiente para el encabezado de respuesta HTTP.
* *`pixelType`* puede utilizarse para realizar la conversión del espacio de color de salida cuando no `icc=` se especifique.

   Se aplica el perfil de color predeterminado correspondiente a *`pixelType`* . Si la administración de color está deshabilitada, se aplica la conversión ingenua. *`pixelType`* se ignora cuando `icc=` se especifica, lo que determina el tipo de píxel de salida.

* *`compression`* solo se permite si `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`o `jpegxr`se especifica como `jpegxr-alpha` *`format`*. Consulte la tabla siguiente para conocer las opciones de compresión admitidas para estos formatos de imagen.

Puede utilizar `qlt=` para definir las opciones de codificación JPEG para estos formatos: JPEG, TIFF con compresión JPEG, PDF con compresión JPEG y SWF. WebP, JPEG 2000 y JPEG XR también utilizan `qlt=` pero los valores tienen diferentes calidades para los diferentes formatos. Utilícelo `quantize=` si `fmt=gif` o `fmt=gif-alpha`. Consulte las descripciones de comandos para obtener más detalles. Los demás formatos no tienen opciones configurables.

Se devuelven 8 bits por componente de píxel para todos *`formats`* y *`pixelTypes`* (8 bits por píxel para GIF).

La siguiente tabla lista las combinaciones válidas de *`format`*y *`pixelType`*, los tipos MIME de respuesta HTTP correspondientes, si se pueden incrustar perfiles ICC (consulte [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) y qué opciones específicas de formato se pueden aplicar.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> formato</i></b> </th> 
   <th class="entry"> <b> <i> pixelType</i></b> </th> 
   <th class="entry"> <b> Tipo MIME de respuesta</b> </th> 
   <th class="entry"> <b>Incrustar perfil ICC</b> </th> 
   <th class="entry"> <b> Opciones</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>El parámetro <span class="codeph"> pscan= </span> sólo se aplica al formato pjpeg. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compresión </span></span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>"tiff" solamente; 'tiff-alpha' no admite compresión jpeg. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> se ignora a menos que <span class="varname"> la compresión </span> se establezca en <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> <p> <p>Nota:  Adobe Flash Player ignora los perfiles ICC incrustados. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compresión </span></span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> se ignora a menos que <span class="codeph"> la compresión <span class="varname"></span> se establezca en </span> jpeg <span class="codeph"> </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> <p>Los datos se convierten en paletas después de la conversión a gris o rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> cuantize= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>web, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compresión </span> </span> ( <span class="codeph"> con pérdida </span>, <span class="codeph"> sin pérdida </span>) </p> <p> <span class="codeph"> qlt= </span> se omite para <span class="codeph"> sin pérdida </span>. </p> <p>Dado que no existe ningún concepto de disminución de resolución de crominancia con el formato WebP, si utiliza un segundo valor con <span class="codeph"> qlt </span> (por ejemplo, <span class="codeph"> qlt=80,1 </span>) se ignora el segundo valor ( <span class="codeph"> 1 </span>). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, gris </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p>Igual que arriba. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p>Igual que arriba. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Solicitar atributo. Se aplica independientemente del ajuste de capa actual si `req=img` (predeterminado) o `req=mask`; se ignoró de otro modo.

*`type`* se ignora si `iccProfile=` se especifica.

## Predeterminado {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, donde el *`defaultType`* problema se gestiona de la siguiente manera: Si `icc=` se especifica, *`defaultType`* corresponde al tipo de píxel del perfil ICC especificado. Si no `icc=` se especifica, *`defaultType`* es `gray` if `req=mask`, de lo contrario es `rgb`.

## Ejemplos {#section-b93222e652df404a84c69025247f07df}

**Solicite una imagen de previsualización pequeña y de baja calidad en formato JPEG (predeterminado):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Solicite la misma imagen convertida a escala de grises:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Solicite la misma imagen en un formato sin pérdida con canal alfa y en alta resolución:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Solicite el canal alfa para la misma imagen que una imagen TIFF de escala de grises:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Convierta la misma imagen a cmyk con los perfiles ICC predeterminados:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Convierta la misma imagen a cmyk con un perfil ICC diferente e incruste el perfil en la imagen TIFF:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Proporcione esta imagen como archivo TIF con compresión JPEG sin conversión de tipo de píxel:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Convierta la imagen en un GIF bitonal con transparencia de color clave y fuerza los colores a blanco y negro:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Pérdida con un entorno de calidad de 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Sin pérdida con alfa:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Pérdida con un entorno de calidad de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Sin pérdida con alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Pérdida con un entorno de calidad de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Sin pérdida con alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Véase también {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [cuantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)pathEmbed=, escaneo.
