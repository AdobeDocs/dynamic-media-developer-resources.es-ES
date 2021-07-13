---
description: Las siguientes opciones se pueden aplicar independientemente del tipo de sourceFile.
solution: Experience Manager
title: Opciones comunes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Opciones comunes{#common-options}

Las siguientes opciones se pueden aplicar independientemente del tipo de sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath  <span class="varname"> string  </span> </span> </p> </td> 
  <td class="stentry"> <p>Carpeta en la que se deben colocar los archivos de salida (incluido el archivo de registro, si se especifica <span class="codeph"> -log </span>). Puede ser una ruta absoluta o relativa al directorio de trabajo actual. La jerarquía de carpetas se creará si no existe. No se aplica al archivo especificado con <span class="codeph"> -log </span>. Si no se especifica, los archivos de salida se escriben en la carpeta en la que se encuentra <span class="varname"> sourceFile </span>. Si se especifica <span class="varname"> destFile </span> , siempre se escribirá en esa ubicación y <span class="codeph"> -destpath </span> solo se aplicará a los archivos de salida secundarios. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -imagen </span> </p> </td> 
  <td class="stentry"> <p>Si se especifica, la (primera) imagen de vista se extrae de la viñeta, una imagen de panel adecuada de un estilo de gabinete o la primera imagen de iluminación de un estilo de cubierta de ventana. La imagen extraída se guarda como un archivo TIFF de resolución completa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Evita la generación de archivos de destino. Útil para extraer rápidamente atributos de <span class="varname"> sourceFile </span>. Solo se generan las miniaturas opcionales ( <span class="codeph"> -thumbwidth </span>), la imagen ( <span class="codeph"> -image </span>) y los archivos de registro ( <span class="codeph"> -log </span>). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Selecciona la codificación JPEG con pérdida para los datos de imagen RGB y escala de grises incrustados en el archivo de salida, en lugar de PNG sin pérdida. Las imágenes con alfa (RGBA) siempre se guardan con codificación PNG. <span class="varname"> ival  </span> especifica la calidad JPEG (1...100); Se recomienda una versión superior o igual a 85. El valor predeterminado es <span class="codeph"> -jpegquality 0 </span>, que selecciona la codificación PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log  <span class="varname"> path  </span> </span> </p> </td> 
  <td class="stentry"> <p>Crea un archivo de registro con la ruta/nombre especificados Las rutas completas de todos los archivos de salida escritos en la carpeta de destino se escriben en el archivo de registro, así como algunas configuraciones adicionales, como información de versión y cualquier advertencia o error encontrado (consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Salida </a> para obtener más información). No se crea ningún archivo de registro si no se especifica <span class="codeph"> -log </span>; en este caso, toda la salida de texto se escribe en <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> ival de prioridad baja  </span> </span> </p> </td> 
  <td class="stentry"> <p>Reduzca la prioridad del proceso <span class="filepath"> vntc </span>. Se puede usar para que <span class="filepath"> vntc </span> no se haga cargo de toda una CPU mientras se procesa una viñeta. Permite al sistema operativo dar más tiempo a otros procesos más importantes. <span class="varname"> ival  </span> especifica el porcentaje de prioridad inferior (0..100). El valor predeterminado es <span class="codeph"> -lowerpriority 0 </span>, que no disminuye la prioridad del proceso <span class="filepath"> vntc </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifique la cantidad máxima de memoria que <span class="filepath"> vntc </span> puede usar en bytes. Cuando <span class="filepath"> vntc </span> alcanza el límite máximo de memoria, detiene el procesamiento y produce un error. <span class="varname"> ival  </span> especifica el límite máximo de memoria en bytes (0.. 3.758.096.384 (3,5 GB). Cuando <span class="varname"> ival </span> es 0, el límite máximo de memoria se desactiva. El valor predeterminado es <span class="codeph"> -maxmem 3221225472 </span>, lo que significa un límite máximo de memoria de 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separador " <span class="varname"> cadena  </span>"  </span> </p> </td> 
  <td class="stentry"> <p>Especifica el separador situado entre el nombre de archivo y el sufijo de tamaño/resolución para los nombres de archivo de salida autogenerados. Si no se especifica lo contrario, el valor predeterminado es "-". Se omite si se especifica <span class="varname"> destFile </span> o <span class="codeph"> -info </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> martillos  </span> </span> </p> </td> 
  <td class="stentry"> <p>Permite enfocar las imágenes remuestreadas (escaladas) durante el procesamiento. Solo se aplica a la nitidez de miniaturas en el caso de archivos de estilo de archivador. </p> <p>Especifique 0 para desactivar el enfoque (predeterminado), 1 para habilitar el enfoque normal, 2 para habilitar el enmascaramiento de enfoque solo para el brillo, o 3 para habilitar el enmascaramiento de enfoque para cada componente de color. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>Establece el nivel de registro. El valor predeterminado es 1, que envía todos los mensajes de información, advertencia y error. Establézcalo en 0 para deshabilitar todos los mensajes excepto los mensajes de error. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -Umbral de  <span class="varname"> radio de la  </span> <span class="varname"> cantidad  </span> <span class="varname"> de suma  </span> </span> </p> </td> 
  <td class="stentry"> <p>Define los parámetros de máscara de enfoque. Se omite si <span class="codeph"> -sharpen </span> está configurado en 0 o 1; obligatorio si <span class="codeph"> -sharpen </span> está configurado en 2 o 3. <span class="varname"> amount  </span> es un valor real en el rango 0.0...500.0,  <span class="varname"> radius  </span> es un valor real en el rango 0.0...10.0 y  <span class="varname"> threshold  </span> es un número entero entre 0 y 255. Consulte la descripción de <span class="codeph"> op_usm= </span> en Referencia del protocolo de servicio de imágenes para obtener más información. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valide que la viñeta dada sea una viñeta de producción adecuada. <span class="varname"> ival  </span> representa la versión mínima del archivo de la viñeta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Versión del archivo de salida. Si se especifica, debe ser 0 o una versión de archivo de viñeta válida (no mayor que la versión de archivo predeterminada). Si se establece en 0 o no se especifica, el archivo de salida se crea con la versión del archivo más actual. Se omite si se especifica <span class="codeph"> -info </span> . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>Devuelve información de la versión de esta utilidad. Especifique sin nombre de archivo y otras opciones. </p> </td> 
 </tr> 
</table>
