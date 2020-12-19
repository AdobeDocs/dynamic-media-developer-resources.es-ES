---
description: Las siguientes opciones controlan el procesamiento de los archivos de viñeta. Se omiten si sourceFile no es una viñeta.
seo-description: Las siguientes opciones controlan el procesamiento de los archivos de viñeta. Se omiten si sourceFile no es una viñeta.
seo-title: Opciones de viñetas
solution: Experience Manager
title: Opciones de viñetas
topic: Scene7 Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# Opciones de viñetas{#options-for-vignettes}

Las siguientes opciones controlan el procesamiento de los archivos de viñeta. Se omiten si sourceFile no es una viñeta.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contenido</span> </p></td> 
  <td class="stentry"> <p>Crea un archivo XML que representa la jerarquía de objetos e incluye los atributos de objeto seleccionados. El contenido del archivo es el mismo que devuelve el comando <span class="codeph"> req=contents</span>. El archivo tiene el mismo nombre que el archivo de origen, pero con un sufijo <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-recortar  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>Recorte la viñeta antes de aplicar escala. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> </span></span> es la esquina superior izquierda del rectángulo de recorte y  <span class="codeph"><span class="varname"> anchura</span>,<span class="varname"> </span></span> es el tamaño del rectángulo de recorte. Los valores son coordenadas de píxeles relativas a la imagen de vista de resolución completa de la viñeta de origen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidnhein</span></span> </p> </td> 
  <td class="stentry"> <p>Recorte la viñeta antes de aplicar escala. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> </span></span> ynis la esquina superior izquierda del rectángulo de recorte y  <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> </span></span> heinis el tamaño del rectángulo de recorte. Los valores se normalizan en relación con la imagen de vista de la viñeta de origen y deben estar entre 0,0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> heinno debe ser mayor que 1,0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -materiales de incrustación</span> </p></td> 
  <td class="stentry"> <p>Mantenga los materiales incrustados en la viñeta de salida. De forma predeterminada, los materiales se eliminan de la viñeta de salida. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Una o más alturas de viñeta de salida en píxeles. Se omite si se especifica -info. <span class="varname"> </span> Ivalmay be 0, que indica la anchura de la viñeta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escalado de viñetas</a> para obtener información detallada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Active la extracción del archivo de mapa de imagen desde la viñeta. Los datos del mapa se escriben en un archivo HTML que contiene solamente un elemento <span class="codeph"> &lt;map&gt;</span>. El nombre del archivo de salida es el mismo que el archivo de imagen de salida, pero con un sufijo <span class="filepath"> .htm</span>. Se genera un mensaje de advertencia y no se crea ningún archivo si se especifica el comando pero no hay datos de mapa en la viñeta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -perfil</span> </p></td> 
  <td class="stentry"> <p>Guarda una copia del perfil ICC incrustado en la viñeta en un archivo. Se genera un mensaje de advertencia y no se crea ningún archivo de perfil ICC si se especifica el comando pero no hay ningún perfil ICC en la viñeta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -piramide</span> </p></td> 
  <td class="stentry"> <p>Crea una viñeta piramidal. Necesario cuando las imágenes procesadas se van a mostrar con los visores de zoom de Scene7. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escalado de viñetas</a> para obtener más información. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">- <span class="varname"> ival de ancho de miniatura</span></span> </p></td> 
  <td class="stentry"> <p>Restricción de anchura y altura de píxeles para la imagen en miniatura. Si se especifica, se genera una imagen JPEG que no es más ancha ni más alta que <span class="varname"> ival</span> a partir de la imagen de vista de viñeta, una imagen de panel del archivo de estilo de archivador o el mapa de iluminación del primer estilo del archivo de estilo de coberturas de ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Uno o varios anchos de viñeta de salida en píxeles. Se omite si se especifica <span class="codeph"> -info</span>. <span class="varname"> </span> Ivalmay be 0, que indica la altura de la viñeta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escalado de viñetas</a> para obtener información detallada. </p></td> 
 </tr> 
</table>

