---
description: Las siguientes opciones se pueden aplicar independientemente del tipo de sourceFile.
solution: Experience Manager
title: Opciones comunes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Opciones comunes{#common-options}

Las siguientes opciones se pueden aplicar independientemente del tipo de sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> string </span> </span> </p> </td> 
  <td class="stentry"> <p>Carpeta en la que se deben colocar los archivos de salida (incluido el archivo de registro, si <span class="codeph"> -log </span> ). Puede ser una ruta absoluta o relativa al directorio de trabajo actual. La jerarquía de carpetas se crea si no existe. No se aplica al archivo especificado con <span class="codeph"> -log </span>. Si no se especifica, los archivos de salida se escriben en la carpeta en la que <span class="varname"> sourceFile </span> está localizado. If <span class="varname"> destFile </span> se especifica, siempre se escribirá en esa ubicación, y <span class="codeph"> -destpath </span> solo se aplica a los archivos de salida secundarios. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -imagen </span> </p> </td> 
  <td class="stentry"> <p>Si se especifica, la (primera) imagen de vista se extrae de la viñeta, una imagen de panel adecuada de un estilo de gabinete o la primera imagen de iluminación de un estilo de cubierta de ventana. La imagen extraída se guarda como un archivo TIFF de resolución completa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Evita la generación de archivos de destino. Útil para extraer rápidamente atributos de <span class="varname"> sourceFile </span>. Solo la miniatura opcional ( <span class="codeph"> -thumbwidth </span>), imagen ( <span class="codeph"> -image </span>) y archivos de registro ( <span class="codeph"> -log </span>). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Selecciona la codificación del JPEG con pérdidas para los datos de imagen de RGB y escala de grises incrustados en el archivo de salida, en lugar de PNG sin pérdidas. Las imágenes con alfa (RGBA) siempre se guardan con codificación PNG. <span class="varname"> ival </span> especifica la calidad del JPEG (1...100); Se recomienda una versión superior o igual a 85. El valor predeterminado es <span class="codeph"> -jpegquality 0 </span>, que selecciona la codificación PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> ruta </span> </span> </p> </td> 
  <td class="stentry"> <p>Crea un archivo de registro con la ruta/nombre especificados Las rutas completas de todos los archivos de salida escritos en la carpeta de destino se escriben en el archivo de registro, así como algunas configuraciones adicionales, como información de versión y cualquier advertencia o error encontrado (consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Salida </a> para obtener más información). No se crea ningún archivo de registro si <span class="codeph"> -log </span> no se especifica; en este caso, toda la salida de texto se escribe en <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Reduzca la prioridad del <span class="filepath"> vntc </span> proceso. Se puede usar para que <span class="filepath"> vntc </span> no se hará cargo de toda una CPU mientras se procesa una viñeta. Permite al sistema operativo dar más tiempo a otros procesos más importantes. <span class="varname"> ival </span> especifica el porcentaje de prioridad inferior (0..100). El valor predeterminado es <span class="codeph"> -lowerpriority 0 </span>, lo que no disminuye la prioridad del <span class="filepath"> vntc </span> proceso. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifique la cantidad máxima de memoria que <span class="filepath"> vntc </span> se permite usar en bytes. When <span class="filepath"> vntc </span> alcanza el límite máximo de memoria, detiene el procesamiento y produce un error. <span class="varname"> ival </span> especifica el límite máximo de memoria en bytes (0.. 3.758.096.384 (3,5 GB). When <span class="varname"> ival </span> es 0, el límite máximo de memoria está desactivado. El valor predeterminado es <span class="codeph"> -maxmem 3221225472 </span>, lo que significa un límite máximo de memoria de 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separador " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>Especifica el separador situado entre el nombre de archivo y el sufijo de tamaño/resolución para los nombres de archivo de salida autogenerados. Si no se especifica lo contrario, el valor predeterminado es "-". Ignorado si <span class="varname"> destFile </span> o <span class="codeph"> -info </span> se ha especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Permite enfocar las imágenes remuestreadas (escaladas) durante el procesamiento. Solo se aplica a la nitidez de miniaturas en el caso de archivos de estilo de archivador. </p> <p>Especifique 0 para desactivar el enfoque (predeterminado), 1 para habilitar el enfoque normal, 2 para habilitar el enmascaramiento de enfoque solo para el brillo, o 3 para habilitar el enmascaramiento de enfoque para cada componente de color. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Establece el nivel de registro. El valor predeterminado es 1, que envía todos los mensajes de información, advertencia y error. Establézcalo en 0 para deshabilitar todos los mensajes excepto los mensajes de error. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> importe </span> <span class="varname"> radius </span> <span class="varname"> umbral </span> </span> </p> </td> 
  <td class="stentry"> <p>Define los parámetros de máscara de enfoque. Ignorado si <span class="codeph"> -sharpen </span> se establece en 0 o 1; obligatorio si <span class="codeph"> -sharpen </span> se establece en 2 o 3. <span class="varname"> importe </span> es un valor real en el rango 0.0...500.0, <span class="varname"> radius </span> es un valor real en el rango 0.0...10.0, y <span class="varname"> umbral </span> es un entero entre 0 y 255. Consulte la descripción de <span class="codeph"> op_usm= </span> en la Referencia del Protocolo de servicio de imágenes para obtener más información. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Valide que la viñeta dada sea una viñeta de producción adecuada. <span class="varname"> ival </span> representa la versión mínima del archivo de la viñeta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Versión del archivo de salida. Si se especifica, debe ser 0 o una versión de archivo de viñeta válida (no mayor que la versión de archivo predeterminada). Si se establece en 0 o no se especifica, el archivo de salida se crea con la versión del archivo más actual. Ignorado si <span class="codeph"> -info </span> se ha especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Devuelve información de la versión de esta utilidad. Especifique sin nombre de archivo y otras opciones. </p> </td> 
 </tr> 
</table>
