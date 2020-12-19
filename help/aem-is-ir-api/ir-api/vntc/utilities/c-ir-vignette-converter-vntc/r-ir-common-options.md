---
description: Las siguientes opciones se pueden aplicar independientemente del tipo de sourceFile.
seo-description: Las siguientes opciones se pueden aplicar independientemente del tipo de sourceFile.
seo-title: Opciones comunes
solution: Experience Manager
title: Opciones comunes
topic: Scene7 Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---


# Opciones comunes{#common-options}

Las siguientes opciones se pueden aplicar independientemente del tipo de sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath  <span class="varname"> string  </span> </span> </p> </td> 
  <td class="stentry"> <p>Carpeta en la que se van a colocar los archivos de salida (incluido el archivo de registro, si se especifica <span class="codeph"> -log </span>). Puede ser una ruta absoluta o relativa al directorio de trabajo actual. La jerarquía de carpetas se creará si no existe. No se aplica al archivo especificado con <span class="codeph"> -log </span>. Si no se especifica, los archivos de salida se escriben en la carpeta en la que se encuentra <span class="varname"> sourceFile </span>. Si se especifica <span class="varname"> destFile </span>, siempre se escribirá en esa ubicación y <span class="codeph"> -destpath </span> sólo se aplicará a los archivos de salida secundarios. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -imagen </span> </p> </td> 
  <td class="stentry"> <p>Si se especifica, la (primera) imagen de vista se extrae de la viñeta, una imagen de panel adecuada de un estilo de gabinete o la primera imagen de iluminación de un estilo de cubierta de ventana. La imagen extraída se guarda como archivo TIFF de resolución completa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Evita la generación de archivos destinatario. Resulta útil extraer rápidamente atributos de <span class="varname"> sourceFile </span>. Sólo se generan las miniaturas opcionales ( <span class="codeph"> -thumbwidth </span>), imágenes ( <span class="codeph"> -image </span>) y archivos de registro ( <span class="codeph"> -log </span>). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Selecciona la codificación JPEG con pérdida para los datos de imagen RGB y escala de grises incrustados en el archivo de salida, en lugar de PNG sin pérdida. Las imágenes con alfa (RGBA) siempre se guardan con codificación PNG. <span class="varname"> ival  </span> especifica la calidad JPEG (1...100); Se recomienda la utilización de 85 o superior. El valor predeterminado es <span class="codeph"> -jpegquality 0 </span>, que selecciona la codificación PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> ruta de registro  </span> </span> </p> </td> 
  <td class="stentry"> <p>Crea un archivo de registro con la ruta/nombre especificados Las rutas completas de todos los archivos de salida escritos en la carpeta de destino se escriben en el archivo de registro, así como algunas opciones de configuración adicionales, como información de la versión y cualquier advertencia o error encontrado (consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Salida </a> para obtener más información). No se crea un archivo de registro si no se especifica <span class="codeph"> -log </span>; en este caso, toda la salida de texto se escribe en <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> ival de menor prioridad  </span> </span> </p> </td> 
  <td class="stentry"> <p>Reduzca la prioridad del proceso <span class="filepath"> vntc </span>. Esto se puede usar para que <span class="filepath"> vntc </span> no se haga cargo de toda una CPU mientras se procesa una viñeta. Permite al sistema operativo dar más tiempo a otros procesos más importantes. <span class="varname"> ival  </span> especifica el porcentaje de prioridad inferior (0..100). El valor predeterminado es <span class="codeph"> -lowerpriority 0 </span>, que no disminuye la prioridad del proceso <span class="filepath"> vntc </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifique la cantidad máxima de memoria que <span class="filepath"> vntc </span> puede utilizar en bytes. Cuando <span class="filepath"> vntc </span> alcanza el límite máximo de memoria, detiene el procesamiento y produce un error. <span class="varname"> ival  </span> especifica el límite máximo de memoria en bytes (0.. 3.758.096.384 (3,5 GB)). Cuando <span class="varname"> ival </span> es 0, se desactiva el límite máximo de memoria. El valor predeterminado es <span class="codeph"> -maxmem 3221225472 </span>, lo que significa un límite máximo de memoria de 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separador "  <span class="varname"> cadena  </span>"  </span> </p> </td> 
  <td class="stentry"> <p>Especifica el separador que se coloca entre el nombre de archivo y el sufijo de tamaño/resolución para los nombres de archivo de salida generados automáticamente. Si no se especifica, el valor predeterminado es "-". Se omite si se especifica <span class="varname"> destFile </span> o <span class="codeph"> -info </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> marrón  </span> </span> </p> </td> 
  <td class="stentry"> <p>Permite el enfoque de imágenes remuestreadas (escaladas) durante el procesamiento. Solo se aplica al enfoque de miniaturas en el caso de archivos de estilo archivador. </p> <p>Especifique 0 para desactivar el enfoque (predeterminado), 1 para activar el enfoque normal, 2 para habilitar la máscara de enfoque solo para el brillo o 3 para habilitar la máscara de enfoque para cada componente de color. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelel  </span> </p> </td> 
  <td class="stentry"> <p>Establece el nivel de registro. El valor predeterminado es 1, que genera todos los mensajes de información, advertencia y error. Establezca en 0 para deshabilitar todos los mensajes excepto los mensajes de error. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> umbral de  </span> <span class="varname"> radio de la cantidad máxima  </span> <span class="varname">   </span> </span> </p> </td> 
  <td class="stentry"> <p>Establece los parámetros de máscara de enfoque. Se omite si <span class="codeph"> -sharpen </span> está configurado en 0 o 1; requerido si <span class="codeph"> -sharpen </span> está establecido en 2 o 3. <span class="varname"> amount  </span> es un valor real en el rango 0.0...500.0,  <span class="varname"> radius  </span> es un valor real en el rango 0.0...10.0 y  <span class="varname"> el umbral  </span> es un entero entre 0 y 255. Consulte la descripción de <span class="codeph"> op_usm= </span> en la Referencia del protocolo de servicio de imágenes para obtener más información. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valide que la viñeta dada sea una viñeta de producción adecuada. <span class="varname"> ival  </span> representa la versión mínima del archivo de la viñeta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Versión del archivo para el archivo de salida. Si se especifica, debe ser 0 o una versión de archivo de viñeta válida (no mayor que la versión de archivo predeterminada). Si se establece en 0 o no, el archivo de salida se crea con la versión de archivo más reciente. Se omite si se especifica <span class="codeph"> -info </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>Devuelve información de la versión de esta utilidad. Especifique sin nombre de archivo y otras opciones. </p> </td> 
 </tr> 
</table>

