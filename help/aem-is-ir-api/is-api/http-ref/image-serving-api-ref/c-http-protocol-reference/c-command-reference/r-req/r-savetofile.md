---
description: Guardar imagen en archivo.
seo-description: Guardar imagen en archivo.
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# saveToFile{#savetofile}

Guardar imagen en archivo.

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> archivo</span> </p> </td> 
  <td class="stentry"> <p>Ruta relativa al archivo de imagen destinatario. </p></td> 
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
   <td> <p>Hora de creación del archivo (número de milisegundos desde medianoche, 1 de enero de 1970 UTC/GMT). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p> Número de píxeles de la imagen guardada. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> estado</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> Si </span> tiene éxito. </p> </td> 
  </tr> 
 </tbody> 
</table>

Devuelve el estado de respuesta HTTP 200 si se realiza correctamente y 403 si la solicitud falla o se agota el tiempo de espera. La respuesta tiene un tipo MIME `text/plain` y no se puede almacenar en caché.

El almacenamiento importante en archivos debe habilitarse especificando la ruta a una carpeta grabable existente en `attribute::SavePath`. `saveToFile=` falla si  `attribute::SavePath` está vacío.

*`file`* debe ser una ruta relativa combinada con  `attribute::SavePath`. El servicio de imágenes no crea carpetas. La carpeta destinatario debe existir en el servidor y tener la configuración de permisos adecuada para el servicio de imágenes para crear archivos.

`timeout=` es opcional. El tiempo de espera predeterminado es de 60.000 ms o el valor que se configure con `PS::SaveTimeout`.
