---
description: Guarde la imagen en el archivo.
seo-description: Guarde la imagen en el archivo.
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---


# saveToFile{#savetofile}

Guarde la imagen en el archivo.

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> archivo</span> </p> </td> 
  <td class="stentry"> <p>Ruta relativa al archivo de imagen de destino. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Intervalo de tiempo de espera (milisegundos). </p></td> 
 </tr> 
</table>

Guarda la imagen de respuesta en un archivo del servidor en lugar de devolverla al cliente.

Cuando la solicitud de guardado se completa correctamente, devuelve varias propiedades con formato Java, entre las que se incluyen las siguientes:

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Propiedad</b> </th> 
   <th class="entry"> <b> Tipo</b> </th> 
   <th class="entry"> <b> Descripción</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p>Hora de creación del archivo (número de milisegundos desde la medianoche del 1 de enero de 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p> Número de píxeles en la imagen guardada. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> estado</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> </span> si tiene éxito. </p> </td> 
  </tr> 
 </tbody> 
</table>

Devuelve el estado de respuesta HTTP 200 si es correcto y 403 si la solicitud falla o se agota el tiempo de espera. La respuesta tiene el tipo MIME `text/plain` y no se puede almacenar en caché.

Importante Guardar en archivos debe habilitarse especificando la ruta a una carpeta grabable existente en `attribute::SavePath`. `saveToFile=` falla si  `attribute::SavePath` está vacío.

*`file`* es obligatorio y debe ser una ruta relativa que se combine con  `attribute::SavePath`. El servicio de imágenes no crea carpetas. La carpeta de destino debe existir en el servidor y tener la configuración de permiso adecuada para que Image Serving cree archivos.

`timeout=` es opcional. El tiempo de espera predeterminado es de 60.000 ms, o el valor que esté configurado con `PS::SaveTimeout`.
