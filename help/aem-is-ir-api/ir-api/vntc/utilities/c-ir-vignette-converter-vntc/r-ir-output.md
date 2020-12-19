---
description: vntc genera datos de texto que se envían al servidor o al archivo de registro.
seo-description: vntc genera datos de texto que se envían al servidor o al archivo de registro.
seo-title: Salida
solution: Experience Manager
title: Salida
topic: Scene7 Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# Salida{#output}

vntc genera datos de texto que se envían al servidor o al archivo de registro.

Los datos tienen el formato de una propiedad `name=value` por registro de texto. Los valores de cadena no están entre comillas. Los mensajes de advertencia y error siempre se envían a `stderr`, incluso si se especifica `-log`.

Determinadas propiedades se pueden producir varias veces en la misma salida. Se anexa un número de secuencia, comenzando por 0, al nombre de estas propiedades, separado por un punto. Estas propiedades se identifican a continuación con un sufijo `. *`n`*` después del nombre de la propiedad.

Se generan las siguientes propiedades:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Color de fondo RGB del estilo de gabinete. Solo estilos de archivador. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Versión predeterminada del archivo de salida. También puede generar el número de versión de archivo más alto que puede generar esta versión de <span class="filepath"> vntc</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">error.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Mensaje de error. La presencia de mensajes de error suele indicar que no se han creado archivos de salida o que no son adecuados para su uso en el procesamiento de imágenes. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">archivo.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Ruta/nombre completo de todos los archivos de salida, incluidas las viñetas, los archivos de estilo archivador, las imágenes de resolución completa y las imágenes en miniatura. Hay un atributo de archivo por cada archivo generado (excepto el archivo de registro). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">vidrio=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 si el gabinete incluye puertas de vidrio, 0 en caso contrario. Solo estilos de archivador. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Nombre del iccProfile incrustado en el <span class="varname"> sourceFile</span>. </p> <p>Vacío si <span class="varname"> sourceFile</span> no está administrado por color. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Mensaje informativo, como información de progreso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> equivale a 1 si  <span class="varname"> </span> sourceFile es una viñeta maestra, 0 si se ha procesado anteriormente con  <span class="filepath"> </span> vnUpdateor  <span class="filepath"> vntc</span>. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> equivale a 0 si  <span class="varname"> </span> sourceFile es un estilo de archivador que contiene datos de imagen JPEG (también se emite una advertencia en este caso); en caso contrario, 1. Solo los archivos de estilo archivadores y de cobertura de ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Límite máximo de memoria que se aplica al proceso <span class="filepath"> vntc</span> en ejecución. <span class="varname"> </span> stringes  <span class="varname"> ival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>,  <span class="varname"> ivalG</span> o  <span class="codeph">  </span> 0(deshabilitado). Donde <span class="varname"> K</span>, <span class="varname"> M</span> y <span class="varname"> G</span> se refieren a Kilobytes (1024 bytes), Megabytes (1048576 bytes) y Gigabytes (1073741824 bytes). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Escala del nivel de pirámide de menor resolución en la viñeta de salida. Sólo está presente si se especifica <span class="codeph"> -piramide</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Número de materiales guardados en el <span class="varname"> sourceFile</span>. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Número de imágenes de panel en este archivo de estilo archivador. Solo estilos de archivador. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Número de niveles de pirámide en la viñeta de salida. Sólo está presente si se especifica -pyramid. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">piramide=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 si la viñeta de origen o de destino tiene una estructura piramidal. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Para los estilos de archivador, la resolución de objeto del archivo<span class="varname"> sourceFile</span>. Para las viñetas, esta es la resolución de material recomendada para obtener resultados de procesamiento de la mejor calidad al procesar la viñeta de salida. Píxeles/pulgada (ppp). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>La resolución de objeto más pequeña de la viñeta de salida. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>La resolución media del objeto en la viñeta de salida. Solo viñetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>La ruta completa <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Versión de archivo de <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>El tamaño en píxeles de la viñeta de entrada, la imagen predeterminada del panel en un archivo de estilo archivador o la primera imagen de opacidad de un archivo de estilo de cobertura de ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Tipo de cobertura de ventana (solo estilos de cobertura de ventana): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=sombra horizontal o persianas </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=persianas verticales </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=cortinas cortas de ancho completo </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=cortinas cortas izquierda/derecha </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=cortinas de ancho completo </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=cortinas de longitud completa izquierda/derecha </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=Cortina de café </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valencia </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFile es una viñeta,  <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFile es un estilo de archivador o  <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFile es un estilo de cobertura de ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>No se especificó el valor especificado con <span class="codeph"> -version</span> o el valor de<span class="codeph"> defaultFileVersion</span> si<span class="codeph"> -version</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSize=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Lista separada por comas de los tamaños de píxel de todas las vistas de la viñeta de salida (la vista de resolución completa para las viñetas piramidales), de la imagen predeterminada del panel en un archivo de estilo archivador o de la primera imagen de opacidad de un archivo de estilo de cobertura de ventana. </p> </td> 
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

