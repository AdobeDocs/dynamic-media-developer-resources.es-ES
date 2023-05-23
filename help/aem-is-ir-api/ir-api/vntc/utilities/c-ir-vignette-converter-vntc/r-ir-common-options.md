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
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> cadena </span> </span> </p> </td> 
  <td class="stentry"> <p>Carpeta en la que se van a colocar los archivos de salida (incluido el archivo de registro, si <span class="codeph"> -log </span> se ha especificado). Puede ser una ruta absoluta o relativa al directorio de trabajo actual. La jerarquía de carpetas se crea si no existe. No se aplica al archivo especificado con <span class="codeph"> -log </span>. Si no se especifica, los archivos de salida se escriben en la carpeta en la que <span class="varname"> sourceFile </span> se encuentra en. If <span class="varname"> destFile </span> se especifica, siempre se escribirá en esa ubicación, y <span class="codeph"> -destpath </span> solo se aplica a los archivos de salida secundarios. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -imagen </span> </p> </td> 
  <td class="stentry"> <p>Si se especifica, la (primera) imagen de vista se extrae de la viñeta, una imagen de panel adecuada de un estilo de armario o la primera imagen de iluminación de un estilo de recubrimiento de ventana. La imagen extraída se guarda como archivo TIFF de resolución completa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Impide la generación de archivos de destino. Útil para extraer atributos rápidamente de <span class="varname"> sourceFile </span>. Solo la miniatura opcional ( <span class="codeph"> -thumbwidth </span>), imagen ( <span class="codeph"> -image </span>) y archivos de registro ( <span class="codeph"> -log </span>) se generen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> rival </span> </span> </p> </td> 
  <td class="stentry"> <p>Selecciona la codificación del JPEG con pérdidas para los datos de imagen de RGB y escala de grises incrustados en el archivo de salida, en lugar de PNG sin pérdidas. Las imágenes con alfa (RGBA) siempre se guardan con codificación PNG. <span class="varname"> rival </span> especifica la calidad JPEG (1...100); se recomienda 85 o superior. El valor predeterminado es <span class="codeph"> -jpegquality 0 </span>, que selecciona la codificación PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> ruta </span> </span> </p> </td> 
  <td class="stentry"> <p>Crea un archivo de registro con la ruta/nombre especificados Las rutas completas de todos los archivos de salida escritos en la carpeta de destino se escriben en el archivo de registro, así como algunas opciones adicionales, como información de versión y cualquier advertencia o error encontrado (consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Output </a> para obtener más información). No se crea ningún archivo de registro si <span class="codeph"> -log </span> no se ha especificado; en este caso, toda la salida de texto se escribe en <span class="codeph"> robusto </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> rival </span> </span> </p> </td> 
  <td class="stentry"> <p>Reducir la prioridad del <span class="filepath"> vntc </span> proceso. Esto se puede utilizar para que <span class="filepath"> vntc </span> no se apoderará de una CPU completa mientras se procesa una viñeta. Permite al sistema operativo dar más tiempo a otros procesos, más importantes. <span class="varname"> rival </span> especifica el porcentaje de prioridad inferior (0.. 100). El valor predeterminado es <span class="codeph"> -prioridad inferior 0 </span>, que no reduce la prioridad del <span class="filepath"> vntc </span> proceso. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> rival </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifique la cantidad máxima de memoria que <span class="filepath"> vntc </span> tiene permiso para usar en bytes. Cuándo <span class="filepath"> vntc </span> alcanza el límite máximo de memoria, detiene el procesamiento y produce un error. <span class="varname"> rival </span> especifica el límite máximo de memoria en bytes (0.. 3.758.096.384 (3,5 GB). Cuándo <span class="varname"> rival </span> es 0, el límite máximo de memoria está desactivado. El valor predeterminado es <span class="codeph"> -maxmem 3221225472 </span>, lo que significa un límite máximo de memoria de 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> cadena </span>" </span> </p> </td> 
  <td class="stentry"> <p>Especifica el separador colocado entre el nombre de archivo y el sufijo de tamaño/resolución para los nombres de archivo de salida generados automáticamente. Si no se especifica nada, el valor predeterminado es "-". Ignorado si <span class="varname"> destFile </span> o <span class="codeph"> -info </span> se ha especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -afilar <span class="varname"> rival </span> </span> </p> </td> 
  <td class="stentry"> <p>Permite enfocar las imágenes remuestreadas (escaladas) durante el procesamiento. Sólo se aplica al enfoque de miniaturas en el caso de archivos de estilo de archivador. </p> <p>Especifique 0 para desactivar el enfoque (predeterminado), 1 para activar el enfoque normal, 2 para activar la máscara de enfoque solo para el brillo o 3 para activar la máscara de enfoque para cada componente de color. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Establece el nivel de registro. El valor predeterminado es 1, que genera todos los mensajes de información, advertencia y error. Establezca el valor en 0 para deshabilitar todos los mensajes excepto los de error. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> cantidad </span> <span class="varname"> radio </span> <span class="varname"> umbral </span> </span> </p> </td> 
  <td class="stentry"> <p>Establece los parámetros de máscara de enfoque. Ignorado si <span class="codeph"> -afilar </span> se establece en 0 o 1; obligatorio si <span class="codeph"> -afilar </span> se establece en 2 o 3. <span class="varname"> cantidad </span> es un valor real entre 0,0 y 500,0, <span class="varname"> radio </span> es un valor real entre 0,0 y 10,0, y <span class="varname"> umbral </span> es un número entero entre 0 y 255. Consulte la descripción de <span class="codeph"> op_usm= </span> en la Referencia del protocolo del servicio de imágenes para obtener más información. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> rival </span> </span> </p> </td> 
  <td class="stentry"> <p>Compruebe que la viñeta dada sea una viñeta de producción adecuada. <span class="varname"> rival </span> representa la versión mínima del archivo de la viñeta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> rival </span> </span> </p> </td> 
  <td class="stentry"> <p>Versión del archivo de salida. Si se especifica, debe ser 0 o una versión de archivo de viñeta válida (no mayor que la versión de archivo predeterminada). Si se establece en 0 o no se especifica, el archivo de salida se crea con la versión del archivo más actual. Ignorado si <span class="codeph"> -info </span> se ha especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Devuelve la información de la versión de esta utilidad. Especifique sin nombre de archivo y otras opciones. </p> </td> 
 </tr> 
</table>
