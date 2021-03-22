---
description: Formato de imagen de respuesta.
seo-description: Formato de imagen de respuesta.
seo-title: fmt
solution: Experience Manager
title: fmt
uuid: 78ee7545-5ad9-4240-bbfc-20efe3e42ed3
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 3%

---


# fmt{#fmt}

Formato de imagen de respuesta.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> format</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alfa | tif | tif-alfa | swf | pdf | gif | gif-alfa | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Especifica el formato de codificación de imagen para los datos de imagen enviados al cliente y el tipo MIME de respuesta correspondiente para el encabezado de respuesta HTTP. </p> <p> <span class="codeph">  jpeg  </span>: JPEG con pérdida </p> <p> <span class="codeph"> png  </span>: PNG sin pérdida </p> <p> <span class="codeph"> png-alfa  </span>: PNG sin pérdida con canal alfa </p> <p> <span class="codeph">  tif  </span>: TIFF </p> <p> <span class="codeph"> tif-alfa  </span>: TIFF con canal alfa </p> <p> <span class="codeph">  swf  </span>: JPEG con pérdida incrustado en un archivo swf de Adobe </p> <p> <span class="codeph"> pdf  </span>: imagen incrustada en PDF </p> <p> <span class="codeph"> gif  </span>: GIF con entre 2 y 256 colores </p> <p> <span class="codeph"> gif-alfa  </span>: GIF con entre 2 y 255 colores más transparencia de color clave </p> <p> <span class="codeph"> fxg  </span>: FXG con variables y manipulación DOM aplicada </p> <p> <span class="codeph">  fxgraw  </span>: FXG original almacenado en el servidor </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | gris | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Se puede utilizar para afectar al espacio de color de salida. </p> <p> <span class="codeph">  rgb  </span>: devolver datos de imagen RGB </p> <p> <span class="codeph"> gris  </span>: devolver datos de imagen en escala gris </p> <p> <span class="codeph"> cmyk  </span>: devolver datos de imagen CMYK </p> </td> 
 </tr> 
</table>

`tiffCompression` solo está permitido si tif, tif-alpha se especifica como formato. Consulte la siguiente tabla para ver las opciones de compresión compatibles con estos formatos de imagen.

`qlt=` se puede utilizar para definir las opciones de codificación JPEG para estos formatos: JPEG, TIFF con compresión JPEG. cuantize= se puede utilizar si fmt=gif o fmt=gif-alpha. Consulte las descripciones de los comandos para obtener más información. Los demás formatos no tienen opciones configurables.

Se devuelven 8 bits por componente de píxel para todos los formatos y `pixelTypes[7]`.

La siguiente tabla enumera las combinaciones válidas de formato y `pixelType`, los tipos MIME de respuesta HTTP correspondientes.

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
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alfa </p> </td> 
   <td> <p>rgb, gris </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb, gris, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( none | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> qlt=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, gris, cmyk </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>sí </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alfa </p> </td> 
   <td> <p>rgb, gris </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> cuantizar=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
