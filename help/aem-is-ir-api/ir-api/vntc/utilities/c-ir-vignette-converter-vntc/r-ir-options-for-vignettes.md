---
description: Las siguientes opciones controlan el procesamiento de archivos de viñeta. Se omiten si sourceFile no es una viñeta.
solution: Experience Manager
title: Opciones para viñetas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Opciones para viñetas{#options-for-vignettes}

Las siguientes opciones controlan el procesamiento de archivos de viñeta. Se omiten si sourceFile no es una viñeta.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -content</span> </p></td> 
  <td class="stentry"> <p>Crea un archivo XML que representa la jerarquía de objetos e incluye los atributos de objetos seleccionados. El contenido del archivo es el mismo que devolvió el comando <span class="codeph"> req=content</span>. El archivo tiene el mismo nombre que el archivo de origen, pero con un sufijo <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-recorte <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Recorte la viñeta antes de escalarla. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> es la esquina superior izquierda del rectángulo de recorte, y <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> es el tamaño del rectángulo de recorte. Los valores son coordenadas en píxeles relativas a la imagen de vista de resolución completa de la viñeta de origen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-recorte <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>Recorte la viñeta antes de escalarla. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> es la esquina superior izquierda del rectángulo de recorte, y <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> hein</span></span> es el tamaño del rectángulo de recorte. Los valores se normalizan en relación con la imagen de vista de la viñeta de origen y deben estar entre 0.0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> y <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> no debe ser mayor que 1.0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> - incrustar materiales</span> </p></td> 
  <td class="stentry"> <p>Mantenga los materiales incrustados en la viñeta de salida. De forma predeterminada, los materiales se eliminan de la viñeta de salida. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-altura <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Una o más alturas de viñeta de salida en píxeles. Se ignora si se especifica -info. <span class="varname"> ival</span> puede ser 0, que indica el ancho de la viñeta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> escala de viñeta</a> para obtener información detallada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Habilite la extracción del archivo de mapa de imagen de la viñeta. Los datos del mapa se escriben en un archivo HTML que contiene solo un elemento &lt;map&gt;<span class="codeph"> de tipo </span>. El nombre del archivo de salida es el mismo que el del archivo de imagen de salida, pero con un sufijo <span class="filepath"> .htm</span>. Se genera un mensaje de advertencia y no se crea ningún archivo si se especifica el comando, pero no hay datos de asignación en la viñeta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -perfil</span> </p></td> 
  <td class="stentry"> <p>Guarda una copia del perfil ICC incrustado en la viñeta en un archivo. Se genera un mensaje de advertencia y no se crea ningún archivo de perfil ICC si se especifica el comando pero no hay ningún perfil ICC en la viñeta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pirámide</span> </p></td> 
  <td class="stentry"> <p>Crea una viñeta piramidal. Necesario cuando las imágenes procesadas se deben mostrar con visores de zoom de Dynamic Media. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> escala de viñeta</a> para obtener más información. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Restricción de anchura y altura de píxeles para la imagen en miniatura. Si se especifica, se genera una imagen de JPEG que no es más ancha ni más alta que <span class="varname"> ival</span> a partir de la imagen de vista de viñeta, una imagen de panel del archivo de estilo de archivador o el mapa de iluminación del primer estilo del archivo de estilo de revestimientos de ventana. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> de ancho <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Una o más anchuras de viñeta de salida en píxeles. Se omite si se especifica <span class="codeph"> -info</span>. <span class="varname"> ival</span> puede ser 0, que indica la altura de la viñeta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> escala de viñeta</a> para obtener información detallada. </p></td> 
 </tr> 
</table>
