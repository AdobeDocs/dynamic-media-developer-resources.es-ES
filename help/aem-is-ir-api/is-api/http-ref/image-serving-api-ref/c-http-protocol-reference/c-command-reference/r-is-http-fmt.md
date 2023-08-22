---
title: fmt
description: Formato de imagen de respuesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 5%

---

# fmt{#fmt}

Formato de imagen de respuesta.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | Descripción |
|---|---|
| `avif-alpha` | AVIF con pérdida y sin pérdida con canal alfa. |
| `avif` | AVIF con pérdidas y sin pérdidas. |
| `eps` | PostScript encapsulado binario sin comprimir. |
| `f4m` | Formato de manifiesto del servidor de flujo de Flash. |
| `gif-alpha` | GIF con entre 2 y 255 colores más transparencia de color clave. |
| `gif` | GIF con 2 a 256 colores. |
| `jpeg` | JPEG perdedor. |
| `jpeg2000-alpha` | JPEG 2000 sin pérdidas y con canal alfa. |
| `jpeg2000` | JPEG 2000 sin pérdidas y sin pérdidas. |
| `jpegxr-alpha` | JPEG XR sin pérdidas y con canal alfa. |
| `jpegxr` | JPEG XR con pérdidas y sin pérdidas. |
| `jpg` | JPG perdedor. |
| `m3u8` | Formato de manifiesto del servidor de flujo Apple. |
| `pdf` | Imagen incrustada en el PDF. |
| `pjpeg` | JPEG progresista. |
| `png-alpha` | PNG sin pérdidas de 24 bits con canal alfa. |
| `png` | PNG sin pérdidas de 24 bits. |
| `png8-alpha` | PNG sin pérdidas de 8 bits con canal alfa. |
| `png8` | PNG sin pérdidas de 8 bits. |
| `swf-alpha` | JPEG con pérdida y máscara comprimida con desinflado incrustada en un archivo swf AS2 de Adobe. |
| `swf` | JPEG con pérdida incrustado en un archivo swf AS2 de Adobe. |
| `swf3-alpha` | JPEG con pérdida y máscara comprimida con desinflado incrustada en un archivo swf AS3 de Adobe. **Nota:** los formatos swf y swf-alpha se utilizan mejor para aplicaciones de ActionScript 2 (Flash Player 8 y anteriores). Los formatos swf3 y swf3-alpha se recomiendan para su uso en aplicaciones ActionScript 3 (Flash Player 9 y posteriores). |
| `swf3` | JPEG con pérdida incrustado en un archivo swf AS3 de Adobe. |
| `tif-alpha` | TIFF con canal alfa. |
| `tif` | TIFF. |
| `webp-alpha` | WebP sin pérdidas y con canal alfa. |
| `webp` | WebP con pérdidas y sin pérdidas. |

| *`pixelType`* – rgb | gris | cmyk |
| *`pixelType`* | Descripción |
|---|---|
| `cmyk` | Devuelve datos de imagen CMYK. |
| `gray` | Devuelve datos de imagen en escala de grises. |
| `rgb` | Devuelve datos de imagen del RGB. |

| *`compression`* – none | lzw | zip | jpeg | con pérdidas | sin pérdidas |
| *`compression`* | Descripción |
|---|---|
| `jpeg` | Compresión JPEG (con pérdida). |
| `lossy` | Compresión WebP, JPEG 2000 y JPEG XR (con pérdida). |
| `lossless` | Compresión WebP, JPEG 2000 y JPEG XR (sin pérdidas). |
| `lzw` | Compresión LZW (Lempel-Ziv-Welch) (sin pérdidas). |
| `none` | Sin comprimir. |
| `zip` | Compresión &quot;Deflate&quot; (sin pérdidas). |

* *`format`* especifica el formato de codificación de imagen para los datos de imagen enviados al cliente y el tipo MIME de respuesta correspondiente para el encabezado de respuesta HTTP.
* *`pixelType`* se puede utilizar para realizar la conversión del espacio de color de salida cuando `icc=` no especificado.

  El perfil de color predeterminado correspondiente a *`pixelType`* se aplica. Si la gestión de colores está desactivada, se aplica una conversión naïve. *`pixelType`* se ignora cuando `icc=` se especifica, que determina el tipo de píxel de salida.

* *`compression`* solo se permite si `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr`, o `jpegxr-alpha` se especifica como *`format`*. Consulte la tabla siguiente para ver las opciones de compresión admitidas para estos formatos de imagen.

Puede utilizar `qlt=` para definir las opciones de codificación de JPEG para estos formatos: JPEG, TIFF con compresión de JPEG, PDF con compresión de JPEG y SWF. WebP, JPEG 2000 y JPEG XR también utilizan `qlt=` pero los valores dan como resultado calidades diferentes para los distintos formatos. Uso `quantize=` if `fmt=gif` o `fmt=gif-alpha`. Consulte las descripciones de los comandos para obtener más información. Los demás formatos no tienen opciones configurables.

Se devuelven 8 bits por componente de píxel para todos los *`formats`* y *`pixelTypes`* (8 bits por píxel para GIF).

En la tabla siguiente se enumeran las combinaciones válidas de *`format`*y *`pixelType`*, los tipos MIME de respuesta HTTP correspondientes, si los perfiles ICC se pueden incrustar (consulte [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) y qué opciones específicas de formato puede aplicar.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> formato</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> Tipo MIME de respuesta</b> </th> 
   <th class="entry"> <b>Incrustar perfil ICC</b> </th> 
   <th class="entry"> <b> Opciones</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> JPEG, JPG, JPEG </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>El <span class="codeph"> pscan= </span> El parámetro solo se aplica al formato pjpeg. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alfa </p> </td> 
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
   <td colname="col5"> <span class="codeph"> <span class="varname"> compresión </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>solo 'tiff'; 'tiff-alpha' no admite la compresión jpeg. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> se ignora a menos que <span class="varname"> compresión </span> se establece en <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alfa, swf-alfa3 </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> <p> <p>Nota: El Flash Player de Adobe ignora los perfiles ICC incrustados. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, gris, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sí </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compresión </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> se ignora a menos que <span class="codeph"> <span class="varname"> compresión </span> </span> se establece en <span class="codeph"> jpeg </span>. </p> </td> 
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
   <td colname="col2"> <p>rgb, gris </p> <p>Los datos se convierten a la paleta después de la conversión a gris o rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>No </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> Quantize= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compresión </span> </span> ( <span class="codeph"> con pérdidas </span>, <span class="codeph"> sin pérdidas </span>) </p> <p> <span class="codeph"> qlt= </span> se ignora para <span class="codeph"> sin pérdidas </span>. </p> <p>Dado que no existe el concepto de disminución de resolución de crominancia con el formato WebP, si utiliza un segundo valor con <span class="codeph"> qlt </span> (por ejemplo, <span class="codeph"> qlt=80,1 </span>) el segundo valor ( <span class="codeph"> 1 </span>) se ignora. </p> </td> 
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
  <tr valign="top"> 
   <td> <p> avif, avif-alfa </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>No </p> </td> 
   <td> <p>Igual que arriba. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual si `req=img` (predeterminado) o `req=mask`; se ignorará en caso contrario.

*`type`* se ignora si `iccProfile=` se ha especificado.

## Predeterminado {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, donde la variable *`defaultType`* se gestiona de la siguiente manera: Si `icc=` se ha especificado, *`defaultType`* corresponde al tipo de píxel del perfil ICC especificado. If `icc=` no se ha especificado, *`defaultType`* es `gray` if `req=mask`, de lo contrario `rgb`.

## Ejemplos {#section-b93222e652df404a84c69025247f07df}

**Solicite una imagen de vista previa pequeña y de baja calidad en formato JPEG (predeterminado):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Solicitar la misma imagen convertida a escala de grises:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Solicite la misma imagen en un formato sin pérdidas con canal alfa y en alta resolución:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Solicite el canal alfa para la misma imagen que una imagen de TIFF en escala de grises:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Convierta la misma imagen a cmyk con los perfiles ICC predeterminados:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Convierta la misma imagen a cmyk con un perfil ICC diferente e incruste el perfil en la imagen del TIFF:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Distribuya esta imagen como un archivo TIF con compresión JPEG sin conversión de tipo de píxel:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Convierta la imagen en un GIF bi-tonal con transparencia de key-color y fuerza los colores a blanco y negro:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Perezoso con un ajuste de calidad de 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Sin pérdidas con alfa:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Perezoso con un ajuste de calidad de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Sin pérdidas con alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Perezoso con un ajuste de calidad de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Sin pérdidas con alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Véase también {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [Quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
