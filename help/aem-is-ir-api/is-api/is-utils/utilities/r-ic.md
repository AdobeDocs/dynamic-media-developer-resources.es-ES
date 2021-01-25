---
description: Utilidad de conversión de imágenes.
seo-description: Utilidad de conversión de imágenes.
seo-title: ic
solution: Experience Manager
title: ic
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 08fabcc9-d0b5-4136-81fc-ac896c341e1d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '1208'
ht-degree: 2%

---


# ic {#ic}

Utilidad de conversión de imágenes.

`ic` es una herramienta de línea de comandos que convierte los archivos de imagen al formato TIFF piramidal optimizado (PTIFF). Aunque el servicio de imágenes puede procesar imágenes sin conversión, se recomienda convertir a PTIFF todas las imágenes de más de 512 x 512 píxeles. Esta conversión garantiza un rendimiento óptimo del servidor y el uso de los recursos, y minimiza los tiempos de respuesta.

Se recomienda que los archivos PTIFF que contengan contenido fotográfico tengan codificación JPEG (especifique `-jpegcompress`). El contenido generado por el equipo puede beneficiarse de una compresión sin pérdidas (ya sea `-deflatecompress` o `-lzwcompress`). A menos que sea necesaria una conversión de color o de tipo de píxel, los datos de la imagen de origen JPEG se transfieren al PTIFF sin descodificarlos, para evitar la degradación de la calidad. En este caso, las opciones de compresión especificadas solo se aplican a los niveles de pirámide de menor resolución.

Si no va a convertir imágenes de gran tamaño, no tiene que definir los parámetros que controlan la cantidad de memoria que debe utilizarse. Sin embargo, si lo está, proporcione `ic` más memoria mediante la configuración `-maxmem` que se describe a continuación. Una buena regla general para calcular la cantidad de memoria necesaria es multiplicar la anchura de la imagen por la altura de la imagen por el número de canales. Por ejemplo, cuatro para una imagen RGB con alfa por tres. Además, si los canales son de 16 bits por componente en lugar de 8 dobles, el resultado final.

## Uso {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>opciones</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Opciones de comando (véase más adelante). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Archivo de imagen de entrada única. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Archivo PTIFF de salida única (no válido si se utiliza con SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Carpeta que contiene imágenes de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Carpeta en la que se escriben los archivos PTIFF de salida. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-36a2dcfa39824d29b69547c432366219}

0 si se realiza correctamente. Si se produce un error, se devuelve un valor distinto de cero y los detalles del error se envían a `stderr`.

## Opciones {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -sin comprimir </span> </p> </td> 
   <td colname="col2"> <p>No comprima la imagen de salida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress  </span> </p> </td> 
   <td colname="col2"> <p>Utilice la compresión deflate (zip) (predeterminada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress  </span> </p> </td> 
   <td colname="col2"> <p>Utilice la compresión Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress  </span> </p> </td> 
   <td colname="col2"> <p>Utilice la codificación JPEG. Se omite si <span class="codeph"> <span class="varname"> sourceFile </span> </span> incluye datos alfa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality  &lt;&gt; quality  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Calidad JPEG (0-100; el valor predeterminado es 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance  </span> </p> </td> 
   <td colname="col2"> <p>Desactive la disminución de resolución de croma JPEG (puede mejorar la calidad del texto en color y los gráficos). Esto no afecta a las imágenes de salida que son CMYK o escala de grises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - &lt;&gt; cantidad máxima  </span>&gt;  &lt;&gt; radio  </span>&gt;  &lt;&gt; umbral  </span>&gt;  &lt;&gt; monocromo  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>Aplique una máscara de enfoque a los niveles de pirámide submuestreados. Consulte <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> para obtener más información. (No se aplica a la imagen de resolución completa). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath  </span> </p> </td> 
   <td colname="col2"> <p>Utilice la ruta del clip en el archivo de origen, si existe, para crear datos alfa asociados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi  &lt;&gt; dpi  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Resolución de impresión (ppp) para <span class="codeph"> <span class="varname"> destFile </span> </span>; si no se especifica, la resolución de impresión de <span class="codeph"> srcFile </span> se copia en <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - &lt;&gt; esquina de recorte automático  </span>&gt;  &lt;&gt; modo  </span>&gt;  &lt;&gt; tolerancia  </span>&gt;  &lt;&gt; archivo de información  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>Calcule un rectángulo de recorte para minimizar un fondo de color sólido. No se muestra información de recorte si el algoritmo de recorte automático tiene como resultado que se recorte toda la imagen. </p> <p>Para calcular el rectángulo de recorte sin convertir la imagen, especifique <span class="codeph"> -autorecortar </span> sin <span class="codeph"> -convertir </span> y sin <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>corner</b></i> - ul | ur | ll | lr </p>
   <p> Especifica qué esquina de la imagen se utiliza un punto de inicialización. Se omite si el modo es 1.</p>
   <p><i><b>modo</b></i> - 0 | 1</p>
   <p>Establezca el valor en 0 para recortar según el color del píxel de esquina especificado; funciona con datos de color premultiplicados si los datos alfa están asociados con la imagen de origen.</p>
   <p>Establezca en 1 para recortar según los datos alfa; corner se omite y 0 es siempre el valor de inicialización; no se aplica ningún recorte si no hay datos alfa asociados con la imagen de origen.</p> 
   <p><i><b>tolerancia</b></i> : tolerancia de coincidencia. Valor real de 0,0 a 1,0. Especifica la tolerancia para valores de componente de píxeles coincidentes. Establezca en 0 para coincidencias exactas.</p>
   <p><i><b>infoFile</b></i> - Ruta y nombre del archivo de salida XML en el que se escribirán los datos de información de recorte.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData  </span> </p> </td> 
   <td colname="col2"> <p>Copie metadatos XMP, si están disponibles, desde <span class="codeph"> <span class="varname"> sourceFile </span> </span> a <span class="codeph"> <span class="varname"> destFile </span> </span> sin modificaciones. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile  </span> </p> </td> 
   <td colname="col2"> <p> Incruste el perfil de color ICC en <span class="codeph"> <span class="varname"> destFile </span> </span>, si está disponible (no hay ningún perfil incrustado de forma predeterminada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile  &lt;&gt; archivo  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Ruta y nombre de un archivo perfil ICC. Define el espacio de color de <span class="codeph"> <span class="varname"> sourceFile </span> </span> y debe coincidir con su tipo de píxel. Solo debe especificarse si no hay ningún perfil incrustado en <span class="codeph"> <span class="varname"> sourceFile </span> </span>, ya que esto anula el perfil incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - &lt;&gt; archivo viewprofile  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Ruta y nombre de un archivo perfil ICC. Define el tipo de píxel y el espacio de color de <span class="codeph"> <span class="varname"> destFile </span> </span>. IC se convierte a este perfil si <span class="codeph"> <span class="varname"> sourceFile </span> </span> tiene un perfil incrustado o si también se especifica <span class="codeph"> -imageprofile </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual  </span> </p> </td> 
   <td colname="col2"> <p>Interpretación perceptual para conversiones de espacio de color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric  </span> </p> </td> 
   <td colname="col2"> <p> Calidad de representación colorimétrica relativa para conversiones de espacio de color (predeterminado). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric  </span> </p> </td> 
   <td colname="col2"> <p>Calidad de representación colorimétrica absoluta para conversiones de espacio de color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation  </span> </p> </td> 
   <td colname="col2"> <p>La saturación procesa la calidad para conversiones de espacio de color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation  </span> </p> </td> 
   <td colname="col2"> <p>Deshabilitar compensación de punto negro para ciertas conversiones de color </p> <p>Habilitado de manera predeterminada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8  </span> </p> </td> 
   <td colname="col2"> <p>Desactive el tramado (difusión de errores) al convertir el color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype  </span> </p> </td> 
   <td colname="col2"> <p> Desactive la conversión automática de CMYK a RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress  </span> </p> </td> 
   <td colname="col2"> <p>Forzar la descodificación y recodificación de imágenes de entrada JPEG. </p> <p> <b>Precaución:</b> la aplicación de esta opción puede reducir la calidad de imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2  </span> </p> </td> 
   <td colname="col2"> <p>Utilice un filtro de remuestreo de calidad estándar (bilineal). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8  </span> </p> </td> 
   <td colname="col2"> <p>Utilice un filtro de remuestreo de mayor calidad (ventana Lanczos) (predeterminado). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix  </span> </p> </td> 
   <td colname="col2"> <p>Utilice un filtro de remuestreo de mayor calidad (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp  </span> </p> </td> 
   <td colname="col2"> <p>Disminuya la resolución con el filtro de enfoque bicúbico de estilo Photoshop 8x8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage  </span> </p> </td> 
   <td colname="col2"> <p> Cuando se especifica como la primera opción, se suprime la salida de la información de uso cuando se encuentran opciones no válidas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -sobrescribir </span> </p> </td> 
   <td colname="col2"> <p>Permitir sobrescribir un <span class="codeph"> <span class="varname"> destFile </span> </span> existente. De forma predeterminada, se agrega un sufijo numérico al nombre del archivo para evitar la sobrescritura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden  </span> </p> </td> 
   <td colname="col2"> <p>Omitir archivos de origen ocultos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror  </span> </p> </td> 
   <td colname="col2"> <p>No detenga el procesamiento cuando se produzca un error. Solo tiene un efecto cuando se procesan varios archivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - &lt;&gt; archivo de registro  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Ruta y nombre del archivo de registro (el valor predeterminado es <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - &lt;&gt; nivel de registro  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Nivel de registro. </p> 
   <p>&lt; 0=""&gt;</p>
   <p>0 - Archivos de Lista que se van a procesar.</p>
   <p>1 - Añadir sistema de informes para archivos innecesarios.</p>
   <p>2 - Añadir el sistema de informes de progreso.</p>
   <p>3: Añada el sistema de informes en cada archivo encontrado.</p>
   <p>4: Añada el sistema de informes de progreso en el nivel de archivo.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend  </span> </p> </td> 
   <td colname="col2"> <p>Anexar al archivo de registro (predeterminado). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend  </span> </p> </td> 
   <td colname="col2"> <p>Sobrescribir archivo de registro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec  &lt;&gt; msec  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Intervalo de registro en mseg para el nivel de registro 2 o superior (el valor predeterminado es 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem  &lt;&gt; bytes  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Límite de uso de memoria. Debe ser de al menos 10 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent  &lt;&gt; percent  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Límite de uso de memoria. El valor predeterminado es el 25 % de la memoria física. Si ni <span class="codeph"> maxmem </span> ni <span class="codeph"> maxmempercent </span> se configuran explícitamente utiliza el valor predeterminado maxmempercent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -versión </span> </p> </td> 
   <td colname="col2"> <p> Devolver información de la versión de esta utilidad. Especifique sin otras opciones. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formatos de imagen de entrada admitidos {#section-ab13d941d6724e65b9f84b62d949d31c}

La siguiente tabla lista los formatos de archivo de imagen y las opciones de formato que admite IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Formato</b> </p> </th> 
   <th class="entry"> <p> <b> Pixel </b> <b> TypeBits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Compresión</b> </p> </th> 
   <th class="entry"> <p> <b> Notas</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Mapa de bits de Windows) </p> </td> 
   <td> <p> RGB | indexado </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> sin comprimir | RLE </p> </td> 
   <td> <p> 5/6 bits/canal indica la compatibilidad con RGB de 16 bits (5-5-5 y 5-6-5 bits/canal). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Postscript encapsulado) </p> </td> 
   <td> <p> CMYK | RGB | gris </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | Binary | JPEG </p> </td> 
   <td> <p> Solo se admiten los archivos EPS generados por Photoshop. </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> indexado </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> Si está presente, el valor de transparencia de la paleta se convierte en alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | gris </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | gris | grisA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> sin comprimir | comprimido </p> </td> 
   <td> <p> Solo imagen combinada; se omiten las capas y los canales adicionales. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> Sólo datos de mapa de bits; se omiten los datos vectoriales. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | gris | grisA | indexado </p> </td> 
   <td> <p> 3 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> comprimido </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | gris | grisA | indexado </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> sin comprimir | ZIP | LZW | JPEG | RÉGIMEN DEL CCITT | CCITT G3 | CCITT G4 | Paquetes </p> </td> 
   <td> <p> A excepción del primer canal alfa asociado, se omiten los canales adicionales. </p> </td> 
  </tr> 
 </tbody> 
</table>

Los perfiles ICC incrustados se reconocen en archivos EPS, JPG, PSD, PNG y TIFF.

Las rutas incrustadas y los metadatos de XMP se reconocen en archivos EPS, JPG, PSD y TIFF.

## Ejemplos {#section-3c1986b30315431989bd76b1ee5bef6d}

Convierta una sola imagen con la mejor calidad y guárdela en la misma carpeta:

`ic -convert src/myFile.png src/myFile.tif`

Convierta todas las imágenes en *`srcFolder`* a TIFF piramidales con codificación JPEG y colóquelas en *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Convierta todas las imágenes en *`srcFolder`*. Los datos de imagen codificados de los archivos JPG se utilizan para la compresión LZW sin pérdida de resolución completa para el resto de la pirámide de imagen de estas imágenes, así como para toda la imagen de salida de todos los archivos de entrada que no sean JPG. Tipos de píxeles, perfiles de color incrustados, metadatos de XMP, etc. se mantienen.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
