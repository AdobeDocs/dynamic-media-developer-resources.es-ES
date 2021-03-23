---
description: vntc genera datos de texto que se envían al servidor o al archivo de registro.
seo-description: vntc genera datos de texto que se envían al servidor o al archivo de registro.
seo-title: Salida
solution: Experience Manager
title: Salida
uuid: f2041600-408f-481c-95fc-3c112def7b8a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 0%

---


# Salida{#output}

vntc genera datos de texto que se envían al servidor o al archivo de registro.

Los datos tienen el formato de una propiedad `name=value` por registro de texto. Los valores de cadena no están entre comillas. Los mensajes de advertencia y error siempre se envían a `stderr`, incluso si se especifica `-log`.

Algunas propiedades pueden producirse varias veces en la misma salida. Se agrega un número de secuencia, que comienza por 0, al nombre de estas propiedades, separado por un punto. Estas propiedades se identifican a continuación con un sufijo `. *`n`*` después del nombre de la propiedad.

Se generan las siguientes propiedades:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>, <span class="varname"> ival</span>, <span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Color de fondo RGB del estilo del gabinete. Solo estilos de gabinete. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>La versión predeterminada del archivo de salida. También puede generarse el número de versión de archivo más alto que puede generar esta versión de <span class="filepath"> vntc</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">error.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Mensaje de error. La presencia de mensajes de error suele indicar que no se han creado archivos de salida o que no son adecuados para su uso en el procesamiento de imágenes. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">archivo.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Ruta/nombre completo de todos los archivos de salida, incluidas viñetas, archivos de estilo archivador, imágenes de resolución completa e imágenes en miniatura. Hay un atributo de archivo presente para cada archivo generado (excepto el archivo de registro). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">vidrio=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> equivale a 1 si el gabinete incluye puertas de cristal; de lo contrario, 0. Solo estilos de gabinete. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Nombre del iccProfile incrustado en el <span class="varname"> sourceFile</span>. </p> <p>Vacío si <span class="varname"> sourceFile</span> no está administrado por el color. Sólo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Mensaje informativo, como información de progreso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> equivale a 1 si  <span class="varname"> </span> sourceFile es una viñeta maestra, 0 si se ha procesado anteriormente con  <span class="filepath"> </span> vnUpdateor  <span class="filepath"> vntc</span>. Sólo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> equivale a 0 si  <span class="varname"> </span> sourceFile es un estilo de archivador que contiene datos de imagen JPEG (también se emite una advertencia en este caso); en caso contrario, 1. El gabinete y la ventana cubren únicamente archivos de estilo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Límite máximo de memoria que se aplica al proceso <span class="filepath"> vntc</span> en ejecución. <span class="varname"> </span> cadena es  <span class="varname"> ival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>,  <span class="varname"> ivalG</span> o  <span class="codeph"> 0</span> (deshabilitado). Donde <span class="varname"> K</span>, <span class="varname"> M</span> y <span class="varname"> G</span> se refieren a Kilobytes (1024 bytes), Megabytes (1048576 bytes) y Gigabytes (1073741824 bytes). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Escala del nivel de pirámide de menor resolución en la viñeta de salida. Solo está presente si se especifica <span class="codeph"> -pyramid</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Número de materiales guardados en el <span class="varname"> sourceFile</span>. Sólo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Número de imágenes de panel en este archivo de estilo .CAB. Solo estilos de gabinete. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Número de niveles de pirámide en la viñeta de salida. Solo está presente si se especifica -piramide. Sólo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">piramide=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 si la viñeta de origen o de destino tiene estructura piramidal. Sólo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Para los estilos de archivador, la resolución de objeto de <span class="varname"> sourceFile</span>. Para las viñetas, esta es la resolución de material recomendada para obtener resultados de procesamiento de la mejor calidad al procesar la viñeta de salida. Píxeles/pulgada (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>La resolución de objeto más pequeña de la viñeta de salida. Sólo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Resolución promedio del objeto en la viñeta de salida. Sólo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>La ruta <span class="varname"> sourceFile</span> completa. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>La versión de archivo de <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>El tamaño de píxel de la viñeta de entrada, la imagen de panel predeterminada de un archivo de estilo archivador o la primera imagen de opacidad de un archivo de estilo que cubre la ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Tipo de cubierta de ventana (solo estilos de cubierta de ventana): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=sombreado horizontal o persianas </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=persianas verticales </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=cortinas cortas de ancho completo </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=duraciones cortas izquierda/derecha </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=cortinas de ancho completo </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5 cintas de longitud completa izquierda/derecha </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=Cortina de café </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFile es una viñeta,  <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFile es un estilo archivador o  <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFile es un estilo de cubierta de ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>El valor especificado con <span class="codeph"> -version</span> o el valor de<span class="codeph"> defaultFileVersion</span> si<span class="codeph"> -version</span> no se especificó. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSize=<span class="varname"> ival</span>, <span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Lista separada por comas de los tamaños de píxeles de todas las vistas de la viñeta de salida (la vista de resolución completa de las viñetas piramidales), de la imagen de panel predeterminada de un archivo de estilo archivador o de la primera imagen de opacidad de un archivo de estilo que cubre una ventana. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> equivale a 1 si el estilo del archivador es texturable, 0 en caso contrario. No está presente para los archivos de estilo de viñetas y coberturas de ventanas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">advertencia.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Mensaje de advertencia (como cuando se especifica <span class="codeph"> -imagemap</span> pero no se encuentran datos de mapa en la viñeta). </p></td> 
 </tr> 
</table>

