---
description: Formato de imagen de respuesta.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 3%

---

# fmt{#fmt}

Formato de imagen de respuesta.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> formato</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Especifica el formato de codificación de imagen para los datos de imagen enviados al cliente y el tipo MIME de respuesta correspondiente para el encabezado de respuesta HTTP. </p> <p> <span class="codeph"> jpeg </span>: JPEG con pérdida </p> <p> <span class="codeph"> png </span>: PNG sin pérdidas </p> <p> <span class="codeph"> png-alpha </span>: PNG sin pérdidas con canal alfa </p> <p> <span class="codeph"> tif </span>: TIFF </p> <p> <span class="codeph"> tif-alpha </span>: TIFF con canal alfa </p> <p> <span class="codeph"> swf </span>: JPEG con pérdida incrustado en un archivo swf de Adobe </p> <p> <span class="codeph"> pdf </span>: imagen incrustada en el PDF </p> <p> <span class="codeph"> gif </span>: GIF con 2 a 256 colores </p> <p> <span class="codeph"> gif-alpha </span>: GIF con 2 a 255 colores más transparencia de clave de color </p> <p> <span class="codeph"> fxg </span>: FXG con variables y manipulación DOM aplicada </p> <p> <span class="codeph"> fxgraw </span>: FXG original almacenado en el servidor </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | gris | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Se puede utilizar para modificar el espacio de color de salida. </p> <p> <span class="codeph"> rgb </span>: devolver datos de imagen del RGB </p> <p> <span class="codeph"> gris </span>: devuelve datos de imagen en escala de grises </p> <p> <span class="codeph"> cmyk </span>: devolver datos de imagen CMYK </p> </td> 
 </tr> 
</table>

`tiffCompression` solo se permite si se especifica tif, tif-alpha como formato. Consulte la tabla siguiente para ver las opciones de compresión admitidas para estos formatos de imagen.

`qlt=` se puede usar para establecer las opciones de codificación de JPEG para estos formatos: JPEG, TIFF con compresión de JPEG. Quantize= puede usarse si fmt=gif o fmt=gif-alpha. Consulte las descripciones de los comandos para obtener más información. Los demás formatos no tienen opciones configurables.

Se devuelven 8 bits por componente de píxel para todos los formatos y `pixelTypes[7]`.

En la tabla siguiente se muestran las combinaciones válidas de formato y `pixelType`, los tipos MIME de respuesta HTTP correspondientes.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> formato</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Tipo MIME de respuesta </p> </th> 
   <th colname="col4" class="entry"> <p>Incrustar perfil ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Opciones </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, gris, cmyk </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alfa </p> </td> 
   <td> <p>rgb, gris </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb, gris, cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( ninguno | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alfa </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, gris, cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb, gris </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> cuantizar=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
