---
description: Utilidad de validación de imágenes. Esta utilidad de línea de comandos verifica los archivos de imagen para asegurarse de que son válidos y de que el servicio de imágenes puede leerlos sin dificultad.
solution: Experience Manager
title: validar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---

# validar{#validate}

Utilidad de validación de imágenes. Esta utilidad de línea de comandos verifica los archivos de imagen para asegurarse de que son válidos y de que el servicio de imágenes puede leerlos sin dificultad.

Todos los archivos de imagen que no son PTIFF deben pasar el parámetro validate antes de que el archivo esté disponible para el servicio de imágenes como imagen de origen. Las imágenes PTIFF deben validarse después de operaciones de copia potencialmente poco fiables.

## Uso {#usage}

` validate *`fileType`* [ *`opciones`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>Tipo de archivo de origen; se debe especificar al menos uno (-any permite los mismos tipos de archivo de imagen admitidos por IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> opciones </span> </span> </p> </td> 
  <td class="stentry"> <p>Otras opciones de comando (consulte más abajo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> Archivo de imagen. Ninguno o más, separados por espacios. </p> </td> 
 </tr> 
</table>

## Devuelve {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 si se realiza correctamente. Si se produce un error, se devuelve un valor distinto de cero y los detalles del error se envían a `stderr`.

## Opciones {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifica un archivo de texto independiente que contiene la lista de archivos de imagen. Un registro por archivo. If <span class="codeph"> -fileList </span> está incluido, <span class="varname"> sourceFile </span> no se debe especificar. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Habilita la verificación de todo el archivo de imagen. De forma predeterminada, solo se valida el encabezado de la imagen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Comprueba la validez del perfil de color incrustado. De forma predeterminada, el cuerpo del perfil no está marcado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> Rechaza imágenes con 16 bits por componente de imagen. Siempre especificado por el servidor de imágenes cuando valida imágenes de origen remoto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verboso </span> </p> </td> 
  <td class="stentry"> <p> Imprime más información si la imagen no es válida. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silencioso </span> </p> </td> 
  <td class="stentry"> <p>Deshabilita <span class="codeph"> robusto </span>/ <span class="codeph"> stderr </span> salida. Solo se devuelve un estado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Termina el procesamiento cuando se produce un error de validación de archivo, incluso si aún no se han validado los archivos adicionales. De forma predeterminada, el procesamiento continúa cuando se produce un error de validación </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versión </span> </p> </td> 
  <td class="stentry"> <p>Devuelve la información de versión de esta utilidad. Especifique sin ninguna otra opción. </p> </td> 
 </tr> 
</table>
