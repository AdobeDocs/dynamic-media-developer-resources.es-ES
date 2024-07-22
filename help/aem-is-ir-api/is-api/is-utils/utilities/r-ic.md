---
description: Utilidad de conversión de imágenes.
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 0%

---

# ic {#ic}

Utilidad de conversión de imágenes.

`ic` es una herramienta de línea de comandos que convierte los archivos de imagen al formato de TIFF piramidal optimizado (PTIFF). Aunque el servicio de imágenes puede procesar imágenes sin conversión, le recomendamos que convierta todas las imágenes de más de 512 x 512 píxeles a PTIFF. Esta conversión garantiza un rendimiento de servidor y un uso de recursos óptimos y minimiza los tiempos de respuesta.

Se recomienda que los archivos PTIFF con contenido fotográfico estén codificados en el JPEG (especifique `-jpegcompress`). El contenido generado por el equipo puede beneficiarse de la compresión sin pérdidas (`-deflatecompress` o `-lzwcompress`). A menos que se requiera una conversión de color o de tipo de píxel, los datos de la imagen de origen del JPEG se transfieren al PTIFF sin descodificación, para evitar la degradación de la calidad. En este caso, las opciones de compresión especificadas sólo se aplican a los niveles piramidales de baja resolución.

Si no está convirtiendo imágenes grandes, no tiene que definir los parámetros que controlan la cantidad de memoria que se debe utilizar. Sin embargo, si es así, dé a `ic` más memoria utilizando la configuración `-maxmem` que se describe a continuación. Una buena regla general para calcular la cantidad de memoria necesaria es multiplicar la anchura de la imagen por la altura de la imagen por el número de canales. Por ejemplo, cuatro para una imagen RGB con alfa por tres. Además, si los canales son de 16 bits por componente en lugar de 8, el resultado final será el doble.

## Uso {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>opciones</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Opciones de comando (consulte más abajo). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>archivoDeOrigen</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Archivo de imagen de entrada única. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Archivo PTIFF de salida única (no válido si se utiliza con SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>carpetaDeOrigen</i></span> </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> - sin comprimir </span> </p> </td> 
   <td colname="col2"> <p>No comprima la imagen de salida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Utilice la compresión deflate (zip) (predeterminada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Utilice la compresión Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>Utilice la codificación del JPEG. Se omitirá si <span class="codeph"> <span class="varname"> sourceFile </span> </span> incluye datos alfa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> quality </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Calidad JPEG (0-100; el valor predeterminado es 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>Deshabilite la disminución de resolución de croma JPEG (puede mejorar la calidad del texto y los gráficos en color). Esto no afecta a las imágenes de salida CMYK o en escala de grises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> cantidad </span>&gt; &lt; radio <span class="varname"> </span>&gt; &lt; umbral <span class="varname"> </span>&gt; &lt; <span class="varname"> monocromo </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Aplicar máscara de enfoque a los niveles piramidales submuestreados. Consulte <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> para obtener detalles. (No se aplica a la imagen con resolución completa). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - applyClippath </span> </p> </td> 
   <td colname="col2"> <p>Utilice la ruta del clip en el archivo de origen, si existe, para crear datos alfa asociados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -ppp &lt; <span class="varname"> ppp </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Resolución de impresión (ppp) para <span class="codeph"> <span class="varname"> destFile </span> </span>; si no se especifica, la resolución de impresión de <span class="codeph"> srcFile </span> se copia en <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autorecorte &lt; <span class="varname"> esquina </span>&gt; &lt; modo <span class="varname"> </span>&gt; &lt; tolerancia <span class="varname"> </span>&gt; &lt; archivo de información <span class="varname"> </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Calcule un rectángulo de recorte para minimizar un fondo de color sólido. No se genera ninguna información de recorte si el algoritmo de recorte automático provoca el recorte total de la imagen. </p> <p>Para calcular el rectángulo de recorte sin convertir la imagen, especifique <span class="codeph"> -autocrop </span> sin <span class="codeph"> -convert </span> y sin <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>esquina</b></i> - ul | ur | ll | lr </p>
   <p> Especifica la esquina de la imagen que debe utilizar un punto semilla. Se ignora si el modo es 1.</p>
   <p><i><b>modo</b></i> - 0 | 1</p>
   <p>Definir en 0 para recortar en función del color del píxel de esquina especificado; funciona en datos de color premultiplicados si los datos alfa están asociados a la imagen de origen.</p>
   <p>Establezca el valor en 1 para recortar en función de los datos alfa; se omite corner y 0 es siempre el valor de semilla; no se aplica ningún recorte si no hay datos alfa asociados con la imagen de origen.</p> 
   <p><i><b>tolerancia</b></i> - Tolerancia de coincidencias. Valor real 0,0 a 1,0. Especifica la tolerancia para valores de componente de píxeles coincidentes. Establezca el valor en 0 para las coincidencias exactas.</p>
   <p><i><b>infoFile</b></i>: ruta de acceso y nombre del archivo de salida XML en el que se escriben los datos de información de recorte.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>XMP Copie los metadatos, si están disponibles, de <span class="codeph"> <span class="varname"> sourceFile </span> </span> a <span class="codeph"> <span class="varname"> destFile </span> </span> sin ninguna modificación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> Incruste el perfil de color ICC en <span class="codeph"> <span class="varname"> destFile </span> </span>, si está disponible (ningún perfil está incrustado de forma predeterminada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> archivo </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ruta y nombre de un archivo de perfil ICC. Define el espacio de color de <span class="codeph"> <span class="varname"> sourceFile </span> </span> y debe coincidir con su tipo de píxel. Se debe especificar solamente si no hay ningún perfil incrustado en <span class="codeph"> <span class="varname"> sourceFile </span> </span>, ya que esto anula el perfil incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> archivo </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ruta y nombre de un archivo de perfil ICC. Define el tipo de píxel y el espacio de color de <span class="codeph"> <span class="varname"> destFile </span> </span>. IC se convierte a este perfil si <span class="codeph"> <span class="varname"> sourceFile </span> </span> tiene un perfil incrustado o si <span class="codeph"> -imageprofile </span> también está especificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - IntentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>Intento de representación perceptual para las conversiones del espacio de color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - IntentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> Interpretación colorimétrica relativa para conversiones del espacio de color (predeterminada). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - IntentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>Interpretación colorimétrica absoluta para conversiones del espacio de color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - IntentSaturation </span> </p> </td> 
   <td colname="col2"> <p>La saturación representa la intención para las conversiones del espacio de color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>Deshabilitar la compensación de punto negro para determinadas conversiones de color </p> <p>Habilitado de forma predeterminada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Deshabilite el tramado (difusión de error) al convertir el color. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> Deshabilite la conversión automática de CMYK a RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>Forzar la descodificación y la recodificación de las imágenes de entrada del JPEG. </p> <p> <b>Precaución:</b> La aplicación de esta opción puede reducir la calidad de la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>Utilice un filtro de remuestreo de calidad estándar (bilineal). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>Utilice un filtro de remuestreo de mayor calidad (ventana de Lanczos) (predeterminado). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Utilice un filtro de remuestreo de mayor calidad (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Disminución de resolución con el filtro bicúbico-sharp estilo Photoshop 8x8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> Cuando se especifica como primera opción, suprime la salida de la información de uso cuando se encuentran opciones no válidas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">: sobrescribir </span> </p> </td> 
   <td colname="col2"> <p>Permitir sobrescribir un elemento destFile </span> </span> de <span class="codeph"> <span class="varname"> existente. De forma predeterminada, se anexa un sufijo numérico al nombre del archivo para evitar que se sobrescriba. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>Omitir archivos de origen ocultos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>No detener el procesamiento cuando se produzca un error. Solo tiene efecto cuando se procesan varios archivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ruta de acceso y nombre del archivo de registro (el valor predeterminado es <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> nivel </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Nivel de registro. </p> 
   <p>&lt; 0 - Registro deshabilitado.</p>
   <p>0 - Archivos de lista para procesar.</p>
   <p>1 - Agregar informes para archivos innecesarios.</p>
   <p>2 - Agregar informes de progreso.</p>
   <p>3 - Añada informes sobre cada archivo encontrado.</p>
   <p>4 - Agregar informes de progreso en el nivel de archivo.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>Anexar al archivo de registro (predeterminado). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>Sobrescribir archivo de registro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Intervalo de registro en ms para el nivel de registro 2 y superior (el valor predeterminado es 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> bytes </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Límite de uso de memoria. Debe tener al menos 10 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Límite de uso de memoria. El valor predeterminado es el 25 % de la memoria física. Si ni <span class="codeph"> maxmem </span> ni <span class="codeph"> maxmempercent </span> se establecen explícitamente, utiliza maxmempercent de forma predeterminada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - versión </span> </p> </td> 
   <td colname="col2"> <p> Devolver información de versión de esta utilidad. Especifique sin ninguna otra opción. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formatos de imagen de entrada admitidos {#section-ab13d941d6724e65b9f84b62d949d31c}

En la tabla siguiente se enumeran los formatos de archivo de imagen y las opciones de formato que admite IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> Formato <b></b> </p> </th> 
   <th class="entry"> <p> <b> Tipo De Píxel</b> <b> Bits/Canal</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Canal</b> </p> </th> 
   <th class="entry"> <p> Compresión <b></b> </p> </th> 
   <th class="entry"> <p> <b> notas</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Mapa de bits de Windows) </p> </td> 
   <td> <p> RGB | indexado </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> sin comprimir | RLE </p> </td> 
   <td> <p> 5/6 bits/canal indica compatibilidad con RGB de 16 bits (5-5-5 y 5-6-5 bits/canal). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Postscript encapsulado) </p> </td> 
   <td> <p> CMYK | RGB | gris </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | Binario | JPEG </p> </td> 
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
   <td> <p> Si está presente, el valor de transparencia de la paleta se convierte a alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG </b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | gris </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | gris | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> sin comprimir | comprimido </p> </td> 
   <td> <p> Solo imagen combinada; se omiten las capas y los canales adicionales. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> Solo datos de mapa de bits; se omiten los datos vectoriales. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | gris | grayA | indexado </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> comprimido </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | gris | grayA | indexado </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> sin comprimir | ZIP | LZW | JPEG | REGLA CCITT | CCITT G3 | CCITT G4 | Bits de paquete </p> </td> 
   <td> <p> Con la excepción del primer canal alfa asociado, se omiten los canales adicionales. </p> </td> 
  </tr> 
 </tbody> 
</table>

Los perfiles ICC incrustados se reconocen en los archivos EPS, JPG, PSD, PNG y TIFF.

Las rutas incrustadas y los metadatos de la se reconocen en los archivos de EPS JPG, XMP de la aplicación, PSD y TIFF.

## Ejemplos {#section-3c1986b30315431989bd76b1ee5bef6d}

Convierta una sola imagen con la mejor calidad y manténgala en la misma carpeta:

`ic -convert src/myFile.png src/myFile.tif`

Convierta todas las imágenes de *`srcFolder`* en TIFF piramidales con codificación de JPEG y colóquelas en *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Convertir todas las imágenes de *`srcFolder`*. Los datos de imagen codificados de los archivos JPG se utilizan para la compresión LZW sin pérdidas y de nivel de resolución completa para el resto de la pirámide de imágenes de estas imágenes, así como para toda la imagen de salida de todos los archivos de entrada no JPG. XMP Los tipos de píxeles, los perfiles de color incrustados, los metadatos de la, etc. se mantienen.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
