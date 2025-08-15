---
description: vntc genera datos de texto que se envían a stderr o al archivo de registro.
solution: Experience Manager
title: Output
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Output{#output}

vntc genera datos de texto que se envían a stderr o al archivo de registro.

Los datos tienen el formato de una propiedad `name=value` por cada registro de texto. Los valores de cadena no están entre comillas. Los mensajes de advertencia y error siempre se envían a `stderr`, aunque se especifique `-log`.

Ciertas propiedades pueden producirse varias veces en la misma salida. Se anexa un número de secuencia, que comienza por 0, al nombre de estas propiedades, separado por un punto. Estas propiedades se identifican a continuación con un sufijo `. *`n`*` después del nombre de propiedad.

Se generan las siguientes propiedades:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>El color de fondo RGB del estilo de archivador. Solo estilos de armario. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Versión predeterminada del archivo de salida. También es el número de versión de archivo más alto que puede generar esta versión de <span class="filepath"> vntc</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">error.<span class="varname"> n</span>=<span class="varname"> cadena</span></span> </p></td> 
  <td class="stentry"> <p>Mensaje de error. La presencia de mensajes de error suele indicar que no se ha creado ningún archivo de salida o que no son adecuados para su uso en el procesamiento de imágenes. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">archivo.<span class="varname"> n</span>=<span class="varname"> cadena</span></span> </p></td> 
  <td class="stentry"> <p>Ruta de acceso o nombre completos de todos los archivos de salida, incluidas viñetas, archivos de estilo de archivador, imágenes de resolución completa e imágenes en miniatura. Hay un atributo de archivo para cada archivo generado (excepto el archivo de registro). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">vidrio=<span class="varname"> vial</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> es 1 si el armario incluye puertas de vidrio, 0 en caso contrario. Solo estilos de armario. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Nombre del iccProfile incrustado en <span class="varname"> sourceFile</span>. </p> <p>Vacío si <span class="varname"> sourceFile</span> no está administrado por colores. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">información.<span class="varname"> n</span>=<span class="varname"> cadena</span></span> </p></td> 
  <td class="stentry"> <p>Mensaje informativo, como información de progreso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> es 1 si <span class="varname"> sourceFile</span> es una viñeta principal, 0 si se ha procesado anteriormente con <span class="filepath"> vnUpdate</span> o <span class="filepath"> vntc</span>. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> es 0 si <span class="varname"> sourceFile</span> es un estilo de contenedor que contiene datos de imagen de JPEG (en este caso también se muestra una advertencia), 1 en caso contrario. Sólo archivos de estilo de recubrimiento de armario y ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> cadena</span></span> </p></td> 
  <td class="stentry"> <p>Límite máximo de memoria que se aplica al proceso vntc<span class="filepath"> en ejecución de </span>. <span class="varname"> cadena</span> es <span class="varname"> ival</span>, <span class="varname"> ivalK</span>, <span class="varname"> ivalM</span>, <span class="varname"> ivalG</span> o <span class="codeph"> 0</span> (deshabilitado). Donde <span class="varname"> K</span>, <span class="varname"> M</span> y <span class="varname"> G</span> se refieren a kilobytes (1024 bytes), megabytes (1048576 bytes) y gigabytes (1073741824 bytes). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Escala del nivel piramidal de menor resolución en la viñeta de salida. Solo está presente si se especifica <span class="codeph"> -pyramid</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Número de materiales guardados en <span class="varname"> sourceFile</span>. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Número de imágenes de panel en este archivo de estilo de archivador. Solo estilos de armario. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>El número de niveles piramidales en la viñeta de salida. Solo está presente si se especifica -pyramid. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pirámide=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 si la viñeta de origen o de destino tiene una estructura piramidal. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Para los estilos de archivador, la resolución del objeto <span class="varname"> sourceFile</span>. En el caso de las viñetas, esta es la resolución de material recomendada para obtener resultados de procesamiento de mejor calidad al procesar la viñeta de salida. Píxeles/pulgada (ppp). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>La resolución de objeto más pequeña en la viñeta de salida. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Resolución media del objeto en la viñeta de salida. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Ruta de acceso <span class="varname"> sourceFile</span> totalmente cualificada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>La versión de archivo de <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>El tamaño en píxeles de la viñeta de entrada, la imagen predeterminada del panel en un archivo de estilo de archivador o la primera imagen de opacidad de un archivo de estilo de cobertura de ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Tipo de recubrimiento de ventana (sólo estilos de recubrimiento de ventana): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=persianas o sombras horizontales </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=persianas verticales </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=cortinas cortas de ancho completo </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=cortinas cortas izquierda/derecha </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=cortinas de ancho completo de longitud completa </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=cortinas de longitud completa izquierda/derecha </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=cortina de café </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sufijo=<span class="varname"> cadena</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> si <span class="varname"> sourceFile</span> es una viñeta, <span class="codeph"> vnc</span> si <span class="varname"> sourceFile</span> es un estilo de contenedor, o <span class="codeph"> vnw</span> si <span class="varname"> sourceFile</span> es un estilo de cobertura de ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>El valor especificado con <span class="codeph"> -version</span> o el valor de <span class="codeph"> defaultFileVersion</span> si no se especificó<span class="codeph"> -version</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Lista separada por comas de los tamaños de píxel de todas las vistas de la viñeta de salida (la vista de resolución completa para las viñetas piramidales), de la imagen del panel predeterminado en un archivo de estilo de archivador o de la primera imagen de opacidad de un archivo de estilo de cobertura de ventana. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> es 1 si el estilo del archivador es texturable, 0 en caso contrario. No está presente para archivos de estilo de viñetas y cubiertas de ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">advertencia.<span class="varname"> n</span>=<span class="varname"> cadena</span></span> </p></td> 
  <td class="stentry"> <p>Mensaje de advertencia (como cuando se especifica <span class="codeph"> -imagemap</span> pero no se encuentran datos de asignación en la viñeta). </p></td> 
 </tr> 
</table>
