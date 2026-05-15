---
description: Guardar imagen en archivo.
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
TQID: 'https://experienceleague.adobe.com/6JtqM7IKcYInFZ4zyuAIVwOabdXIltB2ZsVZP6pLL4E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 1%

---

# saveToFile{#savetofile}

Guardar imagen en archivo.

`req=saveToFile&name= *`archivo`*[&timeout= *`val`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> archivo</span> </p> </td> 
  <td class="stentry"> <p>Ruta relativa al archivo de imagen de destino. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Intervalo de espera (milisegundos). </p></td> 
 </tr> 
</table>

Guarda la imagen de respuesta en un archivo del servidor en lugar de devolvérsela al cliente.

Cuando la solicitud de guardado se completa correctamente, la solicitud devuelve varias propiedades con formato Java, incluidas las siguientes:

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> propiedad</b> </th> 
   <th class="entry"> <b> tipo</b> </th> 
   <th class="entry"> <b> Descripción</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p>Hora de creación del archivo (cantidad de milisegundos desde la medianoche del 1 de enero de 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> píxelesTotal</span> </p> </td> 
   <td> <p> entero </p> </td> 
   <td> <p> Número de píxeles de la imagen guardada. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> estado</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> hecho</span> si se realizó correctamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

Devuelve el estado de respuesta HTTP 200 si se realiza correctamente y 403 si la solicitud falla o se agota el tiempo de espera. La respuesta tiene un tipo MIME `text/plain` y no se puede almacenar en caché.

Importante Es necesario habilitar la opción Guardar en archivos especificando la ruta de acceso a una carpeta de escritura existente en `attribute::SavePath`. `saveToFile=` produce un error si `attribute::SavePath` está vacío.

*`file`* es obligatorio y debe ser una ruta relativa que se combine con `attribute::SavePath`. El servicio de imágenes no crea carpetas. La carpeta de destino debe existir en el servidor y tener la configuración de permisos adecuada para que el servicio de imágenes cree archivos.

`timeout=` es opcional. El tiempo de espera predeterminado es de 60.000 ms, o el valor que esté configurado con `PS::SaveTimeout`.
