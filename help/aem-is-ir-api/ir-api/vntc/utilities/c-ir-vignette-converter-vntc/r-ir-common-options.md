---
title: Opciones comunes
description: Las siguientes opciones se pueden aplicar independientemente del tipo de sourceFile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Opciones comunes{#common-options}

Las siguientes opciones se pueden aplicar independientemente del tipo de sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> cadena </span> </span> </p> </td> 
  <td class="stentry"> <p>Carpeta en la que se van a colocar los archivos de salida (incluido el archivo de registro, si se especifica <span class="codeph"> -log </span>). Puede ser una ruta absoluta o una ruta relativa al directorio de trabajo actual. La jerarquía de carpetas se crea si no existe, pero no se aplica al archivo especificado con <span class="codeph"> -log </span>. Si no se especifica, los archivos de salida se escribirán en la carpeta en la que se encuentra el archivo de origen <span class="varname"> </span>. Si se especifica <span class="varname"> destFile </span>, siempre se escribe en esa ubicación y <span class="codeph"> -destpath </span> solo se aplica a los archivos de salida secundarios. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -imagen </span> </p> </td> 
  <td class="stentry"> <p>Si se especifica, la (primera) imagen de vista se extrae de la viñeta, una imagen de panel adecuada de un estilo de armario o la primera imagen de iluminación de un estilo de recubrimiento de ventana. La imagen extraída se guarda como archivo TIFF de resolución completa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -información </span> </p> </td> 
  <td class="stentry"> <p>Impide la generación de archivos de destino. Útil para extraer atributos rápidamente de un archivo de origen <span class="varname"> </span>. Solo se generan la miniatura opcional ( <span class="codeph"> -thumbwidth </span>), la imagen ( <span class="codeph"> -image </span>) y los archivos de registro ( <span class="codeph"> -log </span>). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Selecciona la codificación del JPEG con pérdidas para los datos de imagen de RGB y escala de grises incrustados en el archivo de salida, en lugar de PNG sin pérdidas. Las imágenes con alfa (RGBA) siempre se guardan con codificación PNG. <span class="varname"> vial </span> especifica la calidad JPEG (1...100); se recomienda 85 o superior. El valor predeterminado es <span class="codeph"> -jpegquality 0 </span>, que selecciona la codificación PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> ruta de acceso </span> </span> </p> </td> 
  <td class="stentry"> <p>Crea un archivo de registro con la ruta/nombre especificados. Las rutas de acceso completas de todos los archivos de salida escritos en la carpeta de destino se escriben en el archivo de registro y algunas opciones de configuración adicionales, como la información de versión y las advertencias o errores encontrados (vea <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Salida </a> para obtener detalles). No se crea ningún archivo de registro si no se especifica <span class="codeph"> -log </span>; en este caso, toda la salida de texto se escribe en <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - prioridad inferior <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Reduzca la prioridad del proceso <span class="filepath"> vntc </span>. Este proceso se puede utilizar para que <span class="filepath"> vntc </span> no se haga cargo de una CPU completa mientras se procesa una viñeta. Permite al sistema operativo dar más tiempo a otros procesos, más importantes. <span class="varname"> vial </span> especifica el porcentaje de prioridad inferior (0..100). El valor predeterminado es <span class="codeph"> -lowerpriority 0 </span>, que no reduce la prioridad del proceso <span class="filepath"> vntc </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifique la cantidad máxima de memoria que <span class="filepath"> vntc </span> puede usar en bytes. Cuando <span class="filepath"> vntc </span> alcanza el límite máximo de memoria, detiene el procesamiento y produce un error. El vial <span class="varname"> </span> especifica el límite máximo de memoria en bytes (0. 3.758.096.384 (3,5 GB). Cuando el vial <span class="varname"> </span> es 0, el límite máximo de memoria está desactivado. El valor predeterminado es <span class="codeph"> -maxmem 3221225472 </span>, lo que significa un límite máximo de memoria de 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separador " <span class="varname"> cadena </span>" </span> </p> </td> 
  <td class="stentry"> <p>Especifica el separador colocado entre el nombre de archivo y el sufijo de tamaño/resolución para los nombres de archivo de salida generados automáticamente. Si no se especifica nada, el valor predeterminado es "-". Se omite si se especifica <span class="varname"> destFile </span> o <span class="codeph"> -info </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -enfocar <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Permite enfocar las imágenes remuestreadas (escaladas) durante el procesamiento. Sólo se aplica al enfoque de miniaturas en archivos de tipo archivador. </p> <p>Especifique 0 para desactivar el enfoque (predeterminado), 1 para activar el enfoque normal, 2 para activar la máscara de enfoque solo para el brillo o 3 para activar la máscara de enfoque para cada componente de color. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Establece el nivel de registro. El valor predeterminado es 1, que genera todos los mensajes informativos, de advertencia y de error. Establezca el valor en 0 para deshabilitar todos los mensajes excepto los de error. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -suma <span class="varname"> importe </span> <span class="varname"> radio </span> <span class="varname"> umbral </span> </span> </p> </td> 
  <td class="stentry"> <p>Establece los parámetros de máscara de enfoque. Se omite si <span class="codeph"> -sharpen </span> se establece en 0 o 1; necesario si <span class="codeph"> -sharpen </span> se establece en 2 o 3. La cantidad <span class="varname"> </span> es un valor real en el intervalo 0,0...500,0, el radio <span class="varname"> </span> es un valor real en el intervalo 0,0...10,0 y el umbral <span class="varname"> </span> es un entero entre 0 y 255. Consulte la descripción de <span class="codeph"> op_usm= </span> en la Referencia de protocolo del servicio de imágenes para obtener información adicional. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Compruebe que la viñeta dada sea una viñeta de producción adecuada. El vial <span class="varname"> </span> representa la versión mínima del archivo de la viñeta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - versión <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Versión del archivo de salida. Si se especifica, debe ser 0 o una versión de archivo de viñeta válida (no mayor que la versión de archivo predeterminada). Si se establece en 0 o no se especifica, el archivo de salida se crea con la versión del archivo más actual. Se omite si se especifica <span class="codeph"> -info </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Devuelve la información de la versión de esta utilidad. Especifique sin nombre de archivo y otras opciones. </p> </td> 
 </tr> 
</table>
