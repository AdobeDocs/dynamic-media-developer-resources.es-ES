---
description: Las siguientes opciones controlan el procesamiento de los archivos de viñeta. Se omiten si sourceFile no es una viñeta.
seo-description: Las siguientes opciones controlan el procesamiento de los archivos de viñeta. Se omiten si sourceFile no es una viñeta.
seo-title: Opciones de viñetas
solution: Experience Manager
title: Opciones de viñetas
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---


# Opciones de viñetas{#options-for-vignettes}

Las siguientes opciones controlan el procesamiento de los archivos de viñeta. Se omiten si sourceFile no es una viñeta.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contenido</span> </p></td> 
  <td class="stentry"> <p>Crea un archivo XML que representa la jerarquía de objetos e incluye los atributos de objeto seleccionados. El contenido del archivo es el mismo que devuelve el comando <span class="codeph"> req=content</span>. El archivo tiene el mismo nombre que el archivo de origen, pero con un sufijo <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-recortar  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>Recorte la viñeta antes de escalar. </p> <p><span class="codeph"><span class="varname"> x</span>, <span class="varname"> </span></span> es la esquina superior izquierda del rectángulo de recorte y,  <span class="codeph"><span class="varname"> wid</span>, <span class="varname"> </span></span> es el tamaño del rectángulo de recorte. Los valores son coordenadas de píxeles relativas a la imagen de vista de resolución completa de la viñeta de origen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidnhein</span></span> </p> </td> 
  <td class="stentry"> <p>Recorte la viñeta antes de escalar. </p> <p><span class="codeph"><span class="varname"> xn</span>, <span class="varname"> </span></span> ynis la esquina superior izquierda del rectángulo de recorte y  <span class="codeph"><span class="varname"> widn</span>, <span class="varname"> </span></span> heinis el tamaño del rectángulo de recorte. Los valores se normalizan en relación con la imagen de vista de la viñeta de origen y deben estar entre 0,0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> width y  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> heinmust no deben ser mayores que 1,0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -materiales incrustados</span> </p></td> 
  <td class="stentry"> <p>Mantenga los materiales incrustados en la viñeta de salida. De forma predeterminada, los materiales se eliminan de la viñeta de salida. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Una o más alturas de la viñeta de salida en píxeles. Se omite si se especifica -info. <span class="varname"> </span> El valor puede ser 0, lo que indica la anchura de la viñeta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escalado de viñeta</a> para obtener información detallada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Habilite la extracción del archivo de mapa de imagen desde la viñeta. Los datos del mapa se escriben en un archivo HTML que contiene solamente un elemento <span class="codeph"> &lt;map&gt;</span>. El nombre del archivo de salida es el mismo que el archivo de imagen de salida, pero con un sufijo <span class="filepath"> .htm</span> . Se genera un mensaje de advertencia y no se crea ningún archivo si se especifica el comando pero no hay datos de asignación en la viñeta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -perfil</span> </p></td> 
  <td class="stentry"> <p>Guarda en un archivo una copia del perfil ICC incrustado en la viñeta. Se genera un mensaje de advertencia y no se crea ningún archivo de perfil ICC si se especifica el comando pero no hay ningún perfil ICC en la viñeta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pirámide</span> </p></td> 
  <td class="stentry"> <p>Crea una viñeta piramidal. Necesario cuando las imágenes procesadas se van a mostrar con visores de zoom Dynamic Media. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escalado de viñeta</a> para obtener más información. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-ancho de  <span class="varname"> miniatura</span></span> </p></td> 
  <td class="stentry"> <p>Restricción de ancho y alto de píxeles para la imagen en miniatura. Si se especifica, se genera una imagen JPEG que no sea más ancha ni más alta que <span class="varname"> ival</span> a partir de la imagen de vista de viñeta, una imagen de panel del archivo de estilo del archivador o el mapa de iluminación del primer estilo del archivo de estilo de las cubiertas de ventanas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Uno o más anchos de viñeta de salida en píxeles. Se omite si se especifica <span class="codeph"> -info</span>. <span class="varname"> </span> El valor puede ser 0, lo que indica la altura de la viñeta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escalado de viñeta</a> para obtener información detallada. </p></td> 
 </tr> 
</table>

